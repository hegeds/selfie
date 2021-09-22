<template>
  <v-container>
    <div class="bg" />
    <div class="bg bg2" />
    <div class="bg  bg2" />
    <div class="bg  bg3" />
    <div class="content">
      <v-row>
        <Landing style="min-height: 100vh" />
      </v-row>
      <v-row id="about-me" class="pt-16">
        <AboutMe />
      </v-row>
      <v-row id="skills" class="pt-16">
        <Skills />
      </v-row>
      <v-row id="cv" class="pt-16">
        <CV />
      </v-row>
    </div>
  </v-container>
</template>

<style scoped>
  .bg {
  animation:slide 10s ease-in-out infinite alternate;
  background-image: linear-gradient(-60deg, #455A64 50%, #37474F 50%);
  bottom:0;
  left:-50%;
  opacity:.5;
  position:fixed;
  right:-50%;
  top:0;
  z-index:-1;
}

.bg2 {
  animation-direction: alternate-reverse;
  animation-duration: 8s;
}

.bg3{
  animation-duration: 12s;
}

@keyframes slide {
  0% {
    transform:translateX(-25%);
  }
  100% {
    transform:translateX(25%);
  }
}
</style>
