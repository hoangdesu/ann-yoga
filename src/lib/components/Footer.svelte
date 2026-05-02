<script lang="ts">
  import { resolve } from '$app/paths';
</script>

<footer class="w-full mt-20 bg-stone-100">
  <div
    class="grid grid-cols-1 md:grid-cols-3 gap-12 py-16 px-8 max-w-7xl mx-auto border-t border-stone-200/30"
  >
    <div>
      <div class="font-notoserif text-xl font-semibold text-stone-900 mb-6">
        Ann Scarab Yoga
      </div>
      <p
        class="font-manrope text-sm leading-relaxed text-stone-600 mb-8 max-w-xs"
      >
        Rooted in tradition, reaching for the light. Our studio is a space for
        modern practitioners to find ancient peace.
      </p>
      <div class="flex gap-4">
        <a class="text-stone-500 hover:text-primary transition-colors" href="/"
          >Instagram</a
        >
        <a class="text-stone-500 hover:text-primary transition-colors" href="/"
          >YouTube</a
        >
      </div>
    </div>
    <div>
      <h5
        class="font-bold text-stone-900 mb-6 font-manrope text-sm uppercase tracking-widest"
      >
        Navigation
      </h5>
      <ul class="space-y-4 font-manrope text-sm text-stone-500">
        <li>
          <a class="hover:text-primary transition-all" href={resolve('/')}
            >Home</a
          >
        </li>
        <li>
          <a class="hover:text-primary transition-all" href={resolve('/about')}
            >About Ann</a
          >
        </li>
        <li>
          <a
            class="hover:text-primary transition-all"
            href={resolve('/contact')}>Contact Us</a
          >
        </li>
      </ul>
    </div>
    <div>
      <h5
        class="font-bold text-stone-900 mb-6 font-manrope text-sm uppercase tracking-widest"
      >
        Contact
      </h5>
      <p class="font-manrope text-sm text-stone-500 mb-4">
        11 Mountain Laurel Lane<br />Ellijay, GA, 30536
      </p>
      <p class="font-manrope text-sm text-stone-500">
        <a
          class="hover:text-primary transition-colors"
          href="mailto:annscarab@gmail.com">annscarab@gmail.com</a
        ><br />
        <a class="hover:text-primary transition-colors" href="tel:+14705649727"
          >+1 (470) 564-9727</a
        >
      </p>
    </div>
  </div>
  <div class="max-w-7xl mx-auto px-8 pb-12">
    <div
      class="flex flex-col md:flex-row justify-between items-center pt-8 border-t border-stone-200/30 font-manrope text-xs text-stone-500 tracking-wide"
    >
      <p>© 2026 Ann Scarab Yoga. All rights reserved.</p>
      <!-- <div class="flex gap-8 mt-4 md:mt-0"> -->
      <div>
        <!-- <a class="hover:underline" href="/">Privacy Policy</a>
        <a class="hover:underline" href="/">Terms of Service</a>
        <a class="hover:underline" href={resolve('/contact')}>Contact Us</a> -->
        Developed by Brian Nguyen
        <span>
          {'('}<a class="hover:underline" href="https://hoangdesu.com" target="_blank" rel="noreferrer">
            hoangdesu.com
          </a>{')'}
        </span> with 🧡
      </div>
    </div>
  </div>
</footer>
