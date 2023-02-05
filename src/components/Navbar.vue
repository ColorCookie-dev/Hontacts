<script setup>
defineProps({
    add_new_contact: Function,
}) 
</script>

<template>
    <div class="flex justify-between bg-green-700 px-4 py-2 tracking-widest text-white">
        <h1 class="left text-4xl font-bold font-sans">
            Hontacts
        </h1>
        <div class="right">
            <button class="text-base bg-red-500 hover:bg-red-600 rounded-md py-2 px-4" @click="add_new_contact">Add New Contact</button>
        </div>
    </div>
</template>