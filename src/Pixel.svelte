<script>
    import 'css-doodle';

    const doodle = `
        <css-doodle click-to-update>
          <style>
            :doodle {
              @grid: 3x2 / 97vmin auto;
              gap: 1.5vmin;
            }
            border: 1.2vmin solid #fff;
            box-shadow: 0 10px 10px -9px #0003;
            background-color: #143d59;
            background-size: 100% 100%;
            background-image: @pn(
              @pattern(
                grid: 10;
                match((int(x+y)%2) == 0) {
                  fill: #f4b51c;
                }
              ),
              @pattern(
                grid: 63;
                match(((int(x*x*y*y)>>5)%2) == 1) {
                  fill: #f4b51c;
                }
              ),
              @pattern(
                grid: 71;
                match(((int(x*y*x*y*7.)>>4)&2) == 2) {
                  fill: #f4b51c;
                }
              ),
              @pattern(
                grid: 43;
                match(((int(sin(y)*sin(x)*6.)>>2)&1) != 1) {
                  fill: #f4b51c;
                }
              ),
              @pattern(
                grid: 43;
                match(((int(cos(x)*cos(y)*5.)>>2)&1) != 1) {
                  fill: #f4b51c;
                }
              ),
              @pattern(
                grid: 80;
                match((int(x*x + y*y)%80) <= 17) {
                  fill: #f4b51c;
                }
              )
            );
          </style>
        </css-doodle>
    `;
</script>
<style>
    main {
      margin: 0;
      height: 100%;
      display: grid;
      place-items: center;
      background: #e0e0e0;
    }
</style>
<main>{@html doodle}</main>

