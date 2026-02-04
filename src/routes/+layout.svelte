<script context="module">
	export const prerender = true;
</script>

<script>
    import Footer from "../components/Footer.svelte";
    import Header from "../components/Header.svelte";
    import favicon from "$lib/assets/favicon.svg";
    import "../app.css";

    let { children } = $props();

    let y = $state(0);
    let innerWidth = $state(0);
    let innerHeight = $state(0);

    function goTop() {
        document.body.scrollIntoView();
    }

    function handleScroll() {
        if (typeof window !== 'undefined') {
            y = window.scrollY;
            innerWidth = window.innerWidth;
            innerHeight = window.innerHeight;
        }
    }
</script>

<svelte:window on:scroll={handleScroll} bind:innerWidth bind:innerHeight />

<svelte:head>
    <link rel="icon" href={favicon} />
</svelte:head>

<div class="container relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen">
    <div
        class={
            "fixed bottom-8 right-8 duration-200 z-[10] " +
            (y > 0 ? "opacity-100 pointer-events-auto" : "pointer-events-none opacity-0")
        }
    >
        <button
            on:click={goTop}
            class="rounded-full bg-violet-600 hover:bg-violet-500 text-white px-4 py-4 cursor-pointer aspect-square grid place-items-center shadow-lg hover:shadow-xl duration-200 blueShadow"
            title="Scroll to top"
        >
            <i class="fa-solid fa-arrow-up text-lg"></i>
        </button>
    </div>

    <Header {y} {innerHeight} />

    {@render children()}

    <Footer />
</div>