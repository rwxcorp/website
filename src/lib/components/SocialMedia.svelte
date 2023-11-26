<script>
  import Icon from '@iconify/svelte';
  const iconSize = 48;
</script>

<div class="text-2xl mb-5">
  <span class="border-b-4 border-orange-600">Follow</span>
</div>

<div class="flex flex-row justify-center md:justify-start space-x-3">
  <a aria-label="Github" href="https://github.com/rwxcorp">
    <Icon icon="mdi:github" height={iconSize} />
  </a>
  <a aria-label="Mastodon" href="https://hachyderm.io/@ramonrwx" rel="me">
    <Icon icon="mdi:mastodon" height={iconSize} /></a
  >
  <a aria-label="Twitch" href="https://twitch.tv/ramonrwx">
    <Icon icon="mdi:twitch" height={iconSize} /></a
  >
  <a aria-label="X" href="https://x.com/rwxramon">
    <Icon icon="mdi:twitter" height={iconSize} />
  </a>
</div>
