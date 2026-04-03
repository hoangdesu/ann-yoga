<script lang="ts">
  import '../app.css';
  import Navbar from '$lib/components/Navbar.svelte';
  import Footer from '$lib/components/Footer.svelte';
  import { onNavigate } from '$app/navigation';

  // Use the View Transitions API for smooth page transitions.
  // SvelteKit calls this before every navigation; returning a Promise
  // lets SvelteKit coordinate the old-page exit and new-page enter.
  onNavigate((navigation) => {
    if (!document.startViewTransition) return;

    return new Promise((resolve) => {
      document.startViewTransition(async () => {
        resolve();
        await navigation.complete;
      });
    });
  });
</script>

<div class="flex flex-col min-h-screen">
  <Navbar />
  <main class="flex-1">
    <slot />
  </main>
  <Footer />
</div>

<style>
  /* Cross-fade for the entire page */
  :global(::view-transition-old(root)) {
    animation: fade-out 0.2s ease-out both;
  }

  :global(::view-transition-new(root)) {
    animation: fade-in 0.25s ease-in both;
  }

  @keyframes fade-out {
    from { opacity: 1; transform: translateY(0); }
    to   { opacity: 0; transform: translateY(-6px); }
  }

  @keyframes fade-in {
    from { opacity: 0; transform: translateY(8px); }
    to   { opacity: 1; transform: translateY(0); }
  }
</style>
