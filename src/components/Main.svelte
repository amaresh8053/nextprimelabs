<script>
  import Step from "./Step.svelte";

  let services = [
    {
      name: "Affordable AI & Cloud",
      icon: "fa-solid fa-bolt",
      description:
        "Automated infrastructure provisioning and GitOps-driven operations eliminate manual overhead—so we pass the savings directly to you. Enterprise-grade AI and cloud at startup-friendly pricing.",
      link: "/blog/why-low-cost",
    },
    {
      name: "Cloud Desktop",
      icon: "fa-solid fa-desktop",
      description:
        "Developer-ready Ubuntu cloud desktops pre-loaded with dev tools, Docker, and Crawlbot compatibility. Security researchers get a hardened pentest environment built-in—Kali Linux coming soon.",
      link: "/blog/cloud-desktop",
    },
    {
      name: "One-Click Open Source",
      icon: "fa-solid fa-rocket",
      description:
        "Deploy Grafana, Nextcloud, GitLab, Mattermost, and dozens more in one click. We handle every heavyweight installation—you pay only for the infrastructure you actually use.",
      link: "/blog/one-click-opensource",
    },
  ];

  let capabilities = [
    {
      name: "Built for Practical Outcomes",
      description:
        "We focus on the parts that move your business forward: faster launches, lower infra overhead, and dependable systems that are easy for your team to operate.",
    },
    {
      name: "Fast Delivery, Clean Operations",
      description:
        "From provisioning to deployment, we automate repeatable workflows so your products ship quickly without creating maintenance debt.",
    },
    {
      name: "Clear Scope, Transparent Support",
      description:
        "You get clear ownership, straightforward communication, and support aligned to your roadmap—not vague promises or bloated service bundles.",
    },
  ];

  let blogPosts = [
    {
      title: "Why We Can Offer Low-Cost AI & Cloud",
      summary:
        "Automated provisioning, IaC, and GitOps-driven operations let us pass real savings to you—without sacrificing reliability or performance.",
      category: "Infrastructure",
      date: "Feb 2026",
      link: "/blog/why-low-cost",
    },
    {
      title: "Cloud Desktop for Developers & Security Researchers",
      summary:
        "Ubuntu cloud desktops pre-loaded with dev tools, Docker, and Crawlbot. Pentest tools built-in—Kali Linux coming soon.",
      category: "Cloud Desktop",
      date: "Feb 2026",
      link: "/blog/cloud-desktop",
    },
    {
      title: "Deploy Open Source Software in One Click",
      summary:
        "Grafana, GitLab, Nextcloud, and more—live in minutes. We handle the heavy lifting; you pay only for the infra you use.",
      category: "Open Source",
      date: "Mar 2026",
      link: "/blog/one-click-opensource",
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <!-- Hero Section -->
  <section id="home" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
    <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl leading-tight">
        Welcome to <span class="text-violet-300">Nextprime</span>
        <br />
        The Future of
        <span class="text-violet-300">AI & Cloud</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl text-white/80">
        We build intelligent, scalable cloud solutions powered by cutting-edge AI. From machine learning pipelines to enterprise infrastructure, we transform your vision into reality using modern tech like Python, TensorFlow, Kubernetes, AWS, and real-time data platforms.
      </p>
      <div class="flex justify-center lg:justify-start">
        <a
          href="#services"
          class="blueShadow text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-8 py-3 group rounded-full bg-slate-900/50 text-white font-semibold text-center border border-white/20"
        >
          <span class="absolute inset-0 bg-gradient-to-r from-violet-400 via-fuchsia-500 to-orange-300 opacity-0 group-hover:opacity-100 transition duration-400 ease-out"></span>
          <span class="absolute inset-[1px] rounded-full bg-slate-900/90 group-hover:bg-transparent transition duration-400 ease-out"></span>
          <span class="relative z-10 flex items-center justify-center gap-3 uppercase tracking-wide text-sm sm:text-base">
            Explore Our Work
            <i class="fa-solid fa-arrow-right text-sm"></i>
          </span>
        </a>
      </div>
    </div>
    <div class="relative grid place-items-center overflow-hidden">
      <div class="absolute inset-0 m-auto h-64 w-64 rounded-full bg-violet-500/25 blur-3xl"></div>
      <img
        src="/images/ai-in.webp"
        alt="Nextprime AI illustration"
        class="relative z-10 max-h-[95vh] w-full max-w-[860px] object-contain opacity-95 mix-blend-screen drop-shadow-[0_28px_110px_rgba(109,40,217,0.25)]"
        loading="eager"
        decoding="async"
      />
      <div class="pointer-events-none absolute bottom-0 left-0 z-20 h-28 w-full bg-gradient-to-b from-transparent via-slate-900/65 to-slate-900"></div>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl text-violet-300">Our Offerings</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl text-white">
        Cutting-Edge <span class="poppins text-violet-300">AI & Cloud</span> Solutions
      </h3>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 lg:gap-10 max-w-6xl mx-auto w-full">
      {#each services as service}
        <Step step={service}>
          <p class="text-white/80 text-sm sm:text-base">
            {service.description}
          </p>
        </Step>
      {/each}
    </div>
  </section>

  <!-- About Section -->
  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-1/4 before:w-1/2 before:h-1 before:bg-violet-700 after:absolute after:bottom-0 after:left-1/4 after:w-1/2 after:h-1 after:bg-violet-700 py-4"
    >
      <h6 class="text-lg sm:text-xl md:text-2xl text-violet-300">Why Choose Nextprime</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl text-white">
        Built for <span class="poppins text-violet-300">speed</span>, <span class="poppins text-violet-300">clarity</span> & <span class="poppins text-violet-300">results</span>
      </h3>
    </div>

    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl text-white">
      Why teams choose Nextprime
    </p>

    <div class="flex flex-col gap-16 w-full mx-auto max-w-[900px]">
      {#each capabilities as capability, index}
        <div class="flex gap-6 sm:gap-8">
          <p class="poppins text-4xl sm:text-5xl md:text-6xl text-violet-400 font-semibold flex-shrink-0">
            0{index + 1}
          </p>
          <div class="flex flex-col gap-4 sm:gap-6">
            <h3 class="text-2xl sm:text-3xl md:text-4xl font-semibold text-white">
              {capability.name}
            </h3>
            <p class="text-white/75 text-base sm:text-lg">
              {capability.description}
            </p>
          </div>
        </div>
      {/each}
    </div>

    <p class="mx-auto text-white text-center">Ready to accelerate your AI journey?
      <a href="mailto:hello@nextprime.io?subject=Let%27s%20Talk" class="text-violet-300 hover:text-violet-200 font-semibold duration-200 ml-1">Get in touch →</a>
    </p>
  </section>

  <!-- Blog Section -->
  <section id="blog" class="py-20 lg:py-32 flex flex-col gap-16">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl text-violet-300">From Our Blog</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl text-white">
        Insights & <span class="poppins text-violet-300">Updates</span>
      </h3>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto w-full">
      {#each blogPosts as post}
        <a
          href={post.link}
          class="group flex flex-col gap-4 rounded-xl border border-violet-700/40 p-6 sm:p-8 hover:border-violet-400 hover:bg-white/5 duration-200"
        >
          <div class="flex items-center justify-between">
            <span class="text-xs text-violet-400 uppercase tracking-widest font-semibold">{post.category}</span>
            <span class="text-xs text-white/40">{post.date}</span>
          </div>
          <h4 class="text-lg font-semibold text-white group-hover:text-violet-300 duration-200 leading-snug">{post.title}</h4>
          <p class="text-white/70 text-sm flex-1 leading-relaxed">{post.summary}</p>
          <span class="text-violet-400 text-sm font-semibold group-hover:text-violet-300 duration-200">
            Read more <i class="fa-solid fa-arrow-right text-xs"></i>
          </span>
        </a>
      {/each}
    </div>

    <div class="text-center">
      <a
        href="/blog"
        class="inline-flex items-center gap-2 text-white/70 hover:text-violet-300 duration-200 text-sm font-medium border border-white/20 hover:border-violet-400 px-6 py-3 rounded-full"
      >
        View all posts <i class="fa-solid fa-arrow-right text-xs"></i>
      </a>
    </div>
  </section>
</main>
