<script lang="ts">
  export let name: string = "Name";
  export let color: string = "orange"; // orange, blue, red
  export let className: string = "";
  
  const colors: Record<string, string> = {
    orange: "bg-orange-500 text-white fill-orange-500",
    blue: "bg-blue-600 text-white fill-blue-600",
    red: "bg-red-500 text-white fill-red-500",
    yellow: "bg-amber-400 text-white fill-amber-400"
  };
  
  $: currentColor = colors[color] || colors.orange;
</script>

<div class="absolute flex flex-col items-start pointer-events-none z-20 {className}">
  <!-- Cursor Arrow -->
  <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="drop-shadow-sm -mb-1 relative z-10">
    <path d="M5.65376 12.3673H5.46026L5.31717 12.4976L0.500002 16.8829L0.500002 1.19841L11.7841 12.3673H5.65376Z" class={currentColor} stroke="white" stroke-width="1"/>
  </svg>
  
  <!-- Label -->
  <div class="{currentColor} px-2.5 py-1 rounded-full rounded-tl-none text-[11px] font-bold shadow-sm ml-2">
    {name}
  </div>
</div>
