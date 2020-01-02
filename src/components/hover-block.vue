<template>
  <section
    @mouseover="hover = true"
    @mouseout="hover = false"
    class="hover-block nes-container is-dark is-rounded nes-pointer"
    :class="{ 'hover-block-filled': hover === true }"
  >
    <img class="hovering-image" src="../assets/Lich.png" alt="Lich" />
    <p v-if="hover === true">
      Take the role of an adventurer alone or with your friends locally and
      explore the open-world of Mystiqa and explore towns and shop, conquer
      dungeons defeat mighty bosses and collect epic loot.
    </p>
  </section>
</template>

<script>
export default {
  data: function() {
    return {
      hover: false
    };
  }
};
</script>

<style scoped>
.hover-block {
  width: 200px;
  -webkit-transition: width .5s;
  transition: width .5s;
}

.hover-block-filled {
    width: 300px;
}
</style>
