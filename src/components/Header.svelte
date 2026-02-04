<script>
  export let y;

  export let tabs = [
        { name: "Services", link: "/#services" },
        { name: "About", link: "/#about" },
    { name: "Blog", link: "https://blog.nextprime.io" }
  ];
</script>

<header
    class={
        "sticky z-[10] top-0 flex items-center justify-between px-6 duration-200 " +
        (y > 0 ? "bg-slate-950 py-4" : "bg-transparent py-6")
    }
>
    <a href="/#home" class="flex items-center gap-3 text-white text-2xl sm:text-3xl font-extrabold poppins tracking-tight hover:text-violet-300 duration-200">
        <span>
            Nextprime <span class="font-semibold text-white/80">Labs</span>
        </span>
    </a>
    <div class="hidden items-center gap-4 sm:flex">
        {#each tabs as tab, index}
            <a
                href={tab.link}
                class="text-sm sm:text-base font-medium text-white/85 hover:text-violet-400 duration-200"
                target={index === 2 ? "_blank" : ""}
            >
                <p>{tab.name}</p>
            </a>
        {/each}
        <button
            class="blueShadow relative overflow-hidden rounded-full bg-white px-5 py-2 text-slate-950 font-semibold shadow-lg"
        >
            <div
                class="absolute top-0 right-full h-full w-full bg-violet-400 opacity-20 duration-200 group-hover:translate-x-full"
            ></div>
            <span class="relative z-10">Get in touch</span>
        </button>
    </div>
</header>