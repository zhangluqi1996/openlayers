<template>
  <div class="home">
    <OpenlayersMap />
  </div>
</template>

<script>
import OpenlayersMap from "@/components/OpenlayersMap";
export default {
  name: 'home',
  components: {OpenlayersMap}
}
</script>


<style scoped>
  .home {
    height: 100%;
  }
</style>
