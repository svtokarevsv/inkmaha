<template>
  <nav class="fixed z-40 top-0 h-32 pt-12 flex w-full max-w-inherit items-center bg-gray-50" aria-label="Main Menu">
    <div id='logo-wrapper' class='lg:w-40 mr-3'>
      <img src="/img/mt_logo.png" class='flex-none h-8 mb-2' alt="Sviatoslav Tokariev's logo" style='border: none;'>
    </div>
    <ul class="flex items-center">
      <li class="flex-1 pl-1">
        <nuxt-link class=" block text-hoverable" to="/">Animation</nuxt-link>
      </li>
      <li class="flex-1 ml-8">
        <nuxt-link class=" block text-hoverable" to="/blog">Branding</nuxt-link>
      </li>
      <li class="flex-1 ml-8">
        <nuxt-link class=" block text-hoverable" to="/projects">UI / UX</nuxt-link>
      </li>
      <li class="flex-1 ml-8">
        <nuxt-link class=" block text-hoverable" to="/projects">Instagram</nuxt-link>
      </li>
      <li class="flex-1 ml-8">
        <nuxt-link class=" block text-hoverable" to="/projects">Illustration</nuxt-link>
      </li>
      <li class="flex-1 ml-8">
        <nuxt-link class=" block whitespace-no-wrap text-hoverable" to="/projects">About / Contact</nuxt-link>
      </li>
    </ul>
    <div id='smm' class='ml-auto mb-4 grid grid-cols-4 gap-8 mr-px'>
      <a class="block text-hoverable snakable border-primary" target="_blank" href="https://www.instagram.com/ink_maha">
        <svg-icon name="instagram"/>
      </a>
      <a class="block text-hoverable snakable border-primary" target="_blank" href="https://www.behance.net/Marun">
        <svg-icon name="behance"/>
      </a>
      <a class="block text-hoverable snakable border-primary" target="_blank" href="https://www.linkedin.com/in/maria-tokarieva">
        <svg-icon name="linkedin"/>
      </a>
      <a class="block text-hoverable snakable border-primary" target="_blank" href="mailto:inkmaha@gmail.com">
        <svg-icon name="email"/>
      </a>
    </div>
  </nav>
</template>

<script>
import SvgIcon from '~/components/icons/SvgIcon'
export default {
  name: 'Header',
  components: { SvgIcon }
}
</script>

<style lang="postcss" scoped>

.scrim-bg {
}
.nuxt-link-exact-active {
  @apply text-primary-800  cursor-default;
}

.light-mode {
 
}
</style>
