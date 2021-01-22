<template>
  <div class="flex items-center justify-between py-2">
    <div class="flex items-center space-x-2">
      <div class="flex-shrink-0">
        <a href="#">
          <img class="w-8 h-8 rounded-full border" :src="user.avatar" alt="avatar">
        </a>
      </div>
      <div class="flex flex-col">
        <a href="#" class="text-sm font-semibold">{{ user.username }}</a>
        <span class="text-xs text-gray-400">{{ user.description }}</span>
      </div>
    </div>
    <a href="#" class="text-xs font-medium text-blue-500">Follow</a>
  </div>
</template>

<script>
  export default {
    props: {
      user: {
        type: Object,
        required: true
      }
    }
  }
</script>