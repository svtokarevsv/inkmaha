<template>
  <section class='mt-15 flex flex-col mb-24'>
    <h2 class='mb-6'>About me / Contact</h2>
    <div class='flex'>
      <div class='min-w-92 bg-contain bg-no-repeat' v-bind:style="{ 'background-image': `url(${this.meImage}` }"></div>
      <div class='ml-8 flex-1 -m-1'>
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
      <p>I'd love to hear from your. Let's collaborate</p>
      <form class="contact-form" id="contact-form" >
        <div class="contact-form__group">
          <input type="text" id="name" value={this.state.name} onChange={this.handleChange} required/>
          <label for="name">NAME</label>
        </div>
        <div class="contact-form__group">
          <input type="text" id="email" value={this.state.email} onChange={this.handleChange} name="email"
                 required/>
          <label for="email">EMAIL</label>
        </div>
        <div class="contact-form__group contact-form__group--textarea">
						<textarea value={this.state.message} name="message" id="message" cols="30" rows="10" onChange={this.handleChange} required>
							</textarea>
          <label for="message">MESSAGE</label>
        </div>
        <button class="button--pink" id="sendMsg">Send message</button>
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
