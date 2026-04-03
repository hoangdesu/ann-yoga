<!-- HomePage -->

<script lang="ts">
  import Button from "$lib/components/Button.svelte";
</script>

<svelte:head>
  <title>Tactile Sanctuary | Find Your Balance</title>
</svelte:head>

<section
  class="relative min-h-[921px] flex items-center px-8 overflow-hidden pt-20"
>
  <div
    class="max-w-7xl mx-auto w-full grid grid-cols-1 lg:grid-cols-12 gap-12 items-center"
  >
    <div class="lg:col-span-5 z-10">
      <span
        class="font-manrope text-xs tracking-[0.2em] uppercase text-primary font-bold mb-4 block"
        >Est. 2024 • Organic Wellness</span
      >
      <h1
        class="font-notoserif text-6xl md:text-7xl lg:text-8xl leading-[1.1] text-on-surface mb-8 tracking-tighter"
      >
        Find Your <br /><span class="italic text-primary">Balance</span>
      </h1>
      <p
        class="font-manrope text-lg text-on-surface-variant max-w-md mb-10 leading-relaxed"
      >
        A boutique sanctuary designed to ground your practice in nature’s
        rhythm. Experience intentional movement in a space crafted for silence
        and soul.
      </p>
      <div class="flex flex-col sm:flex-row gap-4">
        <!-- Using explicit button to maintain exact reference padding/size -->
        <button
          class="bg-primary text-on-primary px-10 py-5 cursor-pointer rounded-lg font-semibold text-lg hover:shadow-xl transition-all bg-gradient-to-br from-primary to-primary-container"
        >
          Book a Class
        </button>
        <button
          class="flex items-center gap-3 px-8 py-5 text-on-surface font-semibold cursor-pointer hover:translate-x-1 transition-transform"
        >
          View Schedule
          <span class="material-symbols-outlined">arrow_forward</span>
        </button>
      </div>
    </div>

    <div class="lg:col-span-7 relative flex justify-center lg:justify-end">
      <div
        class="w-11/12 lg:w-10/12 aspect-[4/5] rounded-[2rem] overflow-hidden shadow-2xl transform lg:rotate-2 lg:translate-x-12 scale-95 lg:scale-90"
      >
        <img
          alt="Yoga in nature"
          class="w-full h-full object-cover"
          src="/images/hero.jpg"
        />
      </div>
      <!-- Decorative Element -->
      <div
        class="absolute -bottom-10 -left-10 w-64 h-64 bg-secondary-container rounded-full mix-blend-multiply filter blur-3xl opacity-30 animate-pulse"
      ></div>
    </div>
  </div>
</section>

