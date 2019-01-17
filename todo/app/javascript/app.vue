<template>
  <div id="app">
    <p>{{ message }}</p>
    <first-element></first-element>
    <div class="container">
      <div class="row">
        <div class="col-xs-12">
          <app-user></app-user>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import FirstElement from './elements/first_element.vue';
  import User from './elements/user.vue';

  export default {
    props: ['app'],
    data: function () {
      return {
        message: "Hello Vue ahuhu!"
      }
    },

    components: {
      firstElement: FirstElement,
      appUser: User
    },

    // mounted () {
    //   console.log(this);
    //   console.log('2', document.getElementById('app'))

    // },

    // created () {
    //   console.log('1', document.getElementById('app'))
    // }
  };
</script>

<style scoped>
p {
  font-size: 2em;
  text-align: center;
}
</style>
