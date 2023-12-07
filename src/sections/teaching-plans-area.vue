<script lang="ts">
export default {
    name: "TeachingPlansArea",
    data() {
        return {
            discipline_choiced: 1,
            discipline_info: {} as { name: string, emment: { avaliations: string[] }[], material: string, bibliography: string },
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
        this.create_fetch_api(`http://127.0.0.1:8000/api/disciplines/${this.discipline_choiced}`).then(discipline_info => {
            this.discipline_info = discipline_info;
        });
    }
}
</script>

<template>
    <section class="bg-siga-1 w-[70%] rounded-lg shadow-md h-min">
        <div class="flex justify-between px-14 pt-8">
            <h1 class="text-black text-3xl">Plano de Ensino de {{ discipline_info.name }}</h1>
            <div class="flex gap-4 items-center p-4 w-72 h-11 bg-white rounded-lg">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" class="fill-siga-4" viewBox="0 0 256 256"><path d="M229.66,218.34l-50.07-50.06a88.11,88.11,0,1,0-11.31,11.31l50.06,50.07a8,8,0,0,0,11.32-11.32ZM40,112a72,72,0,1,1,72,72A72.08,72.08,0,0,1,40,112Z"></path></svg>
                <span class="text-siga-4">Procurar</span>
            </div>  
        </div>

        <div class="flex w-full p-6">
            <div class="flex flex-col">
                <div v-for="(discipline_emment, index) in discipline_info.emment[0]" class="w-[90%] flex flex-col gap-4 mt-4">
                    <span v-if="String(index) != 'avaliations'" class="text-lg font-bold">{{ index }}</span>
                    <span v-if="String(index) != 'avaliations'">{{ discipline_emment }}</span>
                </div>
            </div>

            <div class="bg-white rounded-md shadow-md w-[30%] p-5 flex flex-col gap-4">
                <span class="text-lg text-gray-500">Carga Horária</span>
                <div class="flex justify-between border-b border-black">
                    <span>Aulas por semana</span>
                    <span>4</span>
                </div>
                <div class="flex justify-between border-b border-black">
                    <span>Aulas teóricas</span>
                    <span>2</span>
                </div>
                <div class="flex justify-between border-b border-black">
                    <span>Aulas práticas</span>
                    <span>2</span>
                </div>
                <div class="flex justify-between border-b border-black">
                    <span>Total</span>
                    <span>80</span>
                </div>
            </div>
        </div>

        <main class="bg-red-100">
            <div class="avaliations">
                <h2 class="text-2xl font-bold">Avaliações</h2>
                <ul>
                   <li v-for="(avaliation, index) in discipline_info.emment[0].avaliations" class="flex gap-4">
                        <h3>{{ index }}</h3>
                        <span>{{ avaliation }}</span>
                    </li> 
                </ul>
            </div>
            <div class="material">
                <h2 class="text-2xl font-bold">Material</h2>
                <span>{{ discipline_info.material }}</span>
            </div>
            <div class="bibliography">
                <h2 class="text-2xl font-bold">Bibliografia</h2>
                <span>{{ discipline_info.bibliography }}</span>
            </div>
        </main>
    </section>
</template>
