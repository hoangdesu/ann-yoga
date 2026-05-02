<script lang="ts">
  import Button from "$lib/components/Button.svelte";

  const address = "11 Mountain Laurel Lane, Ellijay, GA, 30536";
  const mapsLink = `https://www.google.com/maps/search/?api=1&query=${encodeURIComponent(address)}`;
  const mapsEmbed = `https://www.google.com/maps?q=${encodeURIComponent(address)}&output=embed`;

  function handleSubmit(event: SubmitEvent) {
    event.preventDefault();
    alert(
      "Thanks for reaching out! Since this is a static demo, your message wasn't actually sent.",
    );
  }
</script>

<svelte:head>
  <title>Contact Ann Scarab Yoga</title>
</svelte:head>

<div class="max-w-5xl mx-auto px-8 py-32 mt-20 flex justify-center">
  <div
    class="bg-surface-container-lowest rounded-3xl shadow-xl overflow-hidden w-full transition-all duration-500"
  >
    <div class="bg-surface-container-low p-8 md:p-16">
      <h1
        class="text-4xl md:text-5xl mb-6 font-notoserif text-on-surface tracking-tight"
      >
        Let's Connect
      </h1>
      <p
        class="font-manrope text-on-surface-variant mb-12 text-lg leading-relaxed"
      >
        Whether you're looking to start your practice or deepen an existing one,
        I'm here to guide you.
      </p>

      <div class="flex flex-col sm:flex-row gap-4 mb-12">
        <a
          class="inline-flex flex-1 items-center justify-center rounded-lg px-8 py-4 font-manrope font-bold bg-primary-container text-on-primary-container hover:bg-inverse-primary transition-colors"
          href="mailto:annscarab@gmail.com"
        >
          Email annscarab@gmail.com
        </a>
        <a
          class="inline-flex flex-1 items-center justify-center rounded-lg px-8 py-4 font-manrope font-bold bg-surface-variant text-on-surface hover:bg-surface-container-high transition-colors"
          href="tel:+14705649727"
        >
          Call +1 (470) 564-9727
        </a>
      </div>

      <div>
        <p
          class="font-manrope text-sm font-bold uppercase tracking-widest text-primary mb-3"
        >
          Teaching methods
        </p>
        <p class="font-manrope text-on-surface mb-10 leading-loose">
          Online or offline<br />1-on-1 coaching
        </p>

        <p
          class="font-manrope text-sm font-bold uppercase tracking-widest text-primary mb-3"
        >
          Email
        </p>
        <p class="font-manrope text-on-surface mb-10">annscarab@gmail.com</p>

        <p
          class="font-manrope text-sm font-bold uppercase tracking-widest text-primary mb-3"
        >
          Phone
        </p>
        <p class="font-manrope text-on-surface mb-10">+1 (470) 564-9727</p>

        <p
          class="font-manrope text-sm font-bold uppercase tracking-widest text-primary mb-3"
        >
          Address
        </p>
        <a
          class="font-manrope text-on-surface leading-loose hover:text-primary transition-colors hover:underline underline-offset-4 inline-block mb-6"
          href={mapsLink}
          target="_blank"
          rel="noreferrer"
        >
          11 Mountain Laurel Lane<br />Ellijay, GA, 30536
        </a>

        <div class="w-full overflow-hidden rounded-2xl shadow-sm border border-surface-variant/60 bg-surface-variant">
          <div class="relative w-full aspect-[4/3]">
            <iframe
              class="absolute inset-0 w-full h-full"
              src={mapsEmbed}
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
              title="Map — 11 Mountain Laurel Lane, Ellijay, GA, 30536"
            ></iframe>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
