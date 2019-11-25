<template>
  <div>
    <h1>Clicked {{ title }} times</h1>
    <button @click="iAmClicked()">More</button>
  </div>
</template>

<script>
  export default {
    data() {
      return {title: 0}
    },
    methods: {
      iAmClicked() {
        this.title = this.title + 1;
      }
    }
  };
</script>
