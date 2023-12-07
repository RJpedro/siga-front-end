<script setup lang="ts">
import HourGradeComponent from "@/components/hour-grade-component.vue";
import CurricularGradeComponent from "@/components/curricular-grade-component.vue";
</script>

<script lang="ts">
export default {
    name: "GradeArea",
}
</script>

<template>
    <section class="dashboard-area bg-siga-1 w-[86%] h-auto absolute right-0 top-0 flex flex-col overflow-y-auto">
        <div class="flex justify-between px-14 pt-8">
            <h1 class="text-black text-3xl">Horário de Aulas</h1>
            <div class="flex gap-4 items-center p-4 w-72 h-11 bg-white rounded-lg">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" class="fill-siga-4" viewBox="0 0 256 256"><path d="M229.66,218.34l-50.07-50.06a88.11,88.11,0,1,0-11.31,11.31l50.06,50.07a8,8,0,0,0,11.32-11.32ZM40,112a72,72,0,1,1,72,72A72.08,72.08,0,0,1,40,112Z"></path></svg>
                <span class="text-siga-4">Procurar</span>
            </div>  
        </div>
        <div class="flex justify-between px-14 pt-8">
            <HourGradeComponent />
        </div>
        <div class="flex justify-between px-14 pt-8">
            <CurricularGradeComponent />
        </div>
    </section>
</template>

