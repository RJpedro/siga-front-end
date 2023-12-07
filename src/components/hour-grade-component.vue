<script setup lang="ts">
import CalendarComponent from "@/components/calendar-component.vue";
</script>

<script lang="ts">
export default {
    name: "HourGradeComponent",
}
</script>

<template>
    <section class="bg-siga-1 w-[70%] rounded-md shadow-md h-min">
        <div class="flex justify-end items-center bg-white py-6 ps-6 pe-10">
            <div class="flex justify-center items-center">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="#000000" viewBox="0 0 256 256"><path d="M165.66,202.34a8,,0,1-11.32,11.32l-80-80a8,,0,1,0-11.32l80-80a8,,0,1,11.32,11.32L91.31,128Z"></path></svg>
                <span class="text-sm">1°SEMESTRE</span>
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="#000000" viewBox="0 0 256 256"><path d="M181.66,133.66l-80,80a8,,0,1-11.32-11.32L164.69,128,90.34,53.66a8,,0,1,11.32-11.32l80,80A8,,0,1,181.66,133.66Z"></path></svg>
            </div>
        </div>

        <table class="w-full">
            <thead class="w-full">
                <tr class="w-full bg-[#F6F9FC]">
                    <th class="text-start text-siga-10 p-3">HOŔARIO</th>
                    <th class="text-center text-siga-10 p-3">SEGUNDA</th>
                    <th class="text-center text-siga-10 p-3">TERÇA</th>
                    <th class="text-center text-siga-10 p-3">QUARTA</th>
                    <th class="text-center text-siga-10 p-3">QUINTA</th>
                    <th class="text-center text-siga-10 p-3">SEXTA</th>
                    <th class="text-center text-siga-10 p-3">SÁBADO</th>
                </tr>
            </thead>
            <tbody class="bg-white">
                <tr>
                    <td class="text-start p-4">07:40 - 08:30</td>
                    <td class="text-center p-4">P. Design</td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4">Inglês</td>
                    <td class="text-center p-4"></td>
                </tr>
                <tr class="border-t border-[#b7b7b7]">
                    <td class="text-start p-4">08:30 - 09:20</td>
                    <td class="text-center p-4">P. Design</td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4">Inglês</td>
                    <td class="text-center p-4"></td>
                </tr>
                <tr class="border-t border-[#b7b7b7]">
                    <td class="text-start p-4">09:30 - 10:20</td>
                    <td class="text-center p-4">P. Design</td>
                    <td class="text-center p-4">E. Dados</td>
                    <td class="text-center p-4">PPSI</td>
                    <td class="text-center p-4">Redes</td>
                    <td class="text-center p-4">Matemática</td>
                    <td class="text-center p-4"></td>
                </tr>
                <tr class="border-t border-[#b7b7b7] h-8 bg-white">
                    <td class="text-start p-4"></td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4"></td>
                    <td class="text-center p-4"></td>
                </tr>
            </tbody>
        </table>
    </section>

    <CalendarComponent />
</template>

