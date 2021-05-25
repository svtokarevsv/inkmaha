<template>
  <section class='mt-15 flex flex-col'>
    <h2 class='max-w-5xl mb-5'>{{ group.name }}</h2>
    <div class='grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8'>
      <div class='project-item' v-for='(item, index) in itemsToShow'
           :class='getColSpanClass(item.width)' :key='index'
           v-bind:style="{ 'background-image': `url(${item.url}` }"></div>
    </div>
    <button :id='`button_${group.id}`' class='button text-primary border-primary hover-primary-800 mt-12 self-center mb-8'
            @click='toggleShowMore'>{{ showAll ? 'Show less' : 'Show more' }}
    </button>
  </section>
</template>

<script>
export default {
  name: 'ProjectGroup',
  props: {
    group: Object,
  },
  data: () => ({
    showAll: false
  }),
  computed: {
    itemsToShow() {
      const itemsToShowShort = []
      let maxWidth = 6
      const itemsCopy = this.group.items.slice()
      while (maxWidth > 0) {
        const item = itemsCopy.shift()
        const itemWidth = item.width || 1
        maxWidth -= itemWidth
        itemsToShowShort.push(item)
      }
      return this.showAll ? this.group.items : itemsToShowShort
    }
  },
  methods: {
    toggleShowMore(){
      this.showAll = !this.showAll;
    },
    getColSpanClass(width = 1) {
      switch (width){
        case 1:
          return 'col-span-1'
        case 2:
          return 'col-span-1 md:col-span-2'
        case 3:
          return 'col-span-1 md:col-span-2 lg:col-span-3'
        case 4:
          return 'col-span-4 md:col-span-2 lg:col-span-3'
        default:
          break
      }
    }
  }
}
</script>

<style scoped>

</style>
