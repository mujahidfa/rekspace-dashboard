<template>
  <!-- Toggle Button -->
  <label :for="toggleId" class="flex items-center cursor-pointer">
    <!-- toggle -->
    <div class="relative">
      <!-- input -->
      <input
        :id="toggleId"
        type="checkbox"
        class="hidden"
        :checked="isChecked"
      />
      <!-- line -->
      <div
        class="toggle__line w-10 h-4 bg-gray-400 rounded-full shadow-inner"
      ></div>
      <!-- dot -->
      <div
        class="toggle__dot absolute w-6 h-6 bg-white rounded-full shadow inset-y-0 left-0"
      ></div>
    </div>
    <!-- label -->
    <div class="ml-3 text-gray-700 font-medium">{{ toggleLabel }}</div>
  </label>
</template>

<script>
export default {
  props: {
    isChecked: {
      type: Boolean,
      default: false,
    },
    toggleLabel: {
      type: String,
      default: '',
    },
    toggleId: {
      type: String,
      required: true,
    },
  },
}
</script>

<style scoped>
.toggle__dot {
  top: -0.25rem;
  left: -0.25rem;
  transition: all 0.3s ease-in-out;
}

input:checked ~ .toggle__dot {
  transform: translateX(100%);
  background-color: #48bb78;
}
</style>
