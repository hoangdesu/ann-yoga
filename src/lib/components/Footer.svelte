<script lang="ts">
  import { resolve } from '$app/paths';
</script>

<footer class="w-full mt-20 bg-stone-100">
  <div class="grid grid-cols-1 md:grid-cols-3 gap-12 py-16 px-8 max-w-7xl mx-auto border-t border-stone-200/30">
    <div>
      <div class="font-notoserif text-xl font-semibold text-stone-900 mb-6">Ann Yoga</div>
      <p class="font-manrope text-sm leading-relaxed text-stone-600 mb-8 max-w-xs">
        Rooted in tradition, reaching for the light. Our studio is a space for modern practitioners to find ancient peace.
      </p>
      <div class="flex gap-4">
        <a class="text-stone-500 hover:text-primary transition-colors" href="#">Instagram</a>
        <a class="text-stone-500 hover:text-primary transition-colors" href="#">YouTube</a>
      </div>
    </div>
    <div>
      <h5 class="font-bold text-stone-900 mb-6 font-manrope text-sm uppercase tracking-widest">Navigation</h5>
      <ul class="space-y-4 font-manrope text-sm text-stone-500">
        <li><a class="hover:text-primary transition-all" href={resolve('/')}>Home</a></li>
        <li><a class="hover:text-primary transition-all" href={resolve('/about')}>About Ann</a></li>
        <li><a class="hover:text-primary transition-all" href={resolve('/contact')}>Contact Us</a></li>
      </ul>
    </div>
    <div>
      <h5 class="font-bold text-stone-900 mb-6 font-manrope text-sm uppercase tracking-widest">Visit Us</h5>
      <p class="font-manrope text-sm text-stone-500 mb-4">122 Sage Creek Blvd<br/>Portland, OR 97201</p>
      <p class="font-manrope text-sm text-stone-500">hello@annyoga.co<br/>+1 (503) 555-0192</p>
    </div>
  </div>
  <div class="max-w-7xl mx-auto px-8 pb-12">
    <div class="flex flex-col md:flex-row justify-between items-center pt-8 border-t border-stone-200/30 font-manrope text-xs text-stone-500 tracking-wide">
      <p>© 2024 Tactile Sanctuary Yoga Studio. All rights reserved.</p>
      <div class="flex gap-8 mt-4 md:mt-0">
        <a class="hover:underline" href="#">Privacy Policy</a>
        <a class="hover:underline" href="#">Terms of Service</a>
        <a class="hover:underline" href={resolve('/contact')}>Contact Us</a>
      </div>
    </div>
  </div>
</footer>