<!-- Featured Classes (Bento Style Cards) -->
<section class="py-32 px-8 bg-surface-container-low">
  <div class="max-w-7xl mx-auto">
    <div class="flex flex-col md:flex-row md:items-end justify-between mb-20">
      <div class="max-w-xl">
        <h2 class="font-notoserif text-4xl md:text-5xl mb-6 text-on-surface">
          Curated Movement
        </h2>
        <p class="font-manrope text-lg text-on-surface-variant">
          Whether you seek a rigorous flow or a deep stillness, our classes are
          tailored to ground your energy and elevate your spirit.
        </p>
      </div>
      <a
        class="mt-8 md:mt-0 inline-flex items-center gap-2 text-primary font-bold hover:underline decoration-2 underline-offset-8"
        href="#"
      >
        View all styles <span class="material-symbols-outlined">north_east</span
        >
      </a>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
      <!-- Vinyasa Card -->
      <div
        class="group bg-surface-container-lowest rounded-xl overflow-hidden shadow-sm hover:shadow-xl transition-all duration-500"
      >
        <div class="aspect-video overflow-hidden">
          <img
            alt="Vinyasa Flow"
            class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700"
            src="https://lh3.googleusercontent.com/aida-public/AB6AXuBqcrZEuCBTXHEvqCroVpBu63TxyRl8IsY0BW87kvDXwqDokFRpA9Jk0uFlauWxjR12sn4A1qEKqu3syJ0IdUJfAeWOg7xNwY30NxubyTAfCt2GKenFZI8gp2qxPx5zh6aCpd0oGJuW7pTz2MZbuu7Dhe7zdynvBcNWW3xWDPV08NX2EuvNAadzD4Mt6QcbBh0EX2T0SBnQrWwVpLNzM_sV2IX4DRrqPNz-hkhXtvquvOMLRAhn6JPmdX7Rtr-XsWejDHFPFCBfY4I"
          />
        </div>
        <div class="p-8">
          <h3 class="font-notoserif text-2xl mb-3 text-on-surface">
            Vinyasa Flow
          </h3>
          <p class="font-manrope text-on-surface-variant mb-6 leading-relaxed">
            A rhythmic, breath-led sequence designed to build heat and fluid
            mobility throughout the body.
          </p>
          <span
            class="text-sm font-bold tracking-widest text-secondary uppercase"
            >Level: Intermediate</span
          >
        </div>
      </div>

      <!-- Hatha Card -->
      <div
        class="group bg-surface-container-lowest rounded-xl overflow-hidden shadow-sm hover:shadow-xl transition-all duration-500"
      >
        <div class="aspect-video overflow-hidden">
          <img
            alt="Hatha Yoga"
            class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700"
            src="https://lh3.googleusercontent.com/aida-public/AB6AXuBAXsnzC5a_dHGTtetzX6GSqgCIlmsCuCqBpb4OKZG8ZANoj4_ObHAWY45UmmGW6AdMiBwEqfH6k2mdEed50ZiVKYSzVyzyxxDg9xo4KbcaXZ0qmAAKSgB4koBEoBjgBRWFg6WIoAfu4fqyzUc8NwZtnW5EWbVHgNTS-mAITXXxcNsj4MnviV-nBv5ZchaJ9jmPv_3s5wWWZQiDJb1tFrKoG8rTAqLMTVRsCw_UiewwGpD3oaingoT3W9jwEMT1fnooG38PKQD_6Bs"
          />
        </div>
        <div class="p-8">
          <h3 class="font-notoserif text-2xl mb-3 text-on-surface">
            Hatha Yoga
          </h3>
          <p class="font-manrope text-on-surface-variant mb-6 leading-relaxed">
            Focus on foundational alignment and mindful breathing to bring
            balance to the mind and body.
          </p>
          <span
            class="text-sm font-bold tracking-widest text-secondary uppercase"
            >Level: All Levels</span
          >
        </div>
      </div>

      <!-- Restorative Card -->
      <div
        class="group bg-surface-container-lowest rounded-xl overflow-hidden shadow-sm hover:shadow-xl transition-all duration-500"
      >
        <div class="aspect-video overflow-hidden">
          <img
            alt="Restorative Yoga"
            class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700"
            src="https://lh3.googleusercontent.com/aida-public/AB6AXuAGoH5rH2TyTbcxf3f67pcfB_I-TrIFrp21cCROU10WteWFjhVHe6RJ3vtWYqdDEi0b6l_BTGSkbdfY_RPCC0De2T0RB7qVqDsdW3mBADkuKwucqlT3S2TUxidEyUctUmfmRvB4iozrOJLbUDvCvR9B0FS4wZ_JM7BjBEjVq819lOFxf5CmRC2DQoL1oue82MOvfQxj_tt_OiFk6hLI3Si8YUX0KBVoZiebtTKOPei6dXkOOfBxCaVcrFbdqF-QTUP4MGdljLaAp6w"
          />
        </div>
        <div class="p-8">
          <h3 class="font-notoserif text-2xl mb-3 text-on-surface">
            Restorative
          </h3>
          <p class="font-manrope text-on-surface-variant mb-6 leading-relaxed">
            Deeply healing practice using props to support long-held poses,
            inviting profound nervous system release.
          </p>
          <span
            class="text-sm font-bold tracking-widest text-secondary uppercase"
            >Level: Gentle</span
          >
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Why Choose Us - Asymmetric Layout -->
<section class="py-40 px-8">
  <div
    class="max-w-7xl mx-auto grid grid-cols-1 lg:grid-cols-2 gap-24 items-center"
  >
    <div class="relative order-2 lg:order-1">
      <div
        class="w-full h-[600px] bg-surface-variant rounded-full overflow-hidden relative"
      >
        <img
          alt="Instructor guiding student"
          class="w-full h-full object-cover mix-blend-multiply grayscale hover:grayscale-0 transition-all duration-700"
          src="https://lh3.googleusercontent.com/aida-public/AB6AXuBojqFp4FHzbyUtl28qoI4QL2TCB3JBvjPWNE--Bfkheka3tcmJ-FYdg-g1Klapyf85QO_xscJpDlLBt0bzYysX_nfJwr47S1pD55Vxjarkiqka-POHVoN5zttNfjhAqaE9vHydMlICoYNMD67nsUdjPloMNlyfwvpKQ77ItSQfwxgwiv5YyaIh2cWRxzSgxUfmcITrCBcyeRSkWHK_6Lc1wdQPd1j7saIgdaTunciGrW_OKHPhHNuDObkhyySzcLwH1srnJXGqO4o"
        />
      </div>
      <div
        class="absolute -top-12 -right-12 p-8 bg-tertiary-fixed rounded-2xl shadow-xl max-w-xs transform rotate-3"
      >
        <p
          class="font-notoserif italic text-on-tertiary-fixed text-lg leading-relaxed"
        >
          "The space feels like a second home. The intentionality in every
          detail is truly healing."
        </p>
        <p
          class="mt-4 font-manrope font-bold text-sm uppercase tracking-widest text-tertiary"
        >
          Sarah J., Member
        </p>
      </div>
    </div>

    <div class="order-1 lg:order-2">
      <h2
        class="font-notoserif text-4xl md:text-5xl mb-12 text-on-surface leading-tight"
      >
        Beyond the Mat, <br />A Sacred Community
      </h2>
      <div class="space-y-12">
        <div class="flex gap-6">
          <div
            class="flex-shrink-0 w-12 h-12 bg-primary-container rounded-full flex items-center justify-center"
          >
            <span
              class="material-symbols-outlined text-on-primary-container"
              style="font-variation-settings: 'FILL' 1;">spa</span
            >
          </div>
          <div>
            <h4 class="font-manrope font-bold text-xl mb-2">
              Sustainable Philosophy
            </h4>
            <p class="font-manrope text-on-surface-variant leading-relaxed">
              We utilize eco-friendly materials and carbon-neutral studio
              operations to ensure our practice honors the earth as much as our
              bodies.
            </p>
          </div>
        </div>

        <div class="flex gap-6">
          <div
            class="flex-shrink-0 w-12 h-12 bg-secondary-container rounded-full flex items-center justify-center"
          >
            <span
              class="material-symbols-outlined text-on-secondary-container"
              style="font-variation-settings: 'FILL' 1;">groups</span
            >
          </div>
          <div>
            <h4 class="font-manrope font-bold text-xl mb-2">
              Small Group Focus
            </h4>
            <p class="font-manrope text-on-surface-variant leading-relaxed">
              Intimate class sizes ensure personalized guidance and hands-on
              adjustments from our world-class instructors.
            </p>
          </div>
        </div>

        <div class="flex gap-6">
          <div
            class="flex-shrink-0 w-12 h-12 bg-surface-container-highest rounded-full flex items-center justify-center"
          >
            <span
              class="material-symbols-outlined text-on-surface-variant"
              style="font-variation-settings: 'FILL' 1;">verified_user</span
            >
          </div>
          <div>
            <h4 class="font-manrope font-bold text-xl mb-2">Expert Pedagogy</h4>
            <p class="font-manrope text-on-surface-variant leading-relaxed">
              Our teachers are lifelong students with over 500+ hours of
              advanced certification in diverse lineages.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Newsletter CTA / Glassmorphism -->
