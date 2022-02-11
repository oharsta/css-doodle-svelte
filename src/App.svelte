<script>
    import Pixel from "./Pixel.svelte";
    import Circle from "./Circle.svelte";
    import Background from "./Background.svelte";
    import Shape from "./Shape.svelte";
    import Basic from "./Basic.svelte";
    import BasicLarge from "./BasicLarge.svelte";
    import TransformColor from "./TransformColor.svelte";
    import Transform from "./Transform.svelte";
    import TransformColorRotate from "./TransformColorRotate.svelte";

    const doodles = [
        {name: "basic", component: Basic},
        {name: "basic-large", component: BasicLarge},
        {name: "transform", component: Transform},
        {name: "transform-color", component: TransformColor},
        {name: "transform-color-rotate", component: TransformColorRotate},
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
        min-width: fit-content;
    }
    a.current {
        color: green;
    }
    section.comp {
        cursor: pointer;
    }
</style>
<main>
    <nav>
        {#each doodles as doodle}
            <a href="/{doodle.name}"
               class:current={currentDoodle.name === doodle.name}
               on:click|preventDefault|stopPropagation={() => currentDoodle = doodles.find(d => d.name === doodle.name)}>
                {doodle.name}
            </a>
        {/each}
    </nav>
    <section class="comp">
        <svelte:component this={currentDoodle.component}/>
    </section>

</main>

