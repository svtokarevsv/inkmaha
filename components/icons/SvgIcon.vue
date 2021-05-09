<template>
  <component :is="name"  class="svg-wrapper fill-current stroke-current"/>
</template>

<script>
import Behance from './behance.svg?inline';
import Email from './email.svg?inline';
import Instagram from './instagram.svg?inline';
import Linkedin from './linkedin.svg?inline';

export default {
  props: {
    name: String,
  },
  components:{
    Behance,
    Email,
    Instagram,
    Linkedin,
  },
}
</script>

<style scoped>
  .svg-wrapper{
    @apply cursor-pointer w-8 h-8;
  }
</style>
