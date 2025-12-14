<script>
  import Cursor from './Cursor.svelte';
</script>

<div class="w-full h-full min-h-[500px] bg-gray-50/50 p-8 relative flex items-center justify-center">
  
  <!-- File 1: Red Image -->
  <div class="absolute top-12 left-1/3 -translate-x-1/2 w-32 h-24 bg-white p-1.5 rounded-lg shadow-sm border border-gray-200 rotate-[-6deg] z-10">
    <div class="w-full h-full rounded bg-red-500 overflow-hidden relative">
       <!-- Pattern for red tiles -->
       <div class="absolute inset-0 opacity-50" style="background-image: repeating-linear-gradient(45deg, transparent, transparent 5px, rgba(255,255,255,0.2) 5px, rgba(255,255,255,0.2) 10px);"></div>
       <div class="absolute inset-0 opacity-30" style="background-image: radial-gradient(circle at center, rgba(255,255,255,0.4) 0%, transparent 70%);"></div>
    </div>
  </div>

  <!-- File 2: Video File -->
  <div class="absolute top-16 right-1/3 translate-x-1/2 w-24 h-28 bg-white/90 backdrop-blur rounded-lg shadow-sm border border-gray-200 rotate-[4deg] flex flex-col items-center justify-center gap-2 z-10">
    <div class="w-12 h-12 rounded-lg bg-gradient-to-br from-blue-400 to-cyan-300 flex items-center justify-center shadow-inner">
      <div class="w-6 h-6 bg-black/20 rounded-full flex items-center justify-center backdrop-blur-sm">
        <svg viewBox="0 0 24 24" fill="currentColor" class="w-3 h-3 text-white ml-0.5">
          <polygon points="5 3 19 12 5 21 5 3"></polygon>
        </svg>
      </div>
    </div>
    <span class="text-[10px] font-medium text-gray-500">MP4</span>
  </div>

  <!-- Drag & Drop Zone -->
  <div class="w-[280px] h-[180px] rounded-2xl border-2 border-dashed border-gray-200 bg-white flex flex-col items-center justify-center gap-4 relative z-0">
    <div class="relative w-16 h-16">
      <!-- Icons cluster -->
      <div class="absolute top-0 left-1/2 -translate-x-1/2">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" class="w-8 h-8 text-gray-400">
           <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
           <polyline points="14 2 14 8 20 8"></polyline>
        </svg>
      </div>
      <div class="absolute bottom-0 left-0">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" class="w-6 h-6 text-gray-400 rotate-[-12deg]">
           <rect x="3" y="3" width="18" height="18" rx="2" ry="2"></rect>
           <circle cx="8.5" cy="8.5" r="1.5"></circle>
           <polyline points="21 15 16 10 5 21"></polyline>
        </svg>
      </div>
      <div class="absolute bottom-2 right-0">
         <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" class="w-6 h-6 text-gray-400 rotate-[12deg]">
            <polygon points="5 3 19 12 5 21 5 3"></polygon>
         </svg>
      </div>
    </div>
    <span class="text-sm font-semibold text-gray-900">Drag & Drop</span>
  </div>

  <!-- Cursors -->
  <Cursor name="Giel" color="yellow" className="absolute top-[35%] left-[42%]" />
  <Cursor name="Jean" color="orange" className="absolute top-[35%] right-[40%]" />

</div>
