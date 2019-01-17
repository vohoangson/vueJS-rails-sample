<template>
  <div class="component">
    <h3>Edit User</h3>
    <p>Tuoi cua toi: {{ userAge }} </p>
    <button @click="editAge">Thay doi</button>
  </div>
</template>

<script>
  export default {
    props: ['userAge'],
    methods: {
      editAge() {
        this.userAge += 1
        this.$emit('ageWasEdited', this.userAge)
        console.log(this.$attrs)
      }
    }
  };
</script>
