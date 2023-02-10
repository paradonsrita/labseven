<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
    <v-card max-width="448" class="mx-auto" color="grey-lighten-3">
    <v-layout>
      <v-app-bar
        color="teal-darken-1"
        image="https://picsum.photos/1920/1080?random"
      >
        <template v-slot:image>
          <v-img
            gradient="to top right, rgba(19,84,122,.8), rgba(128,208,199,.8)"
          ></v-img>
        </template>

        <template v-slot:prepend>
          <v-app-bar-nav-icon></v-app-bar-nav-icon>
        </template>

        
        <v-app-bar-title ><router-link to="/" >Home</router-link></v-app-bar-title>
        <v-app-bar-title><router-link to="/news">ข่าว</router-link></v-app-bar-title>
        <v-app-bar-title><router-link to="/plan">แผนการเรียน</router-link></v-app-bar-title>
        <v-app-bar-title><router-link to="/adddrop">เพิ่มถอนรายวิชา</router-link></v-app-bar-title>
        


        <v-spacer></v-spacer>

        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-heart</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </v-app-bar>

      
    </v-layout>
  </v-card>




  

  <div class="mark-1"><RouterView /></div>
</template>

<style scoped>
.mark-1{
  padding-top: 70px;
}


</style>
