<script lang="ts">
export default {
    name: "AbsenseComponent",
}
</script>

<template>
    <section class="bg-siga-1 w-[70%] rounded-md shadow-md mb-4 h-min">
        <div class="flex justify-between items-center bg-white py-6 ps-6 pe-10">
            <h2 class="text-2xl font-bold">Faltas</h2>
            <div class="flex justify-center items-center">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="#333333" viewBox="0 0 256 256"><path d="M165.66,202.34a8,8,0,0,1-11.32,11.32l-80-80a8,8,0,0,1,0-11.32l80-80a8,8,0,0,1,11.32,11.32L91.31,128Z"></path></svg>
                <span class="text-sm">1°SEMESTRE</span>
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="#000000" viewBox="0 0 256 256"><path d="M181.66,133.66l-80,80a8,8,0,0,1-11.32-11.32L164.69,128,90.34,53.66a8,8,0,0,1,11.32-11.32l80,80A8,8,0,0,1,181.66,133.66Z"></path></svg>
            </div>
        </div>

        <table class="w-full">
            <thead class="w-full">
                <tr class="w-full bg-[#F6F9FC]">
                    <th class="text-start text-siga-10 p-3">DISCIPLINAS</th>
                    <th class="text-center text-siga-10 p-3">AUSÊNCIAS</th>
                    <th class="text-center text-siga-10 p-3">PRESENÇAS</th>
                    <th class="text-center text-siga-10 p-3">FREQUÊNCIA</th>
                </tr>
            </thead>
            <tbody class="bg-white">
                <tr>
                    <td class="text-start p-4">Algorítimos e Lógica de Prog.</td>
                    <td class="text-center p-4">0</td>
                    <td class="text-center p-4">34</td>
                    <td class="text-center p-4">100%</td>
                </tr>
                <tr class="border-t border-[#b7b7b7]">
                    <td class="text-start p-4">Bases da Internet</td>
                    <td class="text-center p-4">0</td>
                    <td class="text-center p-4">34</td>
                    <td class="text-center p-4">100%</td>
                </tr>
                <tr class="border-t border-[#b7b7b7]">
                    <td class="text-start p-4">Criação de Conteúdo Web</td>
                    <td class="text-center p-4">0</td>
                    <td class="text-center p-4">34</td>
                    <td class="text-center p-4">100%</td>
                </tr>
                <tr class="border-t border-[#b7b7b7] h-8 w-full bg-white">
                    <td class="text-start p-4"></td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4"></td>
                </tr>
            </tbody>
        </table>
    </section>
</template>

