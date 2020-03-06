<template>
  <div ref="hero" id="hero">
    <Background />
    <!-- <canvas></canvas> -->

    <div id="logo">
      <!-- <img src="public/img/logo.svg" /> -->
      <svg
        id="gx-logo"
        class="tronFilter"
        data-name="gx-logo"
        xmlns:svg="http://www.w3.org/2000/svg"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1366 700"
      >
        <g class="svgWrapper">
          <defs>
            <filter id="glow">
              <fegaussianblur
                class="blur"
                result="coloredBlur"
                stddeviation="4"
              ></fegaussianblur>
              <femerge>
                <femergenode in="coloredBlur"></femergenode>
                <femergenode in="coloredBlur"></femergenode>
                <femergenode in="coloredBlur"></femergenode>
                <femergenode in="SourceGraphic"></femergenode>
              </femerge>
            </filter>
          </defs>
        </g>
        <g
          transform="translate(1.000000, 1.000000)"
          strF00="true"
          stroke-width="3"
        />

        <circle
          class="st0"
          style="fill-opacity: 10; stroke-width: 15;
         stroke: #0abcf2;"
          cx="670"
          cy="400.7"
          r="200"
        />
        <polygon
          class="st0"
          style="fill-opacity: 15; stroke-width: 6; stroke: #0abcf2;"
          points="482.6,238.3 957.6,390.9 400.5,617.7 870.7,391.9 350.6,230.7 1108.7 "
        />

        

        
        
        
        

        
        
      </svg>

      <div id="logo-text">
        <span class="flicker-on">t</span>
        <span>a</span>
        <span>c</span>
        <span>h</span>
        <span>y</span>
        <span>o</span>
        <span>n</span>
        
      </div>
    </div>
    <div id="eventInfo"><br>
      <div class="date">APRIL 10<sup>th</sup> - 11<sup>th</sup> 2020</div>
      <div>TECHFEST JUET 2020</div>
      <div>Stay Tuned</div>
    </div>
  </div>
</template>

<script>
import Background from "@/components/Background.vue";
export default {
  mounted() {
    let logoText = document.getElementById("logo-text").childNodes;
    let indices = [],
      i;
    for (i = 0; i < logoText.length; i++) {
      indices.push(i);
    }
    indices = this.shuffle(indices);

    i = 0;
    const interval = setInterval(() => {
      if (i == 13) {
        clearInterval(interval);
      }
      logoText[indices[i]].classList.add("flicker-on");
      i++;
    }, 100);

    let hero = document.getElementById("hero");
    let logo = document.getElementById("gx-logo");
    let text = document.getElementById("logo-text");

    let counter = 0;
    let updateRate = 1;
    hero.addEventListener("mousemove", event => {
      const isTimeToUpdate = function() {
        return counter++ % updateRate === 0;
      };
      if (isTimeToUpdate()) {
        let part = 60;
        let xLogo = (hero.clientWidth / 2 - event.clientX) / (part * 2);
        let yLogo = (hero.clientHeight / 2 - event.clientY) / (part * 2);
        let xText = (hero.clientWidth / 2 - event.clientX) / part;
        let yText = (hero.clientHeight / 2 - event.clientY) / part;
        let xDeg = (hero.clientWidth / 2 - event.clientX) / (part * 50);
        let yDeg = (hero.clientHeight / 2 - event.clientY) / (part * 20);
        if (window.innerWidth > 1120)
          logo.style.transform = `translate(${xLogo}px, ${yLogo}px) rotateX(${yDeg}deg) rotateY(${-xDeg}deg)`;
        text.style.transform = `translate(${xText}px, ${yText}px) rotateX(${yDeg}deg) rotateY(${-xDeg}deg)`;
        // logo.style.transform = `rotateX(${yDeg}deg) rotateY(${-xDeg}deg)`;
        // text.style.transform = `rotateX(${yDeg}deg) rotateY(${-xDeg}deg)`;
      }
    });
  },
  methods: {
    shuffle(array) {
      var currentIndex = array.length,
        temporaryValue,
        randomIndex;

      // While there remain elements to shuffle...
      while (0 !== currentIndex) {
        // Pick a remaining element...
        randomIndex = Math.floor(Math.random() * currentIndex);
        currentIndex -= 1;

        // And swap it with the current element.
        temporaryValue = array[currentIndex];
        array[currentIndex] = array[randomIndex];
        array[randomIndex] = temporaryValue;
      }

      return array;
    }
  },
  components: {
    Background
  }
};
</script>

<style>
@import "../assets/css/Hero.css";
</style>
