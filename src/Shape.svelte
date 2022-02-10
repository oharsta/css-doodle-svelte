<script>
    import 'css-doodle';

    const doodle = `
        <css-doodle click-to-update>
          :doodle {
            @grid: 7 / 100vmax;
            background: #0a0c27;
          }
          @shape: clover 8;
          background: hsla(
            calc(360 - @i * 4), 70%, 68%, @r.8
          );
          transform:
            scale(@r(.2, 1.5))
            translate(@m2.@r(±50%));
        </css-doodle>
`;
</script>
<style>
    main {
      margin: 0;
      height: 100%;
      background: #12142E;
      display: grid;
      place-items: center;
      overflow: hidden;
      user-select: none;
}
</style>
<main>{@html doodle}</main>

