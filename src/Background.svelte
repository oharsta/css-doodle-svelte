<script>
    import 'css-doodle';

    const doodle = `
        <css-doodle>
          <style>
            @grid: 1 / 100vw 100vh;
            background-size: 83px 135px;
            background-color: #D24B45;
            background-image: @doodle(
              @grid: 2 / 100%;
              background: @pn(#3C2B34, #F7F0E9, #F7F0E9);
              transform-origin:
                @pn(100% 100%, 0 100%, 100% 0, 0 0);
              transform:
                rotateX(45deg)
                skewY(@pn(34deg, -34deg, -34deg));
            );
          </style>
        </css-doodle>`;
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

