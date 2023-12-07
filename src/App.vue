<script setup lang="ts">
import LoginArea from "@/sections/login-area.vue";
import SidebarComponent from "@/components/sidebar-component.vue";
// import DashboardArea from "@/sections/dashboard-area.vue";
import GradeArea from "@/sections/grade-area.vue";
</script>

<template>
  <SidebarComponent />
  <!-- <LoginArea /> -->
  <!-- <DashboardArea /> -->
  <GradeArea />
</template>

<script lang="ts">
export default {
  name: 'App',
  components: {
    LoginArea,
    SidebarComponent,
    // DashboardArea,
    GradeArea,
  }
}
</script>

<style>
@import '@/assets/output.css';
</style>
