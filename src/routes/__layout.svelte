<script>
    import "../app.css";
    let open = false
    $: innerWidth = 0

    function handleClick(){
        open = !open
    }
    
</script>

<svelte:window bind:innerWidth/>

<main class="bg-white h-screen flex flex-col">
<nav>
<div class="flex items-center justify-between flex-wrap p-4 container mx-auto">
  
  <a href="/" >
  <div class="flex items-center flex-shrink-0 text-white mr-4">
    <svg class="fill-current h-8 w-8 mr-4" stroke="white"
    stroke-width="10"
    fill-opacity="0" 
    width="317" 
    height="405.1" 
    x="-92.8465"
    y="-184.123"
    viewBox="-20 -20 150 150"
    xmlns="http://www.w3.org/2000/svg">
      <path d="M60 120C40 100 60 0 40 0 30 0 20 120 10 120 0 120 0 60 20 60L90 60C110 60 110 0 100 0 80 0 90 120 110 120"/>
    </svg>
    <span class="font-semibold text-xl tracking-tight">Andree Hultgren</span>
  </div>
</a>
  <div class="block lg:hidden">
    <button on:click={handleClick} class="flex items-center px-3 py-2 border rounded text-gray-400 border-gray-400 hover:text-white hover:border-white">
      <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>
    </button>
  </div>
  {#if innerWidth >= 1023 || open}
	<div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
    <div class="text-sm lg:flex-grow">
      
    </div>
    <div>
      <a href="/frontend" class="block mt-4 lg:inline-block lg:mt-0 text-gray-400 hover:text-white mr-4">
        Frontend
      </a>
      <a href="/backend" class="block mt-4 lg:inline-block lg:mt-0 text-gray-400 hover:text-white mr-4">
        Backend
      </a>
      <a href="/database" class="block mt-4 lg:inline-block lg:mt-0 text-gray-400 hover:text-white mr-4">
        Database
      </a>
      <a href="/cloud" class="block mt-4 lg:inline-block lg:mt-0 text-gray-400 hover:text-white mr-4">
        Cloud
      </a>
      <a href="/work" class="block mt-4 lg:inline-block lg:mt-0 text-gray-400 hover:text-white mr-4">
        Work
      </a>
      <a href="/education" class="block mt-4 lg:inline-block lg:mt-0 text-gray-400 hover:text-white">
        Education
      </a>
    </div>
  </div>
  {/if}
</div>
</nav>
  <div class="container mx-auto bg-white flex-1 p-8 shadow-xl shadow-slate-400">
    <slot />
  </div>
</main>
