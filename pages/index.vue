<template>
  <main>
    <section class='h-120 bg-cover flex flex-col justify-end'
             v-bind:style="{ 'background-image': `url(${this.realPreviewImageUrl}` }">
      <button
        class='button self-center mb-8 border-gray-50 text-gray-50 hover:border-white hover:text-white'>
        Preview Showreel
      </button>
    </section>
    <ProjectGroup v-for='(group, index) in projectGroups' :key='index' :name='group.name' :items='group.items'/>
    <ContactMe/>
  </main>
</template>
<script>
import ProjectGroup from '~/components/ProjectGroup'
import ContactMe from '~/pages/ContactMe'

export default {
  components: { ContactMe, ProjectGroup },
  data:()=>({
    realPreviewImageUrl:'/img/sample_landscape_image.jpeg',
    projectGroups:[
      {
        name: 'Animation',
        items: [
          {
            url: '/img/sample_landscape_image.jpeg',
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
        ],
      },
      {
        name: 'Branding',
        items: [
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg',
            width: 2,
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
        ],
      },
      {
        name: 'UI / UX',
        items: [
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg',
            width: 3,
          },
          {
            url: '/img/sample_landscape_image.jpeg',
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
        ],
      },
      {
        name: 'SMM / Instagram',
        items: [
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg',
            width: 2,
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
        ],
      },
      {
        name: 'Illustrations',
        items: [
          {
            url: '/img/sample_landscape_image.jpeg',
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
          {
            url: '/img/sample_landscape_image.jpeg'
          },
        ],
      }
    ],
  })
}
</script>
