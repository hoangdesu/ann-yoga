<script lang="ts">
  import { resolve } from "$app/paths";
  import Button from "$lib/components/Button.svelte";

  const contactLink = resolve("/contact" as any);
</script>

<svelte:head>
  <title>About Ann Scarab Yoga</title>
</svelte:head>

<div class="max-w-7xl mx-auto px-8 py-32 mt-20">
  <div class="mb-24 text-center">
    <h1 class="text-5xl font-notoserif text-on-surface tracking-tight mb-4">
      About Ann
    </h1>
    <p
      class="font-manrope text-sm uppercase tracking-widest text-on-surface-variant font-bold"
    >
      The Philosophy
    </p>
  </div>

  <div class="flex flex-col lg:flex-row items-center gap-12 lg:gap-0">
    <div
      class="flex-[5] w-full h-[500px] lg:h-[800px] rounded-3xl overflow-hidden shadow-2xl relative z-[1]"
    >
      <img
        src="https://images.unsplash.com/photo-1544367567-0f2fcb009e0b?q=80&w=800&auto=format&fit=crop"
        alt="Ann instructing yoga"
        class="w-full h-full object-cover"
      />
    </div>

    <div
      class="flex-[7] bg-surface-container-low p-8 md:p-20 rounded-3xl lg:-ml-24 mt-[-6rem] lg:mt-0 relative z-[2] shadow-sm hover:shadow-xl transition-all duration-500"
    >
      <p
        class="text-3xl font-notoserif text-primary mb-8 leading-snug tracking-tighter"
      >
        My journey into yoga wasn't about achieving the perfect pose. It was
        about finding stillness in a loud world.
      </p>

      <p
        class="font-manrope text-on-surface-variant mb-6 text-lg leading-relaxed"
      >
        I believe that movement is medicinal. Through years of personal practice
        and intensive study, I've cultivated an approach that focuses heavily on
        alignment, breath, and profound physiological awareness. I do not run
        large, crowded classroom studios. My focus is singular: you.
      </p>

      <p
        class="font-manrope text-on-surface-variant mb-6 text-lg leading-relaxed"
      >
        By working one-on-one or in very small, intimate settings, I can tailor
        every asana to your body's specific biomechanics. We build a tactile
        sanctuary—a safe space to explore your edges, release tension, and
        reclaim your mind-body connection.
      </p>

      <div class="mt-12">
        <Button
          text="Start Your Journey"
          href={contactLink}
          variant="primary"
        />
      </div>
    </div>
  </div>
</div>
