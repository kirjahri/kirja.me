<script lang="ts">
  import '../app.css';

  import '@fontsource/inter/400.css';
  import '@fontsource/inter/400-italic.css';
  import '@fontsource/ibm-plex-mono/700.css';
  import '@fontsource/ibm-plex-mono/700-italic.css';

  import Footer from '$lib/components/Footer.svelte';
  import Header from '$lib/components/Header.svelte';
  import Sidebar from '$lib/components/Sidebar.svelte';

  let { children } = $props();
</script>

<div class="flex h-screen items-center justify-center">
  <div
    class="m-4 grid h-180 w-7xl grid-cols-[auto_1fr] grid-rows-[auto_1fr_auto] gap-4 rounded-lg border-2 border-solid p-4"
  >
    <div class="col-span-2">
      <Header />
    </div>
    <Sidebar />
    <main class="rounded-lg border-2 border-solid p-4">
      {@render children?.()}
    </main>
    <div class="col-span-2">
      <Footer />
    </div>
  </div>
</div>
