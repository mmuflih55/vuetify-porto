<template>
  <v-row>
    <v-col cols="12" xs="12" md="12">
      <v-card class="box-card">
        <h2>MY WORKS</h2>
        <br />
        <div class="bodycon">
          <v-card class="ma-3 pa-3">
            <p>
              <b>JALBA</b>
            </p>
            <p>
              Jalba is an app that I create for my team when we participate in an event called "1,000 Startups Movement",
              I create this with react native + redux as the state management and meteor js framework for the backend,
              my idea for this event is to create a traveling platform that have chats feature and ratings for the tour guide.
              So I use meteor as a back end to build easy chat app.
            </p>
            <br />
            <p>But this project fail because i can't find, tour maker/traveling agent partner Lol</p>
            <a
              href="https://play.google.com/store/apps/details?id=com.jalba"
            >https://play.google.com/store/apps/details?id=com.jalba</a>
            <div class="imgpreview">
              <img
                src="https://lh3.googleusercontent.com/D4tgvyDdPbrG3j3PbX3IJO0DubLkHavsLa2Iu3TjjzStVe44oGqwoULfoW2ZGl6w=s360-rw"
                alt
              />
              <img
                src="https://lh3.googleusercontent.com/sFW6FFee3mBxSNR5NRqqOndqj_sWKnDfl5f3uCktxjZO1gYdvnryVmNunMF41sonS_c=w1440-h620-rw"
                alt
              />
              <img
                src="https://lh3.googleusercontent.com/8lDscW4uWpovmsPMlBr3VP-RoGIxUdO3Ji6Nr3lFkjUZSwhX4PbY9MRSJXSgGAQmGA=w1440-h620-rw"
                alt
              />
            </div>
          </v-card>
          <v-card class="ma-3 pa-3">
            <p>
              <b>ARR</b>
            </p>
            <p>Just random app that i crate to learn flutter. it is a blog reader for my blogspot blog</p>
            <a
              href="https://play.google.com/store/apps/details?id=com.apemricarica"
            >https://play.google.com/store/apps/details?id=com.apemricarica</a>
            <div class="imgpreview">
              <img
                src="https://lh3.googleusercontent.com/NuZoyABcsopbZmP7EGPJ_QD06VXfI7cy7ycl49hzyWDWaCQxDWQC2LPxovYo9a_qa__4=w1440-h620-rw"
                alt
              />
              <img
                src="https://lh3.googleusercontent.com/AOyCqcdt-FgJHa07bm3v6tV2mVWcV2PTJkuBR8zmWNyLyu5TqmQjCN7ANX-BkTZyLA=w1440-h620-rw"
                alt
              />
              <img
                src="https://lh3.googleusercontent.com/MVHs5IY0azufh5ddZptPfDZtLIL5AiNFH8fFNJ9MvL567bJp6P0bsfz23DJ9nMwCY9Q=w1440-h620-rw"
                alt
              />
            </div>
          </v-card>
        </div>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import Profile from "~/components/Profile.vue";

export default {
  components: {
    Profile
  }
};
</script>

<style>
.bodycon {
  height: 85vh;
  overflow: hidden;
  overflow-y: scroll;
}

.imgpreview {
  display: flex;
}

.imgpreview img {
  width: 100px;
  margin: 15px;
  object-fit: contain;
}
</style>
