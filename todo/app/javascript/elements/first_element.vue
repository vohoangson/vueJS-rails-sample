<template>
  <div id="first-element">
    <h1>This is the first element</h1>
  </div>
</template>

<script>
  export default {
    props: ['name', 'number'],
    data: function () {
      return {
        message: "This is the first element"
      }
    }
  };
</script>
