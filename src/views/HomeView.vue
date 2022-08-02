<template>
  <main>
    <br />
    <section>
      <header @scroll.passive="mousescroll()">
        <img src="@/img/bg.jpg" id="bg" />
        <img src="@/img/moon.png" id="moon" />
        <img src="@/img/mountain.png" id="mountain" />
        <img src="@/img/road.png" id="road" />
        <h2 id="text">Welcome</h2>
      </header>
    </section>

    <br />
    <section>
      <!-- <img src="@/img/bg.jpg" class=""/> -->
      <img src="@/img/ceva2.png" id="mountain" />
      <img src="@/img/ceva3.png" id="moon-darth" />
      <img src="@/img/ceva1.png" id="darth" />
      <h2 id="text-darth">Animations all over</h2>
    </section>
  </main>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld,
  },
  data() {
    return {};
  },
  created() {
    window.addEventListener("scroll", this.mousescroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.mousescroll);
  },
  methods: {
    mousescroll(event) {
      let bg = document.getElementById("bg");
      let moon = document.getElementById("moon");
      let mountain = document.getElementById("mountain");
      let road = document.getElementById("road");

      let darth = document.getElementById("darth");
      let moondarth = document.getElementById("moon-darth");
      let mountaindarth = document.getElementById("mountain-darth");
      let textdarth = document.getElementById("text-darth");

      var value = window.scrollY;
      moon.style.right = -value * 1 + "px";
      moon.style.bottom = value * 0.2 + "px";
      moon.style.transform ="rotate(" + window.pageYOffset/10 + "deg)";

      darth.style.left = value *0.5 +'px';
    },
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Kdam+Thmor+Pro&display=swap');

*{
    
    font-family: 'Poppins', sans-serif;
}

body{
    background: #43180a !important;
    min-height: 1500px;
    align-content: center;
    justify-content: center;
}
section{
    position: relative;
    width: 100%;
    height: 107vh;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50px;
    padding: 1px;
}
section:before{
    content: '';
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 100px;
    background: linear-gradient(to top, #0a2a43, transparent);
    z-index: 1000;
}
section:after{
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    /* background: #43180a; */
    z-index: 10000;
    mix-blend-mode: color; /* all the elements are #0a2a43 */

}
section img{
    /* combine all the images here */
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    pointer-events: none;
}

#text{
    position: relative;
    color: #fff;
    font-size: 10em;
    z-index: 1;
}
</style>
