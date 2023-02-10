<script setup>
  import courses from "../stores/subject.json";
  import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
    <h2>รายวิชาทั้งหมด</h2>
    <hr />
    <table>
      <tr>
        <th>รหัสวิชา</th>
        <th>ชื่อวิชา</th>
      </tr>
  
      <tr v-for="(course, index) in courses" :key="index">
        <td>{{ course.course_id }}</td>
        <td>
          {{ course.course_name }}
        </td>
      </tr>
    </table>
    <router-link to="/adddrop">เพิ่มถอนรายวิชา</router-link>
    <RouterView />
</template>

