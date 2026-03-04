<svelte:head>
  <title>Deploy Open Source Software in One Click | Nextprime Labs Blog</title>
  <meta name="description" content="Deploy Grafana, Nextcloud, GitLab, Mattermost, and dozens more open-source apps in one click on Nextprime Cloud. We handle all installations—you pay only for the infrastructure you use." />
  <meta name="keywords" content="one click deploy, open source cloud, Grafana deploy, GitLab self-hosted, Nextcloud, Mattermost, Nextprime Cloud" />
  <meta property="og:title" content="Deploy Open Source Software in One Click | Nextprime Labs" />
  <meta property="og:description" content="We handle every heavyweight installation. You pay only for the infrastructure you use." />
  <meta property="og:type" content="article" />
  <meta property="og:url" content="https://nextprime.io/blog/one-click-opensource" />
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="Deploy Open Source Software in One Click | Nextprime Labs" />
  <meta name="twitter:description" content="Grafana, GitLab, Nextcloud, and more—live in minutes. We handle the heavy lifting." />
</svelte:head>

<main class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8 py-16 sm:py-24 text-white/90">
  <!-- Back -->
  <a href="/blog" class="inline-flex items-center gap-2 text-violet-400 hover:text-violet-300 duration-200 text-sm font-medium mb-10">
    <i class="fa-solid fa-arrow-left text-xs"></i> Back to Blog
  </a>

  <header class="space-y-4 mb-12">
    <div class="flex items-center gap-3">
      <span class="text-xs text-violet-400 uppercase tracking-widest font-semibold">Open Source</span>
      <span class="text-white/30">·</span>
      <span class="text-xs text-white/40">March 2026</span>
      <span class="text-white/30">·</span>
      <span class="text-xs text-white/40">5 min read</span>
    </div>
    <h1 class="text-3xl sm:text-4xl font-bold poppins text-white leading-tight">
      Deploy Any Open Source Software in One Click — We Handle the Heavy Lifting
    </h1>
    <p class="text-white/70 text-lg leading-relaxed">
      Self-hosting powerful open-source software has always meant hours of reading docs, debugging dependencies, and wrestling with reverse proxies. With Nextprime Cloud, that's over. One click and you're live.
    </p>
  </header>

  <div class="space-y-10 text-white/80">

    <section class="space-y-4">
      <h2 class="text-2xl font-semibold poppins text-white">The Problem with Self-Hosting</h2>
      <p class="leading-relaxed">
        Open-source software is incredible. Tools like Grafana, GitLab, and Nextcloud rival or surpass their SaaS counterparts in capability. But deploying them is painful:
      </p>
      <ul class="list-disc list-inside space-y-2 pl-2">
        <li>Complex installation instructions spread across multiple docs pages</li>
        <li>Dependency conflicts, missing system libraries, and version mismatches</li>
        <li>Manual SSL certificate setup and reverse proxy configuration</li>
        <li>Database initialisation, migrations, and backup strategies</li>
        <li>Firewall rules, security hardening, and ongoing updates</li>
      </ul>
      <p class="leading-relaxed">
        Most teams either give up and pay for a SaaS version, or spend days on setup that has nothing to do with their actual work. We think there's a better way.
      </p>
    </section>

    <section class="space-y-4">
      <h2 class="text-2xl font-semibold poppins text-white">How Nextprime One-Click Deploy Works</h2>
      <p class="leading-relaxed">
        Every app in our catalogue is backed by a hardened, production-tested deployment template. When you click <strong class="text-white">Deploy</strong>:
      </p>
      <ol class="space-y-3 pl-2">
        <li class="flex items-start gap-3">
          <span class="bg-violet-600 text-white text-xs font-bold rounded-full h-5 w-5 flex items-center justify-center flex-shrink-0 mt-0.5">1</span>
          <span>We provision dedicated infrastructure in your chosen region (AWS, GCP, or Azure)</span>
        </li>
        <li class="flex items-start gap-3">
          <span class="bg-violet-600 text-white text-xs font-bold rounded-full h-5 w-5 flex items-center justify-center flex-shrink-0 mt-0.5">2</span>
          <span>The app is deployed via our battle-tested Helm chart or Docker Compose template</span>
        </li>
        <li class="flex items-start gap-3">
          <span class="bg-violet-600 text-white text-xs font-bold rounded-full h-5 w-5 flex items-center justify-center flex-shrink-0 mt-0.5">3</span>
          <span>SSL/TLS is automatically configured with Let's Encrypt on your custom domain</span>
        </li>
        <li class="flex items-start gap-3">
          <span class="bg-violet-600 text-white text-xs font-bold rounded-full h-5 w-5 flex items-center justify-center flex-shrink-0 mt-0.5">4</span>
          <span>Automated backups and monitoring are set up before you even see the login screen</span>
        </li>
        <li class="flex items-start gap-3">
          <span class="bg-violet-600 text-white text-xs font-bold rounded-full h-5 w-5 flex items-center justify-center flex-shrink-0 mt-0.5">5</span>
          <span>You receive your app URL, admin credentials, and a live infrastructure dashboard</span>
        </li>
      </ol>
      <p class="leading-relaxed">
        Total time from click to usable app: <strong class="text-white">under 5 minutes</strong>.
      </p>
    </section>

    <section class="space-y-4">
      <h2 class="text-2xl font-semibold poppins text-white">What's in the Catalogue</h2>
      <p class="leading-relaxed">
        We currently support one-click deployment for the following apps, with more being added every month:
      </p>

      <div class="grid grid-cols-1 sm:grid-cols-2 gap-3 mt-2">
        {#each [
          { icon: "fa-solid fa-chart-line", name: "Grafana", desc: "Observability & dashboards" },
          { icon: "fa-brands fa-gitlab", name: "GitLab CE", desc: "Git repos, CI/CD, DevOps" },
          { icon: "fa-solid fa-cloud", name: "Nextcloud", desc: "File storage & collaboration" },
          { icon: "fa-solid fa-comments", name: "Mattermost", desc: "Team messaging platform" },
          { icon: "fa-brands fa-docker", name: "Portainer", desc: "Container management UI" },
          { icon: "fa-solid fa-server", name: "Prometheus", desc: "Metrics collection & alerting" },
          { icon: "fa-solid fa-robot", name: "n8n", desc: "Workflow automation" },
          { icon: "fa-solid fa-note-sticky", name: "Outline", desc: "Team knowledge base & wiki" },
          { icon: "fa-solid fa-envelope", name: "Listmonk", desc: "Newsletter & mailing lists" },
          { icon: "fa-solid fa-shield-halved", name: "Vaultwarden", desc: "Self-hosted password manager" },
          { icon: "fa-solid fa-code-branch", name: "Gitea", desc: "Lightweight Git service" },
          { icon: "fa-solid fa-calendar", name: "Cal.com", desc: "Scheduling & bookings" },
        ] as app}
          <div class="flex items-center gap-3 rounded-lg border border-white/10 p-3 hover:border-violet-400/50 duration-200">
            <div class="h-9 w-9 grid place-items-center rounded-lg bg-violet-500/10 border border-violet-500/20 text-violet-300 flex-shrink-0">
              <i class={app.icon + " text-sm"}></i>
            </div>
            <div>
              <p class="text-white text-sm font-semibold">{app.name}</p>
              <p class="text-white/50 text-xs">{app.desc}</p>
            </div>
          </div>
        {/each}
      </div>
      <p class="text-sm text-white/60 mt-2">
        Don't see the app you need? <a href="mailto:hello@nextprime.io?subject=App%20Catalogue%20Request" class="text-violet-400 hover:text-violet-300 duration-200">Request it →</a>
      </p>
    </section>

    <section class="space-y-4">
      <h2 class="text-2xl font-semibold poppins text-white">Pay Only for What You Use</h2>
      <p class="leading-relaxed">
        There's no Nextprime platform fee on top of your infrastructure. You pay for the underlying cloud resources at our optimised rates (typically 20–40% below list price thanks to our reserved capacity and volume discounts). That's it.
      </p>
      <ul class="list-disc list-inside space-y-2 pl-2">
        <li>No per-app licensing fees—all apps are open source</li>
        <li>No "managed service" markup—you own the infrastructure</li>
        <li>Scale the app's resources up or down from your dashboard at any time</li>
        <li>Destroy it when you're done and stop paying immediately</li>
      </ul>
    </section>

    <section class="space-y-4">
      <h2 class="text-2xl font-semibold poppins text-white">You Own Everything</h2>
      <p class="leading-relaxed">
        Unlike SaaS products, your data lives in your own cloud account. We never have access to your application data. You can export, migrate, or self-manage your deployment at any time—there's no lock-in.
      </p>
    </section>

    <section class="rounded-xl bg-violet-700/20 border border-violet-600/40 p-8 space-y-4 text-center">
      <h2 class="text-2xl font-semibold poppins text-white">Try it yourself</h2>
      <p class="text-white/70">
        We're opening early access now. Tell us which app you want to deploy first and we'll have it live for you within minutes.
      </p>
      <a
        href="mailto:hello@nextprime.io?subject=One-Click%20Deploy%20Early%20Access"
        class="inline-block bg-violet-600 hover:bg-violet-500 text-white font-semibold px-8 py-3 rounded-full duration-200 mt-2"
      >
        Get Early Access
      </a>
    </section>

  </div>
</main>
