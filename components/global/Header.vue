<template>
  <nav class='fixed z-40 top-0 h-16 md:h-32 pt-0 md:pt-12 flex w-full max-w-inherit  bg-gray-50'
       aria-label='Main Menu'>
    <div class='flex items-center w-full'>
      <div id='logo-wrapper' class='lg:w-40 md:mr-3 md:ml-0 mx-auto'>
        <img src='/img/mt_logo.png' class='flex-none h-8 mb-2' alt="Maria Tokarieva's logo"
             style='border: none;'>
      </div>
      <ul class='items-center md:flex hidden' id='navigation_projects'>
        <li class='flex-1 ml-3 lg:ml-4 xl:ml-8' v-for='projectGroup in projectGroups'>
          <a class='block cursor-pointer text-hoverable'
             v-scroll-to='`#${projectGroup.id}`'>{{ projectGroup.link_name }}</a>
        </li>
        <li class='flex-1 ml-3 lg:ml-4 xl:ml-8'>
          <a class=' block cursor-pointer whitespace-no-wrap text-hoverable'
             v-scroll-to="'#Contact'">About / Contact</a>
        </li>
      </ul>
      <div class='ml-auto mb-4 grid grid-cols-4 gap-4 lg:gap-8 mr-px md:grid hidden'>
        <a class='block text-hoverable snakable border-primary' target='_blank'
           v-for='item in smm_links' :href='item.link'>
          <svg-icon :name='item.svg_name' />
        </a>
      </div>
    </div>
    <HamburgerIcon :isMobileHeaderOpen.sync='isMobileHeaderOpen' />
    <nav class='mobile-nav fixed top-0 right-0 flex h-full flex-col justify-between px-3 md:hidden'
         :class='isMobileHeaderOpen?"open":""'>
      <ul class='flex items-center flex-col mt-32'>
        <li class='flex-1 w-full mb-6' v-for='projectGroup in projectGroups'>
          <a class='block cursor-pointer text-hoverable'
             v-scroll-to='`#${projectGroup.id}`'>{{ projectGroup.link_name }}</a>
        </li>
        <li class='flex-1 w-full'>
          <a class=' block cursor-pointer whitespace-no-wrap text-hoverable'
             v-scroll-to="'#Contact'">About / Contact</a>
        </li>
      </ul>
      <div class='mb-4 flex flex-col items-center'>
        <a class='block text-hoverable snakable border-primary' target='_blank'
           v-for='item in smm_links' :href='item.link'>
          <svg-icon :name='item.svg_name' />
        </a>
      </div>
    </nav>
  </nav>
</template>

<script>
import SvgIcon from '~/components/icons/SvgIcon'
import { mapState } from 'vuex'

export default {
  name: 'Header',
  components: { SvgIcon },
  data: () => ({
    sections: [
      {
        name: 'Animation',
        path: ''
      }
    ],
    isMobileHeaderOpen: false
  }),
  computed: {
    ...mapState('projects', ['projectGroups', 'smm_links'])
  }
}
</script>

<style lang='postcss' scoped>

.scrim-bg {
}

.nuxt-link-exact-active {
  @apply text-primary-800  cursor-default;
}

.light-mode {

}
</style>
