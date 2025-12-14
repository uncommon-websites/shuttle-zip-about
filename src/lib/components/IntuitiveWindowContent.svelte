<script>
  import FileIcon from './FileIcon.svelte';
</script>

<div class="w-full h-full min-h-[500px] bg-gray-50 relative p-8">
  <!-- Background Files -->
  <FileIcon type="ai" name="Fashion Week Logo.ai" date="April 5, 2025 08:15" className="absolute top-1/2 left-16 -translate-y-1/2" />
  <FileIcon type="ps" name="Shoot '25.psd" date="March 10, 2025 09:45" className="absolute top-1/2 right-16 -translate-y-1/2" />

  <!-- Preview Modal -->
  <div class="absolute top-8 left-1/2 -translate-x-1/2 w-[400px] h-[440px] bg-white rounded-xl shadow-2xl border border-gray-200 overflow-hidden flex flex-col z-10">
    <!-- Modal Header -->
    <div class="h-10 border-b border-gray-100 flex items-center justify-between px-3 bg-white">
      <div class="flex items-center gap-2">
        <div class="w-4 h-4 grid grid-cols-2 gap-0.5">
           <div class="bg-gray-400 rounded-[1px]"></div><div class="bg-gray-400 rounded-[1px]"></div>
           <div class="bg-gray-400 rounded-[1px]"></div><div class="bg-gray-400 rounded-[1px]"></div>
        </div>
        <span class="text-[12px] font-medium text-gray-700">Preview</span>
      </div>
      <button aria-label="Close preview" class="text-gray-400 hover:text-gray-600">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="w-4 h-4">
          <line x1="18" y1="6" x2="6" y2="18"></line>
          <line x1="6" y1="6" x2="18" y2="18"></line>
        </svg>
      </button>
    </div>
    
    <!-- Modal Content (Image) -->
    <div class="flex-1 bg-gray-100 relative overflow-hidden">
       <!-- Red Tile Pattern Image -->
       <div class="absolute inset-0 bg-red-500">
          <div class="absolute inset-0 opacity-50" style="background-image: repeating-linear-gradient(45deg, transparent, transparent 5px, rgba(255,255,255,0.2) 5px, rgba(255,255,255,0.2) 10px);"></div>
          <!-- Some shadow/depth to look like a room/wall as in screenshot -->
          <div class="absolute left-0 top-0 bottom-0 w-1/3 bg-gradient-to-r from-black/20 to-transparent"></div>
       </div>
       <!-- Fake UI elements on image if needed? The screenshot shows a wall with tiles and some fixtures. I'll just keep it abstract red tiles. -->
       <!-- Actually, let's try to make it look a bit more like the screenshot: Split view, left side wood/beige, right side red tiles. -->
       <div class="absolute inset-0 flex">
          <div class="w-1/3 bg-[#C4A484] relative">
             <!-- Wood texture simulation -->
             <div class="absolute top-1/4 left-1/2 -translate-x-1/2 w-4 h-4 bg-black/50 rounded-full shadow-lg"></div>
          </div>
          <div class="w-2/3 bg-red-500 relative overflow-hidden">
             <!-- Tiles -->
             <div class="absolute inset-0" style="background-image: linear-gradient(rgba(255,255,255,0.1) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.1) 1px, transparent 1px); background-size: 20px 20px;"></div>
             <!-- Fixtures -->
             <div class="absolute bottom-1/4 left-8 flex gap-4">
                <div class="w-8 h-8 bg-white/90 rounded shadow-md"></div>
                <div class="w-8 h-8 bg-white/90 rounded shadow-md"></div>
             </div>
          </div>
       </div>
    </div>
  </div>
</div>
