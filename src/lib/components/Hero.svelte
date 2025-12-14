<script>
  import AppWindow from './AppWindow.svelte';
  import HeroWindowContent from './HeroWindowContent.svelte';
</script>

<section class="pt-32 pb-20 px-4 flex flex-col items-center text-center max-w-7xl mx-auto">
  <div class="mb-16 max-w-2xl mx-auto">
    <h1 class="text-5xl md:text-6xl font-bold tracking-tight text-gray-900 mb-6 leading-[1.1]">
      New simple <br/>
      in file sharing
    </h1>
    <p class="text-lg md:text-xl text-gray-500 mb-4 leading-relaxed">
      With Shuttle your work never gets lost.<br/>
      Built for simplicity and powered by AI.
    </p>
    <p class="text-[11px] text-gray-400 font-medium tracking-wide uppercase">2GB for free</p>
  </div>

  <div class="w-full max-w-5xl mx-auto px-4 md:px-8">
    <AppWindow className="w-full aspect-[16/10]">
      <HeroWindowContent />
    </AppWindow>
  </div>
</section>