<section class="py-24 px-8">
  <div
    class="max-w-5xl mx-auto rounded-[3rem] bg-stone-900 overflow-hidden relative p-12 md:p-24 text-center"
  >
    <div class="absolute inset-0 opacity-20">
      <img
        alt="Texture background"
        class="w-full h-full object-cover"
        src="https://lh3.googleusercontent.com/aida-public/AB6AXuBobp6NdYKVBxMqDgytS5bfnveLHDxWyPkiaiKjhB1Tiilt0ZW86Nckgzf5HNghgMygLyWLTyZYHoYKsxppWp6ellOGFK7Ye9wBOsUS-tJBbW2GR1lSnMQdyHasHXLP0WriNCorVUwBUr-Qe8m6FoVco2wftWvlwDjf7RAeBCxpXwbB7efAhGed_GYvSzR_LYscnKidHtEi5rFBj9leQfp7U_9eXgRBjkE8bPw3UhCkl3MzFYsuIVNauIjWhtJAJbHWkN2h0_14yO4"
      />
    </div>
    <div class="relative z-10">
      <h2 class="font-notoserif text-4xl md:text-5xl text-white mb-6">
        Begin Your Journey
      </h2>
      <p class="text-stone-300 font-manrope text-lg mb-12 max-w-xl mx-auto">
        Join our community newsletter for mindful insights, studio updates, and
        15% off your first class pack.
      </p>
      <form class="flex flex-col sm:flex-row gap-4 max-w-lg mx-auto">
        <input
          class="flex-grow bg-white/10 border-none rounded-lg px-6 py-4 text-white placeholder:text-stone-500 focus:ring-2 focus:ring-primary-container outline-none transition-all"
          placeholder="Your email address"
          type="email"
        />
        <button
          class="bg-primary-container text-on-primary-container px-8 py-4 rounded-lg font-bold hover:bg-inverse-primary transition-colors"
          >Subscribe</button
        >
      </form>
    </div>
  </div>
</section>
