<template>
  <div id="app">
    <Slides/>
  </div>
</template>

<script>
import Slides from './components/Slides.vue'

export default {
  name: 'App',
  components: {
    Slides
  }
}
</script>

<style>
body {
  background: #000;
  margin: 0;
  font-family: 'Helvetica Neue', 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}
/** full screen on mobile & fixed size on desktop **/
.vue-insta-stories {
  position: absolute;
  height: 100vh;
  height: -webkit-fill-available;
  width: 100vw;
  top: 0;
}

.vue-insta-stories .timeline {
  width: 100vw !important;
}

.see-more-wrapper .see-more {
  width: 100vw !important;
  background: transparent;
}

@media (max-width: 768px) {
  .vue-insta-stories {
    position: relative;
    height: 730px;
    width: 420px;
  }

  .vue-insta-stories img {
    width: 100vw !important;
    margin: auto 0 !important;
  }

  .see-more-wrapper .see-more {
    bottom: 64px !important;
  }
}
</style>
