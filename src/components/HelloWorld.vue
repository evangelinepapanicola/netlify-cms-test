<template>
  <div>
    <h1>This component mounts `aboutme.md` as Vue component</h1>
    <h2>{{ title }}</h2>
    <img :src="thumbnail" />
    <about-me />
  </div>
</template>

<script>
  import fm from "../../public/content/about/aboutme.md"

  export default {
    components: {
      AboutMe: fm.vue.component
    },
    data () {
      return {
        title: fm.attributes.title,
        thumbnail: fm.attributes.thumbnail
      }
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
