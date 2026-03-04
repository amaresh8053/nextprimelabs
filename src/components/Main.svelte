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
      name: "AI & Cloud Experts",
      description:
        "Our team consists of seasoned engineers with deep expertise in machine learning, cloud architecture, and distributed systems. We stay at the forefront of AI innovation and cloud-native technologies.",
    },
    {
      name: "Production-Ready Excellence",
      description:
        "Every solution we deliver is battle-tested, scalable, and optimized for performance. We believe in meticulous engineering and follow industry best practices for reliability and security.",
    },
    {
      name: "End-to-End Partnership",
      description:
        "From initial consultation through deployment and beyond, we work closely with your team. Transparent communication and collaborative problem-solving are core to our approach.",
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
      <div class="flex flex-col sm:flex-row gap-4 mx-auto lg:mx-0">
        <a
          href="#services"
          class="blueShadow text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 font-semibold text-center"
        >
          <div
            class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
          ></div>
          <span class="relative z-10">Explore Our Work →</span>
        </a>
        <a
          href="mailto:hello@nextprime.io?subject=Demo%20Request"
          class="text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full border-2 border-white/40 text-white font-semibold hover:border-violet-300 duration-200 text-center"
        >
          <span class="relative z-10">Schedule a Demo</span>
        </a>
      </div>
    </div>
    <div class="relative grid place-items-center">
      <img
        src="/images/brain.png"
        alt="Nextprime AI illustration"
        class="max-h-[95vh] w-full max-w-[820px] object-contain rounded-2xl shadow-2xl drop-shadow-[0_28px_110px_rgba(109,40,217,0.35)]"
        loading="eager"
        decoding="async"
      />
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
        We are <span class="poppins text-violet-300">innovators</span> & <span class="poppins text-violet-300">builders</span>
      </h3>
    </div>

    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl text-white">
      What makes us different . . .
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

    <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins text-white mt-8">
      The <span class="text-violet-300">Complete</span> Stack
    </h5>

    <div class="flex flex-col overflow-x-auto gap-10 max-w-full mx-auto w-full px-4">
      <table class="bg-white/5 text-white rounded-lg border border-white/10 text-center mx-auto w-full max-w-2xl">
        <thead class="border-b border-violet-700/40">
          <tr>
            <th class="p-3 text-left text-sm font-semibold"></th>
            <th class="whitespace-nowrap p-3 px-4 text-sm font-semibold">Competitor A</th>
            <th class="whitespace-nowrap p-3 px-4 text-sm font-semibold">Competitor B</th>
            <th class="whitespace-nowrap p-3 px-4 text-sm font-semibold">Competitor C</th>
            <th class="bg-violet-700 text-white whitespace-nowrap p-4 px-6 rounded-tr-lg text-sm font-semibold">
              Nextprime
            </th>
          </tr>
        </thead>
        <tbody>
          <tr class="border-b border-white/10">
            <td class="border-r border-white/10 pl-3 pr-4 py-3 font-medium text-sm text-left">AI Expertise</td>
            <td><i class="fa-solid fa-xmark text-red-500"></i></td>
            <td><i class="fa-solid fa-check text-gray-400"></i></td>
            <td><i class="fa-solid fa-xmark text-red-500"></i></td>
            <td><i class="fa-solid fa-check text-green-400 text-lg"></i></td>
          </tr>
          <tr class="border-b border-white/10">
            <td class="border-r border-white/10 pl-3 pr-4 py-3 font-medium text-sm text-left">Cloud Native</td>
            <td><i class="fa-solid fa-check text-gray-400"></i></td>
            <td><i class="fa-solid fa-xmark text-red-500"></i></td>
            <td><i class="fa-solid fa-check text-gray-400"></i></td>
            <td><i class="fa-solid fa-check text-green-400 text-lg"></i></td>
          </tr>
          <tr class="border-b border-white/10">
            <td class="border-r border-white/10 pl-3 pr-4 py-3 font-medium text-sm text-left">24/7 Support</td>
            <td><i class="fa-solid fa-xmark text-red-500"></i></td>
            <td><i class="fa-solid fa-check text-gray-400"></i></td>
            <td><i class="fa-solid fa-xmark text-red-500"></i></td>
            <td><i class="fa-solid fa-check text-green-400 text-lg"></i></td>
          </tr>
          <tr>
            <td class="border-r border-white/10 pl-3 pr-4 py-3 font-medium text-sm text-left">Custom Solutions</td>
            <td><i class="fa-solid fa-check text-gray-400"></i></td>
            <td><i class="fa-solid fa-check text-gray-400"></i></td>
            <td><i class="fa-solid fa-xmark text-red-500"></i></td>
            <td><i class="fa-solid fa-check text-green-400 text-lg"></i></td>
          </tr>
        </tbody>
      </table>
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
