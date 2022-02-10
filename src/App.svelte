<script>
    import Pixel from "./Pixel.svelte";
    import Circle from "./Circle.svelte";
    import Background from "./Background.svelte";
    import Shape from "./Shape.svelte";

    const doodles = [
        {name: "circle", component: Circle},
        {name: "pixels", component: Pixel},
        {name: "background", component: Background},
        {name: "shape", component: Shape},
    ];
    let currentDoodle = doodles[0];

</script>
<style>
    main {
        display: flex;
    }
    nav {
        display: flex;
        margin: 25px 50px;
        flex-direction: column;
    }
</style>
<main>
    <nav>
        {#each doodles as doodle}
            <a href="/{doodle.name}"
               on:click|preventDefault|stopPropagation={() => currentDoodle = doodles.find(d => d.name === doodle.name)}>
                {doodle.name}
            </a>
        {/each}
    </nav>
    <section>
        <svelte:component this={currentDoodle.component}/>
    </section>

</main>

