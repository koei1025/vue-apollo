<template>
  <div>
    <!-- 1 -->
    <h4 v-if="loading">Loading...</h4>
    <link-item
      v-for="film in allFilms"
      :key="film.id"
      :film="film">
    </link-item>
  </div>
</template>

<script>
  // 2
  import { ALL_LINKS_QUERY } from '../contents/graphql'
  import LinkItem from './LinkItem'

  export default {
    name: 'LinkList',
    data () {
      return {
        // 3
        allFilms: [],
        loading: 0
      }
    },
    components: {
      LinkItem
    },
    // 4
    apollo: {
      allFilms: {
        query: ALL_LINKS_QUERY
      }
    }
  }
</script>