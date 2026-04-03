<script lang="ts">
  import { resolve } from '$app/paths';
  import { page } from '$app/stores';

  let isMobileMenuOpen = $state(false);

  // Helper function to check if a link is active.
  function isActive(path: string) {
    const currentPath = $page.url.pathname;
    const resolvedPath = resolve(path as any);
    if (path === '/') return currentPath === resolvedPath;
    return currentPath.startsWith(resolvedPath) && resolvedPath !== '/';
  }

  const toggleMenu = () => {
    isMobileMenuOpen = !isMobileMenuOpen;
  };

  const baseLinkClasses = "transition-colors duration-300 font-notoserif text-lg tracking-tight pb-1 border-b-2";
  const activeLinkClasses = "text-olive-900 border-primary font-semibold";
  const inactiveLinkClasses = "text-stone-600 border-transparent font-medium hover:text-primary";
</script>

<!-- ============ Navbar Bar ============ -->
<nav class="fixed top-0 w-full z-50 bg-[#fafaf5]/80 backdrop-blur-md shadow-[0_10px_40px_-15px_rgba(26,28,25,0.04)]">
  <div class="flex justify-between items-center h-20 px-8 max-w-7xl mx-auto">
    <a href={resolve('/')} class="font-notoserif text-2xl font-bold text-olive-900 tracking-tight">Ann Yoga</a>

    <!-- Desktop Links -->
    <div class="hidden md:flex space-x-12">
      <a href={resolve('/')} class="{baseLinkClasses} {isActive('/') ? activeLinkClasses : inactiveLinkClasses}">Home</a>
      <a href={resolve('/about')} class="{baseLinkClasses} {isActive('/about') ? activeLinkClasses : inactiveLinkClasses}">About</a>
      <a href={resolve('/contact')} class="{baseLinkClasses} {isActive('/contact') ? activeLinkClasses : inactiveLinkClasses}">Contact</a>
    </div>

    <!-- Right: Book Now + Hamburger -->
    <div class="flex items-center gap-3">
      <a
        href={resolve('/contact')}
        class="hidden sm:block bg-primary text-on-primary px-6 py-3 rounded-lg font-medium tracking-wide transition-transform scale-95 active:scale-90 shadow-sm hover:shadow-md bg-gradient-to-br from-primary to-primary-container"
      >
        Book Now
      </a>

      <button
        onclick={toggleMenu}
        class="md:hidden flex items-center justify-center w-10 h-10 text-olive-900 focus:outline-none"
        aria-label={isMobileMenuOpen ? 'Close menu' : 'Open menu'}
      >
        <span class="material-symbols-outlined text-[2rem]">
          {isMobileMenuOpen ? 'close' : 'menu'}
        </span>
      </button>
    </div>
  </div>
</nav>

<!-- ============ Mobile Overlay — OUTSIDE nav to avoid backdrop-filter stacking context ============ -->
{#if isMobileMenuOpen}
  <div
    class="mobile-menu fixed left-0 right-0 z-40"
    style="top: 5rem;"
  >
    <nav class="flex flex-col gap-2 p-8">
      <a
        href={resolve('/')}
        onclick={() => isMobileMenuOpen = false}
        class="mobile-link {isActive('/') ? 'active' : ''}"
      >
        Home
      </a>
      <a
        href={resolve('/about')}
        onclick={() => isMobileMenuOpen = false}
        class="mobile-link {isActive('/about') ? 'active' : ''}"
      >
        About
      </a>
      <a
        href={resolve('/contact')}
        onclick={() => isMobileMenuOpen = false}
        class="mobile-link {isActive('/contact') ? 'active' : ''}"
      >
        Contact
      </a>
      <div class="mt-auto pt-8">
        <a
          href={resolve('/contact')}
          onclick={() => isMobileMenuOpen = false}
          class="block w-full text-center bg-gradient-to-br from-primary to-primary-container text-on-primary px-8 py-5 rounded-xl font-bold text-xl shadow-lg"
        >
          Book Now
        </a>
      </div>
    </nav>
  </div>
{/if}

<style>
  .mobile-menu {
    background-color: #fafaf5;
    border-top: 1px solid #e7e5e4;
    animation: slideDown 0.25s ease-out;
  }

  .mobile-link {
    display: block;
    font-family: 'Noto Serif', serif;
    font-size: 2rem;
    line-height: 1.2;
    padding: 0.75rem 0;
    color: #57534e; /* stone-600 */
    border-bottom: 1px solid #e7e5e4;
    transition: color 0.2s;
  }

  .mobile-link.active {
    color: var(--color-primary);
    font-weight: 600;
  }

  .mobile-link:not(.active):hover {
    color: var(--color-primary);
  }

  @keyframes slideDown {
    from { opacity: 0; transform: translateY(-8px); }
    to   { opacity: 1; transform: translateY(0); }
  }
</style>
