<template>
  <svg
    v-html="icon"
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 24 24"
    width="24"
    height="24"
  ></svg>
</template>

<script lang="ts">
export default {
    name: "Icon",
    props: {
        icon: String,
    }
}
</script>