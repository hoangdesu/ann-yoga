<script lang="ts">
  // Svelte 5: Directly destructure $props() to ensure reactivity is maintained.
  let { 
    text = "", 
    href = "", 
    variant = "primary" 
  } = $props<{ 
    text?: string;
    href?: string;
    variant?: "primary" | "secondary" | "ghost";
  }>();

  // Base styles for the button component.
  const baseClasses = "inline-flex items-center justify-center font-manrope rounded-lg transition-all duration-300";

  // Reactive classes derived from props.
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
