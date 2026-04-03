<script lang="ts">
  import Button from '$lib/components/Button.svelte';
  
  function handleSubmit(event: SubmitEvent) {
    event.preventDefault();
    alert('Thanks for reaching out! Since this is a static demo, your message wasn\'t actually sent.');
  }
</script>

<svelte:head>
  <title>Contact Ann - The Tactile Sanctuary</title>
</svelte:head>

<div class="max-w-5xl mx-auto px-8 py-32 mt-20 flex justify-center">
  <div class="bg-surface-container-lowest rounded-3xl shadow-xl flex flex-col md:flex-row overflow-hidden w-full transition-all duration-500">
    <div class="flex-1 bg-surface-container-low p-8 md:p-16">
      <h1 class="text-4xl md:text-5xl mb-6 font-notoserif text-on-surface tracking-tight">Let's Connect</h1>
      <p class="font-manrope text-on-surface-variant mb-12 text-lg leading-relaxed">Whether you're looking to start your practice or deepen an existing one, I'm here to guide you.</p>
      
      <div>
        <p class="font-manrope text-sm font-bold uppercase tracking-widest text-primary mb-3">Email</p>
        <p class="font-manrope text-on-surface mb-10"><a href="mailto:hello@annyoga.co" class="text-on-surface hover:text-primary transition-colors hover:underline underline-offset-4">hello@annyoga.co</a></p>
        
        <p class="font-manrope text-sm font-bold uppercase tracking-widest text-primary mb-3">Location</p>
        <p class="font-manrope text-on-surface leading-loose">Serving the Greater Area<br/>Available for In-Home & Virtual Sessions</p>
      </div>
    </div>
    
    <form 
      class="flex-1 p-8 md:p-16 flex flex-col gap-6" 
      onsubmit={handleSubmit}
    >
      <div class="flex flex-col gap-3">
        <label for="name" class="font-manrope text-sm font-bold text-on-surface-variant">Name</label>
        <input type="text" id="name" required placeholder="Your full name" class="bg-surface-variant border-none rounded-lg focus:ring-2 focus:ring-primary-container focus:bg-surface-container-low p-4 font-manrope text-base text-on-surface transition-all placeholder:text-stone-500" />
      </div>
      
      <div class="flex flex-col gap-3">
        <label for="email" class="font-manrope text-sm font-bold text-on-surface-variant">Email</label>
        <input type="email" id="email" required placeholder="your.email@example.com" class="bg-surface-variant border-none rounded-lg focus:ring-2 focus:ring-primary-container focus:bg-surface-container-low p-4 font-manrope text-base text-on-surface transition-all placeholder:text-stone-500"  />
      </div>

      <div class="flex flex-col gap-3">
        <label for="message" class="font-manrope text-sm font-bold text-on-surface-variant">Message</label>
        <textarea id="message" rows="5" required placeholder="How can I help you on your journey?" class="bg-surface-variant border-none rounded-lg focus:ring-2 focus:ring-primary-container focus:bg-surface-container-low p-4 font-manrope text-base text-on-surface transition-all placeholder:text-stone-500"></textarea>
      </div>

      <div class="mt-4">
        <Button text="Send Message" variant="primary" />
      </div>
    </form>
  </div>
</div>
