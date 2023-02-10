<script setup>
  import { useEnrollment } from "../stores/use";
  const enrollmentList = useEnrollment();
  const myEnrollment = enrollmentList.getState;
</script>


<template>
    <div class="container">
      <h2>วิชาที่ฉันลงทะเบียนทั้งหมด</h2>
      <table>
        <thead>
          <th>รหัสวิชา</th>
          <th>ชื่อวิชา</th>
        </thead>
        <tbody>
          <tr v-for="(subject, index) in myEnrollment" :key="index">
            <td>{{ subject.course_id }}</td>
            <td>{{ subject.course_name }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  

