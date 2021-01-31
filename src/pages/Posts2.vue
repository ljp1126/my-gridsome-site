<template>
  <Layout>
    <div>
      <h1>Posts2</h1>
      <ul>
        <li v-for="edge in $page.posts.edges" :key="edge.node.id">
          <go-link to='/'>{{ edge.node.title }}</go-link>
        </li>
      </ul>
    </div>
  </Layout>
</template>

<page-query>
  query {
    posts: allPost {
      edges {
        node {
          id
          title
        }
      }
    }
  }
</page-query>

<script>
export default {
  name: 'Posts',
  data() {
    return {

    }
  },
  components: {

  },
  methods: {

    direct: function(val) { }
  }
}
</script>

<style lang='scss' scoped>

 
</style>
