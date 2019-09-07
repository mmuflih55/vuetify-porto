<template>
  <v-container>
    <v-row >
    <Profile/>
    <PostDetail :data="postdata"/>
    </v-row>
  </v-container>
</template>

<script>
import Profile from '~/components/Profile.vue'
import PostDetail from '~/components/Post.vue'

export default {
  components: {
    Profile,
    PostDetail,
  },
  asyncData ({$axios,params}) {
    return $axios.get(`https://www.googleapis.com/blogger/v3/blogs/4606092665974021629/posts/${params.slug}?key=AIzaSyDci4ioLXX-x0SsC88MOQk399SO0PMPR14`)
    .then((res) => {
      // console.log(res);
      return {postdata:res.data}
    });
  },
  mounted(){
    // console.log(this.$route.params);
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
