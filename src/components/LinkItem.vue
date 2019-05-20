<template>
  <div>{{film.title}}({{film.director}})</div>
</template>

<script>
  export default {
    name: 'LinkItem',
    props: ['film']
  }
</script>