<template>
  <div id="contactForm">
    <h1>Have an idea? <span class="accent">Let's do somthing about it!</span></h1>
    <div v-if="isSending" class=""></div>
    <form class="form" @submit="onSubmit" method="post">
      <input type="text" name="name" required v-model="contact.name" placeholder="Name" autocomplete="off">
      <input type="email" name="email" required v-model="contact.email" placeholder="Email" autocomplete="off">
      <textarea name="message" v-model="contact.message" rows='4' placeholder="Tell me about it..."></textarea>
      <button class="button" type="submit">Send</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  data: function (){
    return {
      contact:{
        name: '',
        email: '',
        message: ''
      },
      isSending: false
    }
  },
  methods: {
    // Clear The Form
    clearForm(){
      for(let field in this.contact){
        this.contact[field] = ''
      }
    },
    //Submit
    onSubmit(evt){
      evt.preventDefault();
      this.isSending = true;

      setTimeout(() => {
        // Build form data
        let form = new FormData();
        for (let field in this.contact){
          form.append(field, this.contact[field]);
        }

        //Send form to server
        this.$http.post('../php/app.php', form).then((response) => {
          console.log(response);
          this.clearForm();
          this.isSending= false;
        }).catch((e) => {
          console.log(e)
        });
      }, 1000)
    }
  }
}
</script>

<style lang="scss">
  
</style>