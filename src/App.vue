<script setup lang="ts">
import LoginArea from "@/sections/login-area.vue";
import SidebarComponent from "@/components/sidebar-component.vue";
// import DashboardArea from "@/sections/dashboard-area.vue";
import GradeArea from "@/sections/grade-area.vue";
import CurricularGradeComponent from "@/components/curricular-grade-component.vue";
import TeachingPlansArea from "@/sections/teaching-plans-area.vue";
</script>

<template>
  <TeachingPlansArea />
</template>

<script lang="ts">
export default {
  name: 'App',
  components: {
    // LoginArea,
    // SidebarComponent,
    // DashboardArea,
    // GradeArea,
    // CurricularGradeComponent
  }
}
</script>

<style>
@import '@/assets/output.css';
</style>
