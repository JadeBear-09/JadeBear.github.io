# JadeBear.github.io
# Hi, I'm Jade

<p align="center">
  <img src="./file/apsgifs-snoopy-transparent.apng" width="190" alt="Snoopy and bird">
</p>

---

### Bio

I am a **Data Scientist** and **IIT Delhi graduate**.
I build **AI agents** and **deep-learning tools** that feel simple, calm, and useful in real life.

---

### What I Build
- **Practical Agent Lab:** Quiet agents for research, retrieval, and decision support.
- **Healthcare DL Assistant:** Deep-learning workflows for medical imaging, made accessible for non-technical users.

---

### Philosophy
- Build less noise.
- Build tools people can trust.
- Keep it simple.

---

### Let's Connect
- 📧 [Email](mailto:your-email@example.com)

<style>
  #snoopy-roamer {
    position: fixed;
    width: clamp(96px, 14vw, 160px);
    left: 0;
    top: 0;
    z-index: 25;
    pointer-events: none;
    opacity: 0;
    transform: translate3d(0, 0, 0) scaleX(1);
    transition: opacity 500ms ease;
    animation: snoopy-first-look 2.6s ease-out 1;
    will-change: transform, opacity;
  }

  #snoopy-roamer img {
    width: 100%;
    height: auto;
    display: block;
    filter: drop-shadow(0 6px 12px rgba(0, 0, 0, 0.2));
    user-select: none;
  }

  @keyframes snoopy-first-look {
    0% { opacity: 0; transform: scale(0.84); }
    30% { opacity: 1; transform: scale(1.04); }
    100% { opacity: 1; transform: scale(1); }
  }

  @media (prefers-reduced-motion: reduce) {
    #snoopy-roamer {
      animation: none;
      right: 14px;
      bottom: 14px;
      left: auto;
      top: auto;
      opacity: 0.64 !important;
      transform: none !important;
    }
  }
</style>

<div id="snoopy-roamer" aria-hidden="true">
  <img src="./file/apsgifs-snoopy-transparent.apng" alt="" loading="eager" decoding="async" onerror="this.src='./apsgifs-snoopy.gif'">
</div>

<script>
  (function () {
    var roamer = document.getElementById("snoopy-roamer");
    if (!roamer) return;

    var reducedMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
    if (reducedMotion) {
      roamer.style.opacity = "0.64";
      return;
    }

    var x = 12;
    var y = Math.max(80, window.innerHeight * 0.26);
    var tx = x;
    var ty = y;
    var speed = 0.022;
    var calmMode = false;

    function pickTarget(allowPeek) {
      var w = roamer.offsetWidth || 120;
      var h = roamer.offsetHeight || 120;
      var margin = 14;

      if (allowPeek && Math.random() < 0.22) {
        var edge = Math.floor(Math.random() * 4);
        if (edge === 0) return { x: -w * 0.55, y: rand(margin, window.innerHeight - h - margin) };
        if (edge === 1) return { x: window.innerWidth - w * 0.45, y: rand(margin, window.innerHeight - h - margin) };
        if (edge === 2) return { x: rand(margin, window.innerWidth - w - margin), y: -h * 0.45 };
        return { x: rand(margin, window.innerWidth - w - margin), y: window.innerHeight - h * 0.35 };
      }

      return {
        x: rand(margin, Math.max(margin, window.innerWidth - w - margin)),
        y: rand(margin, Math.max(margin + 40, window.innerHeight - h - margin))
      };
    }

    function rand(min, max) {
      return Math.random() * (max - min) + min;
    }

    function loop() {
      var dx = tx - x;
      var dy = ty - y;
      var dist = Math.hypot(dx, dy);

      if (dist < 2) {
        var next = pickTarget(true);
        tx = next.x;
        ty = next.y;
      } else {
        x += dx * speed;
        y += dy * speed;
      }

      var face = dx >= 0 ? -1 : 1;
      roamer.style.transform = "translate3d(" + x.toFixed(2) + "px," + y.toFixed(2) + "px,0) scaleX(" + face + ")";
      requestAnimationFrame(loop);
    }

    roamer.style.opacity = "0.98";
    var first = pickTarget(false);
    tx = first.x;
    ty = first.y;

    setTimeout(function () {
      calmMode = true;
      speed = 0.0135;
      roamer.style.opacity = "0.62";
    }, 6500);

    setInterval(function () {
      if (!calmMode) return;
      roamer.style.opacity = Math.random() < 0.5 ? "0.48" : "0.62";
    }, 5000);

    window.addEventListener("resize", function () {
      tx = Math.min(tx, window.innerWidth - (roamer.offsetWidth || 120) - 8);
      ty = Math.min(ty, window.innerHeight - (roamer.offsetHeight || 120) - 8);
    });

    loop();
  })();
</script>
