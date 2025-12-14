<script>
  import FileIcon from './FileIcon.svelte';
  
  const users = [
    { name: 'Giel', email: 'giel@gmail.com', role: 'Full access', avatar: 'bg-yellow-400' },
    { name: 'Jean', email: 'jean@gmail.com', role: 'Read only', avatar: 'bg-orange-400' },
    { name: 'Niels', email: 'niels@shuttle.zip', role: 'Read only', avatar: 'bg-red-500' },
    { name: 'Jeroen', email: 'jeroen@gmail.com', role: 'Full access', avatar: 'bg-green-500' },
  ];
</script>

<div class="w-full h-full min-h-[500px] bg-gray-50 flex relative">
  <!-- Sidebar -->
  <div class="w-60 bg-white border-r border-gray-100 flex flex-col p-4 z-10">
    <div class="flex items-center justify-between mb-4">
      <span class="text-[13px] font-semibold text-gray-900">Storage</span>
      <button class="text-gray-400 hover:text-gray-600">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="w-3.5 h-3.5">
          <line x1="18" y1="6" x2="6" y2="18"></line>
          <line x1="6" y1="6" x2="18" y2="18"></line>
        </svg>
      </button>
    </div>
    
    <div class="space-y-1">
      <button class="w-full flex items-center gap-2 px-2 py-1.5 bg-gray-50 rounded-md text-left">
        <div class="w-4 h-4 bg-blue-600 rounded-[3px] flex items-center justify-center text-white">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" class="w-2.5 h-2.5"><path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z" /></svg>
        </div>
        <div class="flex-1">
          <div class="text-[12px] font-medium text-gray-900">Shuttle</div>
          <div class="text-[10px] text-gray-500">2GB for free</div>
        </div>
        <div class="w-2 h-2 bg-blue-500 rounded-full"></div>
      </button>
      
      <button class="w-full flex items-center gap-2 px-2 py-1.5 hover:bg-gray-50 rounded-md text-left opacity-60">
        <div class="w-4 h-4 bg-red-600 rounded-[3px] flex items-center justify-center text-white font-bold text-[8px]">B</div>
        <div class="flex-1">
          <div class="text-[12px] font-medium text-gray-900">Backblaze</div>
          <div class="text-[10px] text-gray-500">16GB stored</div>
        </div>
      </button>
      
      <button class="w-full flex items-center gap-2 px-2 py-1.5 hover:bg-gray-50 rounded-md text-left opacity-60">
        <div class="w-4 h-4 bg-orange-400 rounded-[3px] flex items-center justify-center text-white font-bold text-[8px]">A</div>
        <div class="flex-1">
          <div class="text-[12px] font-medium text-gray-900">Amazon S3</div>
          <div class="text-[10px] text-gray-500">8GB stored</div>
        </div>
      </button>

       <button class="w-full flex items-center gap-2 px-2 py-1.5 hover:bg-gray-50 rounded-md text-left opacity-60">
        <div class="w-4 h-4 bg-blue-400 rounded-[3px] flex items-center justify-center text-white font-bold text-[8px]">G</div>
        <div class="flex-1">
          <div class="text-[12px] font-medium text-gray-900">Google Cloud</div>
          <div class="text-[10px] text-gray-500">1GB stored</div>
        </div>
      </button>
      
      <button class="w-full flex items-center gap-2 px-2 py-2 mt-2 text-gray-500 hover:text-gray-900">
        <div class="w-4 h-4 border border-gray-300 rounded-[3px] flex items-center justify-center">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="w-2.5 h-2.5"><line x1="12" y1="5" x2="12" y2="19"></line><line x1="5" y1="12" x2="19" y2="12"></line></svg>
        </div>
        <span class="text-[11px] font-medium">Add storage provider</span>
      </button>
    </div>
  </div>

  <!-- Main Content (File Grid) -->
  <div class="flex-1 p-6 grid grid-cols-3 gap-6 content-start">
    <FileIcon type="ai" name="Fashion Week Logo.ai" date="April 5, 2025 08:15" />
    <FileIcon type="folder" name="Paris Fashion Week '25" date="March 22, 2025 16:20" />
    <FileIcon type="ps" name="Shoot '25.psd" date="March 10, 2025 09:45" />
    <FileIcon type="folder" name="IMG_6012.RAW" date="March 14, 2025 07:45" />
    <div class="flex flex-col items-center gap-2">
       <div class="w-16 h-20 rounded-lg bg-white border border-gray-200 flex items-center justify-center shadow-sm relative overflow-hidden">
          <div class="absolute inset-0 bg-gray-100 flex items-center justify-center">
             <svg viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6 text-gray-400"><polygon points="5 3 19 12 5 21 5 3"></polygon></svg>
          </div>
       </div>
       <div class="text-center">
          <p class="text-[10px] font-medium text-gray-700 leading-tight">Spring Ad 2025</p>
          <p class="text-[9px] text-gray-400 mt-0.5">March 30, 2025 14:00</p>
       </div>
    </div>
    <FileIcon type="folder" name="IMG_6094.RAW" date="April 15, 2025 11:30" />
  </div>

  <!-- Share Modal (Overlay) -->
  <div class="absolute top-4 right-4 w-[280px] bg-white rounded-xl shadow-xl border border-gray-200 flex flex-col overflow-hidden z-20">
    <div class="flex items-center justify-between p-3 border-b border-gray-100">
      <div class="flex items-center gap-2">
         <div class="w-4 h-4 grid grid-cols-2 gap-0.5">
           <div class="bg-gray-400 rounded-[0.5px]"></div><div class="bg-gray-400 rounded-[0.5px]"></div>
           <div class="bg-gray-400 rounded-[0.5px]"></div><div class="bg-gray-400 rounded-[0.5px]"></div>
        </div>
        <span class="text-[12px] font-semibold text-gray-900">Share</span>
      </div>
      <button aria-label="Close share" class="text-gray-400 hover:text-gray-600">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="w-3.5 h-3.5">
          <line x1="18" y1="6" x2="6" y2="18"></line>
          <line x1="6" y1="6" x2="18" y2="18"></line>
        </svg>
      </button>
    </div>
    
    <div class="p-3">
      <div class="mb-4">
        <label for="share-input" class="text-[10px] font-medium text-gray-500 mb-1.5 block">Name or Email</label>
        <input id="share-input" type="text" placeholder="John Doe" class="w-full bg-gray-50 border border-gray-200 rounded-md px-2 py-1.5 text-[12px] focus:outline-none focus:border-blue-500" />
      </div>
      
      <div>
        <span class="text-[10px] font-medium text-gray-500 mb-2 block">People with access</span>
        <div class="space-y-3">
          {#each users as user}
            <div class="flex items-center justify-between">
              <div class="flex items-center gap-2">
                <div class="w-6 h-6 rounded-full {user.avatar} flex items-center justify-center text-[10px] font-bold text-white shadow-sm">
                   <!-- Avatar image simulation -->
                   <img src={`https://api.dicebear.com/7.x/avataaars/svg?seed=${user.name}`} alt={user.name} class="w-full h-full rounded-full" />
                </div>
                <div class="flex flex-col">
                  <span class="text-[11px] font-medium text-gray-900">{user.name}</span>
                  <span class="text-[9px] text-gray-500">{user.email}</span>
                </div>
              </div>
              <div class="flex items-center gap-1 text-[10px] text-gray-500">
                {user.role}
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="w-2.5 h-2.5"><polyline points="6 9 12 15 18 9"></polyline></svg>
              </div>
            </div>
          {/each}
        </div>
      </div>
    </div>
  </div>
</div>
