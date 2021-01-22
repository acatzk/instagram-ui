<template>
  <div class="bg-gray-100 text-gray-900 leading-tight">
    <TheNavBar />
    <main>
      <Nuxt />
    </main>
  </div>
</template>

<script>
  export default {
    components: {
      TheNavBar: () => import('~/components/TheNavBar')
    }
  }
</script>