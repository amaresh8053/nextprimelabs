<script>
  let { step, children } = $props();
</script>

<a
  href={step.href || "#"}
  target={step.href ? "_blank" : ""}
  class="p-6 sm:p-8 md:p-10 flex flex-col gap-6 rounded-xl border border-solid border-violet-700/40 text-center cursor-pointer group hover:border-violet-400 hover:bg-white/5 duration-200 transition-all"
>
  <div
    class="bg-slate-950 grid place-items-center px-4 text-5xl md:text-6xl -mt-14 sm:-mt-16 md:-mt-20 mx-auto duration-200 group-hover:scale-110"
  >
    <i class={step.icon} />
  </div>
  <h3 class="font-semibold text-xl sm:text-2xl md:text-3xl text-white">
    {step.name}
  </h3>
  {@render children()}
  <div class="flex-1 flex justify-end gap-4 items-end">
    <div
      class="ml-auto cursor-pointer text-violet-300 group-hover:text-violet-200 duration-200 relative"
    >
      <p>Learn more →</p>
    </div>
  </div>
</a>
