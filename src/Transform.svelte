<script>
    import 'css-doodle';

    const doodle = `
        <css-doodle click-to-update>
        :doodle {
            @grid: 10x10;
            @size: 25rem;
            grid-gap: 1px;
        }
        background-color: tomato;
        transform: scale(@rand(.1,.9));
        </css-doodle>
    `;
</script>
<style>
</style>
<main>{@html doodle}</main>

