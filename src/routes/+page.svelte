<script lang="ts">
  import Header from '$lib/components/home/Header.svelte';
  import Sidebar from '$lib/components/home/Sidebar.svelte';
  import Footer from '$lib/components/home/Footer.svelte';
</script>

<div class="flex h-screen items-center justify-center">
  <div
    class="grid h-180 w-7xl grid-cols-[auto_1fr] grid-rows-[auto_1fr_auto] [&>*]:border-2 [&>*]:border-solid"
  >
    <div class="col-span-full">
      <Header />
    </div>
    <Sidebar />
    <main>Main</main>
    <div class="col-span-full">
      <Footer />
    </div>
  </div>
</div>
