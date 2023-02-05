<script setup>
import { ref } from 'vue';

defineProps({
    contacts: Array,
})
</script>

<template>
    <table class="border-collapse text-white w-full">
        <thead class="sticky top-0 bg-indigo-400 text-lg">
            <th class="px-4 py-2 border-slate-600">Sn.</th>
            <th class="px-4 py-2 border-slate-600">Name</th>
            <th class="px-4 py-2 border-slate-600">Phone Number</th>
        </thead>
        <tbody class="bottom bg-indigo-500 text-slate-300">
            <tr class="hover:bg-indigo-600 hover:text-slate-100 hover:cursor-pointer" v-for="(contact, index) in contacts">
                <td class="border border-slate-600 px-4 py-2 text-center text-base">{{ index + 1 }}</td>
                <td class="border border-slate-600 px-4 py-2 text-base">{{ contact.name }}</td>
                <td class="border border-slate-600 px-4 py-2 text-base text-center">{{ contact.number }}</td>
            </tr>
        </tbody>
    </table>
</template>