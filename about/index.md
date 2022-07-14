---
title: mypst
date: 2022-07-14 04:14:05
tags:

<body>
    <div class="content">
        <h2>小吴 & Ch，我们已经在一起了</h2>
        <div class="timer">
            <b id="d"></b> Days <b id="h"></b> Hours <b id="m"></b> Minutes <b id="s"></b> Seconds
        </div>
    </div>

    <script>
        function timer() {
          window.setTimeout("show_date_time()", 1000);
          var start = new Date("2022-04-08 00:21:00").getTime(); 
          var t = new Date().getTime() - start; 
            var h = ~~(t / 1000 / 60 / 60 % 24);
            if (h < 10) {
                h = "0" + h;
            }
            var m = ~~(t / 1000 / 60 % 60);
            if (m < 10) {
                m = "0" + m;
            }
            var s = ~~(t / 1000 % 60);
            if (s < 10) {
                s = "0" + s;
            }
            document.getElementById('d').innerHTML = ~~(t / 1000 / 60 / 60 / 24);
            document.getElementById('h').innerHTML = h;
            document.getElementById('m').innerHTML = m;
            document.getElementById('s').innerHTML = s;
        }
        timer();
        setInterval(timer, 1000);
    </script>
</body>
---
