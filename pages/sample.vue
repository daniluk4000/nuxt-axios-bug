<template>
  <div>

  </div>
</template>

<script>
    export default {
        name: "sample",
        async asyncData() {
            await new Promise((resolve) => {
                setTimeout(() => {
                    resolve();
                }, 1000)
            })
            return {}
        }
    }
</script>

<style scoped>

</style>
