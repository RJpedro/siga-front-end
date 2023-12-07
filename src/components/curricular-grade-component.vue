<script lang="ts">
export default {
    name: "CurricularGradeComponent",
    data() {
        return {
            discipline_per_semester: {} as Record<string, { name: string }[]>
        }
    },
    methods: {
        async create_fetch_api(url: string) {
            const response = await fetch(url);
            const data = await response.json();

            return data;
        }
    },
    created() {
        this.create_fetch_api('http://127.0.0.1:8000/api/disciplines').then(all_discplines => {
            this.discipline_per_semester = all_discplines;
        });
    }
}
</script>

<template>
    <section class="bg-siga-1 w-[70%] rounded-lg shadow-md h-min">
        <h2 class="text-2xl font-bold">Grade Curricular</h2>

        <div class="w-full flex mt-10">
            <div v-for="(disciplines, semester) in discipline_per_semester" class="w-full flex flex-col justify-center items-center">
                <span class="text-xl text-black text-opacity-70 font-bold mb-4">{{ semester }}° Semestre</span>
                <div v-for="(discipline) in disciplines" class="w-full flex flex-col justify-center items-center">
                    <div class="w-[164px] flex flex-col px-4 py-3 shadow-md bg-white mb-4">
                        <span class="text-sm text-black font-bold">IAL102</span>
                        <span class="flex flex-wrap text-sm text-black font-bold">{{ discipline.name }}</span>
                    </div>
                </div> 
            </div>
        </div>
    </section>
</template>

