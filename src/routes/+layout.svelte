<script>
  import '../app.postcss';
</script>

<svelte:head>
  <title>RwXCorp</title>
  <meta name="title" content="RwXCorp" />
  <meta name="description" content="Explore RWXCorp open-source projects." />
  <meta name="theme-color" content="#ff8100" />

  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://rwxcorp.github.io/website" />
  <meta property="og:title" content="RwXCorp" />
  <meta property="og:description" content="Explore RWXCorp open-source projects." />
</svelte:head>

<div class="container mx-auto p-4">
  <slot />
</div>

<footer class="container mx-auto p-4 text-sm text-center">
  <span class="dark:text-orange-600">
    Supporting RwxCorp with
    <a
      aria-label="Github Sponsors"
      class="text-orange-900 dark:text-orange-200 hover:text-orange-900 transition duration-300 ease-in-out"
      href="https://github.com/sponsors/ramonrwx"
      target="_blank"
    >
      Github Sponsors
    </a>
  </span>
</footer>
