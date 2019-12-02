<template>
  <div>
    <ul v-if="numbers.length > 0 && numbers.length <10">
      <li :key="number" v-for="number in numbers">{{ number }}</li>
    </ul>
    <button @click="addNew()">Add new random number</button>
  </div>
</template>

<script>
  export default {
    data() {
      return {numbers: []}
    },
    methods: {
      addNew() {
        this.numbers.push(Math.round(Math.random() * 100));
      }
    }
  };
</script>

