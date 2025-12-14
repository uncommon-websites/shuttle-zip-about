<script>
  export let className = "";
</script>

<div class="bg-white rounded-3xl shadow-sm border border-gray-100 overflow-hidden relative {className}">
  <!-- Top Bar -->
  <div class="h-14 border-b border-gray-100 flex items-center justify-between px-4">
    <!-- Left: Breadcrumbs -->
    <div class="flex items-center gap-2">
      <button class="flex items-center gap-1.5 px-2 py-1 hover:bg-gray-50 rounded-md transition-colors">
        <div class="w-5 h-5 bg-black rounded-full flex items-center justify-center text-white">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" class="w-2.5 h-2.5">
            <path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z" />
          </svg>
        </div>
        <span class="text-[13px] font-medium text-gray-900">Palet</span>
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-3 h-3 text-gray-400">
          <path d="M6 9l6 6 6-6" />
        </svg>
      </button>

      <button class="flex items-center gap-1.5 px-2 py-1 hover:bg-gray-50 rounded-md transition-colors">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-4 h-4 text-gray-500">
          <path d="M22 19a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h5l2 3h9a2 2 0 0 1 2 2z" />
        </svg>
        <span class="text-[13px] font-medium text-gray-900">Untitled</span>
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-3 h-3 text-gray-400">
          <path d="M6 9l6 6 6-6" />
        </svg>
      </button>
    </div>

    <!-- Right: Actions -->
    <div class="flex items-center gap-3">
      <button class="flex items-center gap-1.5 px-3 py-1.5 hover:bg-gray-50 rounded-md transition-colors text-gray-600">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-3.5 h-3.5">
          <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4" />
          <polyline points="7 10 12 15 17 10" />
          <line x1="12" y1="15" x2="12" y2="3" />
        </svg>
        <span class="text-[12px] font-medium">Download</span>
      </button>
      
      <button class="bg-blue-600 hover:bg-blue-700 text-white px-3 py-1.5 rounded-md flex items-center gap-1.5 transition-colors shadow-sm shadow-blue-200">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-3.5 h-3.5">
          <line x1="22" y1="2" x2="11" y2="13" />
          <polygon points="22 2 15 22 11 13 2 9 22 2" />
        </svg>
        <span class="text-[12px] font-medium">Share</span>
      </button>
    </div>
  </div>

  <!-- Content Slot -->
  <div class="relative min-h-[400px] bg-white">
    <slot />
  </div>

  <!-- Bottom Left Zoom Control -->
  <div class="absolute bottom-4 left-4 bg-white border border-gray-100 rounded-full shadow-sm flex items-center px-1 py-1">
    <button aria-label="Zoom out" class="w-6 h-6 flex items-center justify-center text-gray-400 hover:text-gray-600 rounded-full hover:bg-gray-50">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-3 h-3">
        <line x1="5" y1="12" x2="19" y2="12" />
      </svg>
    </button>
    <span class="text-[11px] font-medium text-gray-600 w-10 text-center">100%</span>
    <button aria-label="Zoom in" class="w-6 h-6 flex items-center justify-center text-gray-400 hover:text-gray-600 rounded-full hover:bg-gray-50">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-3 h-3">
        <line x1="12" y1="5" x2="12" y2="19" />
        <line x1="5" y1="12" x2="19" y2="12" />
      </svg>
    </button>
  </div>
</div>
