<script>
  import '../app.css';
  import TheHeader from '$lib/components/TheHeader.svelte';
  import TheFooter from '$lib/components/TheFooter.svelte';
</script>

<TheHeader />
<main class="bg-gray-300 min-h-screen">
  <div
    class="max-w-7xl lg:mx-20 md:mx-16 max-sm:mx-2 sm:mx-5"
  >
    <slot />
  </div>
</main>
<TheFooter />
