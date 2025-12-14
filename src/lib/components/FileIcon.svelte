<script lang="ts">
  export let type: string = "ai"; // ai, ps, folder
  export let name: string = "Untitled";
  export let date: string = "April 5, 2025 08:15";
  export let className: string = "";

  const colors: Record<string, string> = {
    ai: "bg-[#330000] text-[#FF9A00] border-[#FF9A00]",
    ps: "bg-[#001E36] text-[#31A8FF] border-[#31A8FF]", 
    folder: "bg-blue-500 text-white"
  };

  $: colorClass = colors[type] || colors.folder;
</script>

<div class="flex flex-col items-center gap-2 {className}">
  <div class="w-16 h-20 rounded-lg {colorClass} border-t-4 flex items-center justify-center shadow-lg relative">
    <span class="text-2xl font-bold tracking-tighter">{type === 'ai' ? 'Ai' : type === 'ps' ? 'Ps' : ''}</span>
    <span class="absolute bottom-1 right-1 text-[8px] font-bold opacity-80 uppercase">{type}</span>
  </div>
  <div class="text-center">
    <p class="text-[10px] font-medium text-gray-700 leading-tight">{name}</p>
    <p class="text-[9px] text-gray-400 mt-0.5">{date}</p>
  </div>
</div>
