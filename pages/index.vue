<template>
  <main>
    <section class='h-120 bg-cover flex flex-col justify-end'
             v-bind:style="{ 'background-image': `url(${this.realPreviewImageUrl}` }">
      <button
        class='button self-center mb-8 border-gray-50 text-gray-50 hover:border-white hover:text-white'>
        Preview Showreel
      </button>
    </section>
    <ProjectGroup v-for='(group, index) in projectGroups' :id='group.id' :key='index' :group='group'/>
    <ContactMe/>
  </main>
</template>
<script>
import { mapState } from 'vuex'
import ProjectGroup from '~/components/ProjectGroup'
import ContactMe from '~/pages/ContactMe'

export default {
  components: { ContactMe, ProjectGroup },
  data:()=>({
    realPreviewImageUrl:'/img/sample_landscape_image.jpeg',
  }),
  computed:{
    ...mapState('projects',['projectGroups'])
  }
}
</script>
