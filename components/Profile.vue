<template>
  <v-col cols="12" xs="12" md="3">
    <v-card class="profile">
      <img class="pprofile" src="/pprofile.jpeg"/>
      <h3 style="margin: 0">Muhammad Muflih</h3>
      <br />
      <span style="textAlign:center">
        Hello~ I'm Muflih a Software Engineer with {{new Date().getFullYear()-2017}} years experience.
      </span>
      <br>
      <br>
      <div style="text-align:left; width:80%;">
          <b><p>Currently interest in :</p></b>
          <p>- Vue Js</p>
          <p>- React Js</p>
          <p>- React Native</p>
          <p>- Flutter</p>
      </div>
    </v-card>
  </v-col>
</template>

<style scoped>
.profilecon {
  float: left;
  margin: 10px;
  margin-right: 5px;
}

.pprofile{
    margin-top: 10px;
    width: 150px;
    height: 150px;
    object-fit: cover;
    border-radius: 50% !important;
}

.profile {
  height: 80vh;
  display: flex;
  align-items: center;
  text-align: center;
  flex-direction: column;
}
</style>
