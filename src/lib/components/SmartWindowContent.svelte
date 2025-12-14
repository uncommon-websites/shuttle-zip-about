<script>
  import FileIcon from './FileIcon.svelte';
</script>

<div class="w-full h-full min-h-[500px] bg-gray-50 relative p-8 overflow-hidden">
  <!-- Blurred Background Files -->
  <div class="absolute inset-0 flex items-center justify-center gap-24 opacity-50 blur-sm pointer-events-none">
     <FileIcon type="ai" name="Fashion Week Logo.ai" date="April 5, 2025 08:15" />
     <FileIcon type="folder" name="Paris Fashion Week '25" date="March 22, 2025 16:20" />
     <FileIcon type="ps" name="Shoot '25.psd" date="March 10, 2025 09:45" />
  </div>
  
  <!-- Context Menu -->
  <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[320px] bg-white/90 backdrop-blur-xl rounded-xl shadow-2xl border border-gray-200/50 overflow-hidden z-10">
    <div class="p-1.5 flex flex-col gap-0.5">
      
      <!-- Group 1 -->
      <div class="px-2 py-1.5 text-[10px] font-semibold text-gray-400 uppercase tracking-wider">Suggestions</div>
      <button class="w-full text-left px-2 py-1.5 text-[13px] text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors flex items-center justify-between group">
        Preview
      </button>
      <button class="w-full text-left px-2 py-1.5 text-[13px] text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors">
        Rename...
      </button>
      <button class="w-full text-left px-2 py-1.5 text-[13px] text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors">
        Delete
      </button>
      <button class="w-full text-left px-2 py-1.5 text-[13px] text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors">
        Download
      </button>

      <div class="h-px bg-gray-100 my-1"></div>

      <!-- Group 2 -->
      <div class="px-2 py-1.5 text-[10px] font-semibold text-gray-400 uppercase tracking-wider">Space actions</div>
      <button class="w-full text-left px-2 py-1.5 text-[13px] text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors">
        Download whole Space
      </button>
      <button class="w-full text-left px-2 py-1.5 text-[13px] text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors">
        Rename all files in Space
      </button>
      <button class="w-full text-left px-2 py-1.5 text-[13px] text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors">
        Delete Space
      </button>
    </div>

    <!-- Search Input -->
    <div class="p-2 border-t border-gray-100 bg-gray-50/50">
      <div class="relative">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="absolute left-2.5 top-1/2 -translate-y-1/2 w-3.5 h-3.5 text-gray-400">
          <circle cx="11" cy="11" r="8"></circle>
          <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
        </svg>
        <input type="text" placeholder="Ask Shuttle a question..." class="w-full bg-white border border-gray-200 rounded-lg pl-8 pr-3 py-1.5 text-[12px] placeholder:text-gray-400 focus:outline-none focus:border-blue-500 transition-colors shadow-sm" />
      </div>
    </div>
  </div>
</div>
