<script>
  let socialMedias = [
    {
      platform: "Email",
      username: "DemoSite@TheTengis.com",
      link: "mailto:DemoSite@TheTengis.com",
      icon: "fa-solid fa-envelope",
    },
    {
      platform: "Github",
      username: "TengisCh",
      link: "https://github.com/TengisCh",
      icon: "fa-brands fa-github",
    },
    {
      platform: "LinkedIn",
      username: "Tengis Chinzorigt",
      link: "https://www.linkedin.com/in/tengis-ch/",
      icon: "fa-brands fa-linkedin",
    },
  ];
</script>

<footer
  class="py-16 sm:py-26 bg-black border-t border-violet-950 flex flex-col gap-8 justify-center items-center rounded-t-3xl"
>
  <p class="px-4 py-2 bg-white text-slate-950 font-medium">
    Connect with me &darr;
  </p>
  <div class="flex flex-col gap-4 items-start justify-center">
    {#each socialMedias as socialMedia}
      <p>
        <i class={socialMedia.icon} />
        <strong class="pr-2">{socialMedia.platform}:</strong><a
          href={socialMedia.link}
          class="text-violet-400"
        >
          {socialMedia.username}<sup
            ><span class="text-xs scale-75 pl-0.5"
              ><i
                class="fa-solid fa-arrow-up-right-from-square text-xs scale-75"
              /></span
            ></sup
          >
        </a>
      </p>
    {/each}
  </div>
</footer>
