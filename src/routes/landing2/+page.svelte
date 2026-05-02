<script lang="ts">
  import Button from '$lib/components/Button.svelte';
</script>

<svelte:head>
  <title>Ann Scarab Yoga - The Tactile Sanctuary</title>
</svelte:head>

<section class="relative overflow-hidden pt-32 pb-20">
  <div class="max-w-7xl mx-auto w-full grid grid-cols-1 lg:grid-cols-12 gap-12 items-center px-8 min-h-[75vh]">
    <div class="lg:col-span-5 z-10 lg:pr-8">
      <h1 class="mb-8 font-notoserif text-6xl md:text-7xl leading-[1.1] text-on-surface tracking-tighter">Find your grounding.<br/>Breathe into space.</h1>
      <p class="font-manrope text-lg text-on-surface-variant max-w-md mb-10 leading-relaxed">Experience personalized wellness with Ann. A mindful approach to movement, designed to restore balance to your body and mind.</p>
      <div class="flex flex-col sm:flex-row gap-4">
        <button class="bg-primary text-on-primary px-10 py-5 rounded-lg font-semibold text-lg hover:shadow-xl transition-all bg-gradient-to-br from-primary to-primary-container">
          Work With Me
        </button>
        <button class="flex items-center justify-center gap-3 px-8 py-5 text-primary font-semibold border-2 border-primary/20 rounded-lg hover:bg-primary/5 transition-colors">
          My Philosophy
        </button>
      </div>
    </div>
    
    <div class="lg:col-span-7 relative h-full min-h-[400px] lg:min-h-full w-full">
      <div class="absolute inset-0 lg:-right-[10vw] lg:w-[150%] rounded-3xl overflow-hidden shadow-2xl z-[1] transform lg:translate-x-12">
        <img src="https://images.unsplash.com/photo-1544367567-0f2fcb009e0b?q=80&w=1200&auto=format&fit=crop" alt="Yoga in natural light" class="w-full h-full object-cover" />
      </div>
    </div>
  </div>
</section>

<section class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 items-center py-32 px-8 gap-0 md:gap-12">
  <div class="flex-1 bg-surface-container-lowest p-8 md:p-16 rounded-3xl shadow-xl z-[2] lg:translate-x-16 -mb-12 md:mb-0 transform hover:-translate-y-2 transition-transform duration-500">
    <h2 class="font-notoserif text-4xl md:text-[2.5rem] mb-6 text-on-surface tracking-tight leading-tight">A tactile sanctuary, tailored for you.</h2>
    <p class="font-manrope text-on-surface-variant text-lg leading-relaxed">Every body is unique, and so is every practice. As a solo instructor, I focus on the subtle shifts—the micro-adjustments that transform a routine into a sanctuary. My sessions are designed to pull you out of the digital noise and root you back into the physical world.</p>
  </div>
  <div class="flex-1 h-[500px] md:h-[600px] rounded-3xl overflow-hidden w-full z-[1]">
    <img src="https://images.unsplash.com/photo-1599901860904-1776dfcab30b?q=80&w=800&auto=format&fit=crop" alt="Yoga mat and soft light" class="w-full h-full object-cover" />
  </div>
</section>
