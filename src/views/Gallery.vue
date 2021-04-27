<template>
  <div class="gallery d-flex justify-center d-flex align-center">
    <ComingSoon />
  </div>
</template>

<script>
import ComingSoon from '@/components/ComingSoon.vue'
export default {
    name: 'Gallery',
    components: {
      ComingSoon
    }
}
</script>

<style scoped>
.gallery {
  height: 100%;
}
</style>
