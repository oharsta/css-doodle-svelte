<script>
    import 'css-doodle';

    const doodle = `
        <css-doodle click-to-update>
        :doodle {
                @grid: 10x10;
                @size: 100vmax;
                grid-gap: 1px;
            }
        background-color: tomato;
        </css-doodle>
    `;
</script>
<style>
</style>
<main>{@html doodle}</main>

