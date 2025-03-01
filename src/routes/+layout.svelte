<script lang="ts">
  import '../app.css';

  import '@fontsource/inter/500.css';
  import '@fontsource/inter/500-italic.css';
  import '@fontsource/inter/700.css';
  import '@fontsource/inter/700-italic.css';
  import '@fontsource/ibm-plex-mono/500.css';
  import '@fontsource/ibm-plex-mono/500-italic.css';
  import '@fontsource/ibm-plex-mono/700.css';
  import '@fontsource/ibm-plex-mono/700-italic.css';

  import Footer from '$lib/components/Footer.svelte';
  import Header from '$lib/components/Header.svelte';
  import Sidebar from '$lib/components/Sidebar.svelte';

  let { children } = $props();
</script>

<div class="flex h-screen items-center justify-center">
  <div
    class="m-4 grid h-180 w-7xl grid-cols-[auto_1fr] grid-rows-[auto_1fr_auto] gap-2 rounded-xl bg-gray-950/5 p-2 shadow-xl outline outline-gray-900/5 dark:bg-white/10 dark:inset-ring dark:inset-ring-white/10"
  >
    <div class="col-span-2">
      <Header />
    </div>
    <Sidebar />
    <main
      class="rounded-xl bg-white px-6 py-8 inset-ring inset-ring-black/10 dark:bg-gray-950 dark:outline dark:outline-white/10"
    >
      {@render children?.()}
    </main>
    <div class="col-span-2">
      <Footer />
    </div>
  </div>
</div>

<style lang="postcss">
  @reference 'tailwindcss/theme';

  :global(html) {
    background-color: theme(--color-white);
  }

  @media (prefers-color-scheme: dark) {
    :global(html) {
      background-color: var(--color-gray-950);
    }
  }
</style>
