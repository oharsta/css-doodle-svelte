<script>
    import 'css-doodle';

    const doodle = `
        <css-doodle click-to-update>
        :doodle {
            @grid: 10x10;
            @size: 50vmax;
            grid-gap: 1px;
        }
        background-color: hsla(@r(360), 85%, @r(70%, 90%), @r(.9));
        transform: scale(@rand(.2,.6)) rotate(@p(±45deg));
        </css-doodle>
    `;
</script>
<style>
    main {
      background: grey;
}
</style>
<main>{@html doodle}</main>

