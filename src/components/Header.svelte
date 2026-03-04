<script>
  export let y;

  export let tabs = [
        { name: "Services", link: "/#services" },
        { name: "About", link: "/#about" },
        { name: "Blog", link: "/blog" }
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
        {#each tabs as tab}
            <a
                href={tab.link}
                class="text-sm sm:text-base font-medium text-white/85 hover:text-violet-400 duration-200"
            >
                <p>{tab.name}</p>
            </a>
        {/each}
        <a
            href="mailto:hello@nextprime.io?subject=Getting%20in%20touch"
            class="blueShadow relative overflow-hidden rounded-full bg-white px-5 py-2 text-slate-950 font-semibold shadow-lg hover:bg-violet-100 duration-200"
        >
            <span class="relative z-10">Get in touch</span>
        </a>
    </div>
</header>