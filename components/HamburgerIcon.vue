<template>
  <div :class="`md:hidden hamburger ${isMobileHeaderOpen?'open':''}`" id='hamburger'
       @click="$emit('update:isMobileHeaderOpen', !isMobileHeaderOpen)">

  <span></span>
  <span></span>
  <span></span>
  </div>
</template>

<script>
export default {
  name: 'Hamburger',
  props: {
    isMobileHeaderOpen: Boolean,
  },
}
</script>
