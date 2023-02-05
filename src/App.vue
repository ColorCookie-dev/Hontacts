<script setup>
import HelloWorld from './components/HelloWorld.vue'
import Navbar from './components/Navbar.vue'
import Hontacts from './components/Hontacts.vue'
import EditContact from './components/EditContact.vue'
import { ref } from 'vue';

const all_contacts = ref([
  { name: "Dummy Name", number: "1800-SUM-NUM" },
]);

function add_new_contact() {
  all_contacts.value.push({ name: "new contact", number: "1800-ANO-NUM" })
}
</script>

<template>
  <div class="h-screen max-h-screen w-full fixed flex flex-col">
    <Navbar v-bind:add_new_contact="add_new_contact" />
    <div class="flex-auto flex w-full flex-col overflow-y-hidden justify-between">
      <div class="flex-1 w-full overflow-scroll">
        <Hontacts v-bind:contacts="all_contacts" />
      </div>
      <div class="hidden px-4 py-2 text-lg h-1/2 w-full flex-shrink-0 bottom-0 bg-orange-500 text-white">
        <EditContact />
      </div>
    </div>
  </div>
</template>