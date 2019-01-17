<template>
  <div class="component">
    <h3>User Details</h3>
    <p>Tuoi toi: {{ age }}</p>
    <p>Email cua toi: {{ email }}</p>
    <button v-on:click="changeAge">Doi tuoi</button>
  </div>
</template>

<script>
  export default {
    props: ['name', 'age'],
    data: function () {
      return {
        email: "a@gmail.com"
      }
    },
    methods: {
      changeAge() {
        this.age = 24,
        this.$emit('ageWasUpdated', this.age)
      }
    }
  };
</script>
