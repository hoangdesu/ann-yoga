<script lang="ts">
  // Svelte 5: Define a formal interface for component props and use the $props() rune.
  interface Props {
    text?: string;
    href?: string;
    variant?: "primary" | "secondary" | "ghost";
  }

  let { 
    text = "", 
    href = "", 
    variant = "primary" 
  } = $props<Props>();

  // Base styles for the button component.
  const baseClasses = "inline-flex items-center justify-center font-manrope rounded-lg transition-all duration-300";

  // Svelte 5: Use $derived for state that changes based on other values.
  const variantClasses = $derived(
    variant === "primary" ? "bg-gradient-to-br from-primary to-primary-container text-on-primary font-semibold tracking-wide shadow-sm hover:shadow-xl active:scale-95" :
    variant === "secondary" ? "bg-secondary-container text-on-secondary-container font-medium" :
    "bg-transparent text-primary hover:bg-primary/5 font-semibold"
  );
    
  const sizeClasses = "px-8 py-4 text-base";
  const cssClass = $derived(`${baseClasses} ${variantClasses} ${sizeClasses}`);
</script>

{#if href}
  <a {href} class={cssClass}>
    {text}
  </a>
{:else}
  <button class={cssClass}>
    {text}
  </button>
{/if}
