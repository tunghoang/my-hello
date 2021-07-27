<template>
  <h4>Hello {{name}} <button @click="$emit('leaderremove')">Remove</button></h4>
</template>

<script>
  export default {
    props: ['name'],
    methods: {
    }
  }
</script>

<style>
</style>
