<script>
  import { ArrowRight } from 'lucide-svelte';
</script>

<footer class="py-32 px-4 flex flex-col items-center text-center">
  <div class="w-12 h-12 bg-blue-600 rounded-xl flex items-center justify-center text-white mb-8 shadow-lg shadow-blue-200 rotate-[-6deg]">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" class="w-6 h-6">
      <path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z" />
    </svg>
  </div>
  
  <h2 class="text-4xl md:text-5xl font-bold tracking-tight text-gray-900 mb-10 max-w-xl leading-tight">
    The smarter and<br/>
    simpler way to share.
  </h2>
  
  <a href="/signup" class="bg-blue-600 hover:bg-blue-700 text-white text-sm font-medium px-6 py-3 rounded-full flex items-center gap-2 transition-colors shadow-md shadow-blue-200 mb-16">
    Create account
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" class="w-3.5 h-3.5">
       <line x1="5" y1="12" x2="19" y2="12"></line>
       <polyline points="12 5 19 12 12 19"></polyline>
    </svg>
  </a>
  
  <div class="flex flex-col items-center gap-6 w-full">
    <div class="flex items-center gap-6 text-sm text-gray-500 font-medium">
      <a href="/" class="hover:text-gray-900 transition-colors">Instagram</a>
      <div class="w-1 h-1 bg-gray-300 rounded-full"></div>
      <a href="/" class="hover:text-gray-900 transition-colors">LinkedIn</a>
    </div>
    
    <div class="flex items-center gap-6 text-[11px] text-gray-400">
      <a href="/" class="hover:text-gray-600 transition-colors">Terms of service</a>
      <div class="w-1 h-1 bg-gray-300 rounded-full"></div>
      <a href="/" class="hover:text-gray-600 transition-colors">Privacy Policy</a>
    </div>
  </div>
</footer>
