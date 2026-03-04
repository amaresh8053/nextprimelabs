<script>
  let { step, children } = $props();
</script>

<div
  class="p-6 sm:p-8 md:p-10 flex flex-col gap-6 rounded-xl border border-solid border-violet-700/40 text-center group hover:border-violet-400 hover:bg-white/5 duration-200 transition-all"
>
  <div
    class="h-20 w-20 sm:h-24 sm:w-24 grid place-items-center rounded-full border border-violet-500/40 bg-violet-500/10 text-4xl sm:text-5xl md:text-6xl -mt-14 sm:-mt-16 md:-mt-20 mx-auto shadow-[0_10px_40px_rgba(109,40,217,0.25)] duration-200 group-hover:scale-110"
  >
    <i class={step.icon}></i>
  </div>
  <h3 class="font-semibold text-xl sm:text-2xl md:text-3xl text-white">
    {step.name}
  </h3>
  {@render children()}
  {#if step.link}
    <a
      href={step.link}
      class="inline-flex items-center justify-center gap-1 text-violet-400 hover:text-violet-300 text-sm font-semibold duration-200 mt-auto"
    >
      Read more <i class="fa-solid fa-arrow-right text-xs"></i>
    </a>
  {/if}
</div>
