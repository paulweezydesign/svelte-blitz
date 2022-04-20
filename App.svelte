<script>
  import NavBrand from "./NavBrand.svelte";
  import NavLinks from "./NavLinks.svelte";
  import Sidebar from "./Sidebar.svelte";
  import Hamburger from "./Hamburger.svelte";
  let sidebar_show = false;
</script>

<style>
  body html {
    font-family: "Fira Sans", sans-serif;
  }
</style>

<nav class="bg-[#222] text-white/90 grid grid-cols-2 items-center h-[100px] w-[100vw]">
  <NavBrand />
  <NavLinks />
  <button on:click={() => sidebar_show = !sidebar_show}>
    <Hamburger />
  </button>
  <Sidebar bind:show={sidebar_show} />
</nav>
<main>
  <div class="container mx-auto ">
	  <h1 class="text-center font-black text-6xl mt-8 ">Hello CodeSandbox</h1>
	  <h2 class="mt-3 text-center font-light text-3xl">Start editing to see some magic happen!</h2>
  </div>
</main>