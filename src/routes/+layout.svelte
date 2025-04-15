<script>
  import Footer from "../components/Footer.svelte";
  import Header from "../components/Header.svelte";
  import "../app.css";
  let y;
  let innerWidth = 0;
  let innerHeight = 0;

  function goTop() {
    document.body.scrollIntoView();
  }
</script>

<div
  class="container relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen"
  aria-label="Scroll to top"
>
  <div
    class="fixed right-3 bottom-0 duration-200 flex flex-row-reverse p-10 z-[10] {y >
    0
      ? ' opacity-full pointer-events-auto'
      : ' opacity-0 pointer-events-none'}"
  >
    <button
      on:click={goTop}
      class=" rounded-full bg-slate-900 text-violet-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer aspect-square grid place-items-center"
      aria-label="Scroll to top"
    >
      <i class="fa-solid fa-arrow-up"></i>
    </button>
  </div>
  <Header {y} />
  <slot />
  <Footer />
</div>
<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
