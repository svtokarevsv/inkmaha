<template>
  <section class='mt-15 flex flex-col mb-24' id='Contact'>
    <h2 class='mb-6'>About me / Contact</h2>
    <div class='flex flex-col md:flex-row'>
      <img
        class="h-fit max-w-92"
        :src="this.meImage"
      >
      <div class='md:ml-8 flex-1 md:-m-1 mt-4 md:mt-0'>
        <p>There are Lorem ipsum dolor sit amet, consectetur adipisicing elit. In, maxime, totam! Atque, commodi eum fuga fugiat ipsa iste magni nostrum quasi quia ut. Assumenda beatae consequatur consequuntur fugiat, incidunt ipsam libero necessitatibus sed velit. Aut dolore non omnis quasi rerum sed, veritatis! Atque consequatur  </p>
        <p class='ml-6.5 mb-2 mt-8 text-primary-800'>I like to work with:</p>
        <div class='ml-6.5 flex'>
          <div class='mr-7'>
            <p>Adobe Lorem Ipsum</p>
            <p class='mt-1.5'>Adobe Lorem Ipsum</p>
            <p class='mt-1.5'>Adobe Lorem Ipsum</p>
            <p class='mt-1.5'>Adobe Lorem Ipsum</p>
            <p class='mt-1.5'>Adobe Lorem Ipsum</p>
            <p class='mt-1.5'>Adobe Lorem Ipsum</p>
          </div>
          <div class='mr-7'>
            <p>Adobe Lorem Ipsum</p>
            <p class='mt-1.5'>Adobe Lorem Ipsum</p>
            <p class='mt-1.5'>Adobe Lorem Ipsum</p>
            <p class='mt-1.5'>Adobe Lorem Ipsum</p>
          </div>
          <div>
            <p>Adobe Lorem Ipsum</p>
            <p class='mt-1.5'>Adobe Lorem Ipsum</p>
            <p class='mt-1.5'>Adobe Lorem Ipsum</p>
          </div>
        </div>
      </div>
    </div>
    <div class='flex flex-col items-center mt-24'> 
      <p class='mb-5 -ml-8'>I'd love to hear from your. Let's collaborate</p>
      <form class="contact-form" id="contact-form" >
        <div class="contact-form__group mt-1">
          <input type="text" id="name"  required/>
          <label for="name">Name</label>
        </div>
        <div class="contact-form__group mt-1">
          <input type="text" id="email"  name="email"
                 required/>
          <label for="email">E-mail</label>
        </div>
        <div class="contact-form__group contact-form__group--textarea mt-10">
          <textarea  name="message" id="message" rows="6"  required></textarea>
          <label for="message">Message</label>
        </div>
        <button class="button mt-8" id="sendMsg">Submit</button>
      </form>
    </div>
  </section>

</template>

<script>
export default {
  name: 'ContactMe',
  data:()=>({
    meImage:'/img/sample_landscape_image.jpeg',
  })

}
</script>

<style scoped>

</style>
