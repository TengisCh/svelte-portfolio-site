<script>
  import Step from "./Step.svelte";
  let steps = [
    {
      name: "Poject 1",
      icon: "fa-solid fa-cart-shopping",
      description: "project details",
    },
    {
      name: "Poject 2",
      icon: "fa-solid fa-cart-shopping",
      description: "project details",
    },
    {
      name: "Poject 3",
      icon: "fa-solid fa-cart-shopping",
      description: "project details",
    },
  ];

  let benefits = [
    {
      name: "A self taught developer",
      description:
        "Sunt et cillum est velit esse deserunt voluptate cillum laboris eiusmod. Ea cillum esse ad ea anim non non nulla Lorem sunt tempor deserunt sunt. Aliqua nisi amet est amet consequat mollit minim. Est ut commodo aliqua minim in deserunt. Aute consectetur commodo commodo consequat duis do.",
    },
    {
      name: "Expertise in .NET API development",
      description:
        "Duis culpa aliqua anim irure qui ut labore Lorem et culpa ullamco pariatur eiusmod occaecat. Nostrud excepteur laborum qui laborum veniam dolor ullamco dolor veniam sint irure in. Id ullamco esse veniam culpa occaecat voluptate commodo eu do velit eiusmod.",
    },
    {
      name: "Azure certified",
      description:
        "Elit culpa est commodo ad excepteur mollit sint qui cupidatat dolore cupidatat ex aute. Tempor incididunt dolore amet exercitation nulla dolore. Laborum id tempor consequat exercitation adipisicing tempor magna aliquip anim officia fugiat pariatur.",
    },
  ];

  let comparison = [
    {
      name: "Dedication",
      icons: [
        "fa-solid fa-xmark text-slate-500",
        "fa-solid fa-check text-slate-500",
        "fa-solid fa-xmark text-slate-500",
        "fa-solid fa-check text-green-500",
      ],
    },
    {
      name: "Critical Though",
      icons: [
        "fa-solid fa-xmark text-slate-500",
        "fa-solid fa-check text-slate-500",
        "fa-solid fa-check text-slate-500",
        "fa-solid fa-check text-green-500",
      ],
    },
    {
      name: "Interpersonal skill",
      icons: [
        "fa-solid fa-check text-slate-500",
        "fa-solid fa-xmark text-slate-500",
        "fa-solid fa-check text-slate-500",
        "fa-solid fa-check text-green-500",
      ],
    },
    {
      name: "Programming ability",
      icons: [
        "fa-solid fa-check text-slate-500",
        "fa-solid fa-check text-slate-500",
        "fa-solid fa-xmark text-slate-500",
        "fa-solid fa-check text-green-500",
      ],
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="intoPage"
    class="grid grid-cols-1 lg:grid-cols-2 gap-2 py-8 sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center lg:text-left text-center gap-6 md:gap-8 sm:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi I'm <span class="poppins text-violet-400">Tengis</span> Chinzorigt
        <br />Full Stack
        <span class="poppins text-violet-400">Developer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-violet-400">favorite tech</span> includes Javascript
        (SvelteKit), TailwindCSS, ASP.NET Core & PostgresSQL!
      </p>
      <a
        href="https://www.linkedin.com/in/tengis-ch/"
        target="_blank"
        class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
        />
        <h4 class="relative z-9">Get in touch &rarr;</h4>
      </a>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <img
        src="images/profile.png"
        alt="Profile picuture"
        class="object-cover z-[2] max-h-[70vh"
      />
    </div>
  </section>

  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        A few of my creative endeavors.
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Curios to <span class="poppins text-violet-400">see</span> my work?
      </h3>
    </div>
    <a
      href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
      target="_blank"
      class="mx-auto px-4 rounded-md border border-solid border-white flex items-center gap -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
    >
      <i class="fa-regular fa-circle-play" />
      <p>Watch the video</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      {#each steps as step, i}
        <Step {step}>
          {step.description}
        </Step>
      {/each}
    </div>
  </section>

  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md: gap:24 relative"
  >
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
      <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        A bit <span class="poppins text-violet-400">about</span> me.
      </h3>
    </div>

    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
      I am ...
    </p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each benefits as benefit, index}
        <div class="flex gap-6 sm:gap-8">
          <p
            class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
          >
            0{index + 1}
          </p>
          <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-5xl">
              {benefit.name}
            </h3>
            <p>{benefit.description}</p>
          </div>
        </div>
      {/each}
    </div>
    <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">
      The <span class="text-violet-500 poppins">Complete</span> Package
    </h5>
    <div
      class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
    >
      <table class="bg-white text-slate-700 rouded text-center">
        <thead class="border-b border-solid border-slate-200">
          <tr>
            <th class="whitespace-nowrap p-2 px-4" />
            {#each { length: 3 } as _, i}
              <th class="whitespace-nowrap p-2 px-4">Candidate #{i + 1}</th>
            {/each}
            <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8">
              Me
            </th>
          </tr>
        </thead>
        <tbody>
          {#each comparison as skill, i}
            <tr class="border-b border-solid border-slate-200">
              <td
                class="border-r border-solid border-white pl-4 py-4 font-semibold whitespace-nowrap"
              >
                {skill.name}
              </td>
              {#each skill.icons as icon}
                <td><i class={icon} /></td>
              {/each}
            </tr>
          {/each}
        </tbody>
      </table>
    </div>
    <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
      <p class="">Scroll to see more &rarr;</p>
    </div>
    <p class="mx-auto">So why not invest?</p>
  </section>
</main>
