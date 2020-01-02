<template>
  <div id="app">
    <img class="title-image" src="@/assets/logo.png" alt="Title" />
    <p class="info">
      Take the role of an adventurer alone or with your friends locally and
      explore the open-world of Mystiqa. Explore towns and shop, conquer
      dungeons defeat mighty bosses and collect epic loot.
    </p>

    <VueGallery
      :images="images"
      :index="index"
      @close="index = null"
    ></VueGallery>
    <div class="screens nes-container is-dark is-rounded pointer">
      <img
        class="image-thumb"
        v-for="(image, imageIndex) in images"
        :key="imageIndex"
        :src="image"
        @click="index = imageIndex"
      />
    </div>
    <section class="contact">
      Contact Info
      <div class="contact-bar pointer">
        <a
          href="https://twitter.com/julcreutz"
          target="_blank"
          title="Twitter"
          alt="Twitter"
          ><i class="contact-icon nes-icon twitter is-medium pointer"></i
        ></a>
        <a
          href="https://www.reddit.com/r/mystiqa"
          target="_blank"
          title="reddit"
          alt="reddit"
          ><i class="contact-icon nes-icon reddit is-medium pointer"></i
        ></a>
      </div>
    </section>
  </div>
</template>

<script>
import "../node_modules/nes.css/css/nes.css";
import "./assets/fonts/PressStart2P.css";
import VueGallery from "vue-gallery";

export default {
  data: function() {
    return {
      images: [
        "./assets/screen-01.png",
        "./assets/screen-02.png",
        "./assets/screen-03.png",
        "./assets/screen-04.png",
        "./assets/screen-05.png",
        "./assets/screen-06.png"
      ],
      index: null
    };
  },
  components: { VueGallery }
};
</script>

<style lang="less">
html {
  background-color: black;
  cursor: default;
}

#app {
  align-content: center;
  align-items: center;
  background-color: black;
  color: white;
  display: flex;
  flex-direction: column;
  font-family: "Press Start 2P", cursive;
  height: 100%;
  justify-content: center;
  width: 100%;
}

.contact {
  align-items: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.contact-bar {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 125px;
}

.hovering-image {
  max-width: 150px;
}

.image-thumb {
  margin: 5px;
  max-height: 106px;
  max-width: 200px;
}

.info {
  max-width: 1200px;
  text-align: justify;
  font-size: 0.75em;
  padding: 12px;
}

.pointer {
  cursor: pointer;
}

.screens {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  max-width: 1200px;
  justify-content: center;
  width: 100%;
}
.title-image {
  width: 100%;
  max-width: 800px;
}

/* Custom, iPhone Retina */
@media only screen and (min-width: 320px) {
}
/* Extra Small Devices, Phones */
@media only screen and (min-width: 480px) {
  /* custom styles */
}
/* Small Devices, Tablets */
@media only screen and (min-width: 768px) {
  .image-thumb {
      max-height: 170px;
    max-width: 300px;
  }
}
/* Medium Devices, Desktops */
@media only screen and (min-width: 992px) {
  /* custom styles */
}
/* Large Devices, Wide Screens */
@media only screen and (min-width: 1200px) {
}
</style>
