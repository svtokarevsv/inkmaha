<template>
  <section class='mt-15 flex flex-col'>
    <h2 class='max-w-5xl mb-5'>{{ group.name }}</h2>
    <div class='grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8'>
      <project-item v-for='(item, index) in itemsToShow' :key='index' :item='item' :group='group'></project-item>
    </div>
    <button :id='`button_${group.id}`' class='button text-primary border-primary hover-primary-800 mt-12 self-center mb-8'
            @click='toggleShowMore'>{{ showAll ? 'Show less' : 'Show more' }}
    </button>
  </section>
</template>

<script>
import ProjectItem from '~/components/ProjectItem'

export default {
  name: 'ProjectGroup',
  components: { ProjectItem },
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
  }
}
</script>

<style scoped>

</style>
