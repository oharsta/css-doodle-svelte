<script>
    import 'css-doodle';

    const doodle = `
        <css-doodle click-to-update>
        :doodle {
                @grid: 5x5;
                @size: 10rem;
                grid-gap: 1px;
            }
        background-color: tomato;
        </css-doodle>
    `;
</script>
<style>
</style>
<main>{@html doodle}</main>

