<script>
    import 'css-doodle';

    const doodle = `
        <css-doodle click-to-update>
          <style>
            @grid: 80x1 / 80vmin;
            @size: @rn(0, 100%, 5);
            @offset: @plot(r: .5);
            @random(.3) { filter: blur(2px) }
            background-size: 35%;
            background-image: @svg(
              viewBox: 0 0 10 10;
              circle {
                r: @rn(0, .5, 5); cx: 9; cy: 5;
                fill: hsl(@rn(0, 360, 8), 80%, 50%);
              }
            );
          </style>
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

