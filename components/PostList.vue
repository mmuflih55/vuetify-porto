
<template>
  <v-col cols="12" xs="12" md="9" >
    <v-card class="con">
      <h2 style="text-align:left;" class="pl-3 pt-3">My Blog Post</h2>
      <div class="bodycon">
        <a v-for="(p,i) in posts" :key="i" @click="toindex(i)">
          <v-card class="pl-3 pr-3 ma-3">
            <div class="plistcontent" >
                <div>
                  <img class="thumbnail" :src="p.images[0].url" alt="">
                </div>
                <div style="padding-left:10px;text-align:left">
                  <label><b>{{p.title}}</b></label>
                  <p>By: {{p.author.displayName}}</p>
                  <p>{{new Date(p.published).toDateString()}}</p>
                </div>
            </div>
          </v-card>
        </a>
      </div> 
    </v-card>
  </v-col>
</template>
<script>
import Header from "~/components/Header.vue";
import Profile from "~/components/Profile.vue";
import Footer from "~/components/Footer.vue";
import Post from "~/components/Post.vue";

export default {
  props:['posts'],
  methods: {
    toindex(idx){
      let id = this.posts[idx].id;
      this.$router.push(`/post/${id}`);
    }
  },
  mounted(){
    console.log(this.posts)
  }
};
</script>
<style scoped>
.thumbnail{
  height: 75px;
  width: 75px;
}

.con{
  height: 80vh;
}

.bodycon {
  height: 90%;
  overflow: hidden;
  overflow-y:scroll;
}

/* .postlist {
  margin: 10px 0 10px 0;
} */

.plistcontent {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.postlist:hover{
  cursor: pointer;
}

</style>
