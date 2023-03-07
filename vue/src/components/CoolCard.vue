<template>
  <div>
    <h1>{{ name }}</h1>
    <p>testing</p>
  </div>
</template>

<script>
export default {
  name: "CoolCard",
  props: {
    name: String,
  },
};
</script>
