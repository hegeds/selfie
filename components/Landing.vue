<template>
  <v-container>
    <v-row>
      <v-col class="d-flex justify-center">
        <h1> Welcome! </h1>
      </v-col>
    </v-row>
    <v-row class="py-10">
      <v-col class="d-flex justify-center">
        <v-avatar width="40vmin" height="40vmin">
          <v-img
            alt="profile picture"
            src="/profile.jpg"
          />
        </v-avatar>
      </v-col>
    </v-row>
    <v-row class="grey justify-center rounded-pill" style="margin-left: 10vmin; margin-right: 10vmin">
      <v-col v-for="item in items" :key="item.href" cols="auto">
        <a :href="item.href" target="blank" style="text-decoration: none;">
          <v-icon size="8vmin" @click="href=item.href">
            {{ item.icon }}
          </v-icon>
        </a>
      </v-col>
    </v-row>
    <v-row class="py-10">
      <v-col class="d-flex justify-center">
        <a href="#about-me" style="text-decoration: none;">
          <v-icon size="16vmin">
            mdi-chevron-down
          </v-icon>
        </a>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      items: [
        {
          icon: 'mdi-github',
          href: 'https://github.com/hegeds'
        },
        {
          icon: 'mdi-stack-overflow',
          href: 'https://stackoverflow.com/users/11395278/b%c3%a1lint-heged%c3%bcs'
        },
        {
          icon: 'mdi-linkedin',
          href: 'https://www.linkedin.com/in/b%C3%A1lint-heged%C3%BCs-30650bb6/'
        },
        {
          icon: 'mdi-email',
          href: 'mailto:hegeds@gmail.com'
        }
      ]
    }
  }
}
</script>

<style>

</style>
