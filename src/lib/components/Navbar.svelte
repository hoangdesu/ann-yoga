<script lang="ts">
  import { resolve } from '$app/paths';
  import { page } from '$app/stores';

  // Helper function to check if a link is active.
  function isActive(path: string) {
    const currentPath = $page.url.pathname;
    // Using 'as any' to bypass SvelteKit 2's strict route literal types for dynamic variables.
    const resolvedPath = resolve(path as any);
    
    // Exact match for the current page
    if (path === '/') {
      return currentPath === resolvedPath;
    }
    return currentPath.startsWith(resolvedPath) && resolvedPath !== '/';
  }

  // Shared classes for links
  const baseLinkClasses = "transition-colors duration-300 font-notoserif text-lg tracking-tight pb-1 border-b-2";
  const activeLinkClasses = "text-olive-900 border-primary font-semibold";
  const inactiveLinkClasses = "text-stone-600 border-transparent font-medium hover:text-primary";
</script>

<nav class="fixed top-0 w-full z-50 bg-[#fafaf5]/80 backdrop-blur-md shadow-[0_10px_40px_-15px_rgba(26,28,25,0.04)]">
  <div class="flex justify-between items-center h-20 px-8 max-w-7xl mx-auto">
    <a href={resolve('/')} class="font-notoserif text-2xl font-bold text-olive-900 tracking-tight">Ann Yoga</a>
    
    <div class="hidden md:flex space-x-12">
      <a 
        href={resolve('/')} 
        class="{baseLinkClasses} {isActive('/') ? activeLinkClasses : inactiveLinkClasses}"
      >
        Home
      </a>
      <a 
        href={resolve('/about')} 
        class="{baseLinkClasses} {isActive('/about') ? activeLinkClasses : inactiveLinkClasses}"
      >
        About
      </a>
      <a 
        href={resolve('/contact')} 
        class="{baseLinkClasses} {isActive('/contact') ? activeLinkClasses : inactiveLinkClasses}"
      >
        Contact
      </a>
    </div>
    
    <a 
      href={resolve('/contact')} 
      class="bg-primary text-on-primary px-8 py-3 rounded-lg font-medium tracking-wide scale-95 active:scale-90 transition-transform shadow-sm hover:shadow-md bg-gradient-to-br from-primary to-primary-container"
    >
      Book Now
    </a>
  </div>
</nav>
