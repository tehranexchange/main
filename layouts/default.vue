<template>
  <v-app dark>
    <!-- <v-app-bar>
    </v-app-bar> -->
    <v-main>
        <Nuxt />
    </v-main>
    <!--<v-footer>
       <span>&copy; {{ new Date().getFullYear() }}</span> 
    </v-footer>-->
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
    }
  }
}
</script>
<style>
.v-application *{
  font-family:  "iryek" !important;
  font-weight: 200 !important;
}
</style>
