<script>
  import { onMount } from 'svelte';
  import { writable } from 'svelte/store';

  let repos = writable([]);

  // fetch Github repositories data
  async function fetchGithubRepos() {
    try {
      const response = await fetch('https://api.github.com/users/rwxcorp/repos');
      const data = await response.json();
      repos.set(data);
    } catch (err) {
      console.error(err);
    }
  }

  onMount(fetchGithubRepos);
</script>

<svelte:head>
  <link rel="preconnect" crossorigin="anonymous" href="https://api.github.com/" />
  <link rel="dns-prefetch" crossorigin="anonymous" href="https://api.github.com" />
</svelte:head>

<div class="text-2xl mt-5 mb-5">
  <span class="border-b-4 border-orange-600">Open source projects</span>
</div>

<ul class="flex flex-col gap-3 md:grid md:grid-cols-3 md:auto-rows-auto">
  {#each $repos as repo (repo.id)}
    <li class="rounded border-2 dark:border-none dark:bg-zinc-900 p-5">
      <a
        aria-label={repo.full_name}
        class="text-[20px] text-orange-900 dark:text-orange-600 hover:text-orange-950 transition duration-300 ease-in-out"
        href={repo.html_url}
        target="_blank"
      >
        {repo.full_name}
      </a>
      <p>
        {repo.description ? repo.description : 'No description for this repository'}
      </p>
    </li>
  {/each}
</ul>
