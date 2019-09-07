<template>
  <v-container>
    <v-row >
      <Profile />
      <PostList :posts="posts" />
    </v-row>
  </v-container>
</template>

<script>
import Profile from "~/components/Profile.vue";
import PostList from "~/components/PostList.vue";

export default {
  components: {
    Profile,
    PostList
  },
  asyncData ({$axios}) {
    return $axios.get('https://www.googleapis.com/blogger/v3/blogs/4606092665974021629/posts?key=AIzaSyDci4ioLXX-x0SsC88MOQk399SO0PMPR14&fetchImages=true')
    .then((res) => {
      return {posts:res.data.items}
    });
  },
};
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
</style>
