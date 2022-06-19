<template>
  <div>
    <v-container>
        <h1>Welcome To  Podcast live <br/><span v-if="currentUser">{{currentUser.displayName}}</span></h1>

        <v-card elevation="12" class="pa-3">
            <signIn/>
        </v-card>
    </v-container>
  </div>
</template>

<script>
import signIn from '../components/signIn.vue'
export default {
    computed:{
     currentUser(){
        return this.$store.state.user;
     }
    },
  components:{
    signIn
  }
}
</script>

<style>

</style>