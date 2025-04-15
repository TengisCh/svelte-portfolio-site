<script>
  export let y;

  let navs = [
    { name: "Projects", link: "#projects" },
    { name: "About me", link: "#about" },
    // {name: 'Blog', '#blog'},
  ];
</script>

<header
  class="z-10 sticky top-0 duration-200 px-6 flex items-center justify-between border border-solid
  {y > 0
    ? 'py-4 bg-slate-950 border-violet-950'
    : 'py-6 bg-transparent border-transparent'}"
>
  <h1 class="font-medium">
    <strong class="font-bold poppins">Tengis</strong> Chinzorigt
  </h1>
  <nav class="sm:flex ml-auto items-center pr-4 gap-4 hidden">
    {#each navs as nav, index}
      <a href={nav.link} class="duration-200 hover:text-violet-400">
        <p>{nav.name}</p>
      </a>
    {/each}
  </nav>
  <a
    href="#contact"
    target="_blank"
    class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950"
  >
    <div
      class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
    ></div>
    <h4 class="relative z-9">Get in touch</h4>
  </a>
</header>
