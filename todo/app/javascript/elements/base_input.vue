<template>
  <div>
    <input
      @input="$emit('inputChange', $event.target.value)">
    <p>{{ value}}</p>
  </div>
</template>

<script>
  export default {
    model: {
      prop: 'value',
      event: 'input'
    },
    props: ['label', 'value'],
    methods: {
    }
  };
</script>
