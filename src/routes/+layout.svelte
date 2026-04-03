<script lang="ts">
  import '../app.css';
  import Navbar from '$lib/components/Navbar.svelte';
  import Footer from '$lib/components/Footer.svelte';
</script>

<div class="flex flex-col min-h-screen">
  <Navbar />
  <main class="flex-1">
    <slot />
  </main>
  <Footer />
</div>
