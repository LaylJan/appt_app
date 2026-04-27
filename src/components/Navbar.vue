<template>
  <div class="bg-white text-white shadow-lg">
    <div class="container mx-auto px-4 flex justify-between items-center h-20">
      <!-- Logo -->
      <div class="flex items-center space-x-3">
        <img src="../assets/logo.png" alt="Logo" class="w-28 h-auto" />
      </div>

      <!-- Navigation Links -->
      <div class="flex space-x-8 h-full">
        <a href="#" class="font-semibold text-black px-6 h-full flex items-center hover:bg-[#0E7490] hover:text-white transition duration-300">Home</a>
        <a href="#" class="font-semibold text-black px-6 h-full flex items-center hover:bg-[#0E7490] hover:text-white transition duration-300">About Us</a>
        <a href="#" class="font-semibold text-black px-6 h-full flex items-center hover:bg-[#0E7490] hover:text-white transition duration-300">Services</a>
        <a href="#" class="font-semibold text-black px-6 h-full flex items-center hover:bg-[#0E7490] hover:text-white transition duration-300">Contact</a>
      </div>

      <!-- Schedule Appointment Button -->
      <div class="h-full flex">
        <button
          @click="showScheduleModal = true"
          class="font-bold text-black px-6 h-full flex items-center hover:bg-[#0E7490] hover:text-white transition duration-300"
        >
          Set an Appointment
        </button>
        <schedule-modal
          v-if="showScheduleModal"
          @close="showScheduleModal = false"
        />
      </div>
    </div>
  </div>
</template>

<script>
  import ScheduleModal from "./scheduleModal.vue";

export default {
  name: "NavbarComponent",
  components: {
    ScheduleModal,
  },
  data() {
    return {
      showScheduleModal: false,
      doctors: [

      ],
    };
  },
};
</script>
