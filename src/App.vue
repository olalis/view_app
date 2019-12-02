<template>
  <div>
    <div>
      <h1>Participants list</h1>
      <!---<ol v-if="text.length > 0">--->
        <li>John Doe</li>
        <li>Robin Hood</li>
        <li>Chuck Norris</li>
        <li :key="text" v-for="text in text">{{text}}</li>

      </ol>
    </div>

    <h3>New participant</h3>
    <form @submit.prevent="addNewParticipant()">
      <label>Firstname</label>
      <input type="text">
      <label>Lastname</label>
      <input type="text">
      <button>Add new participant</button>
    </form>
  </div>
</template>

<script>
  export default {
    data() {
      return {name:[]};
    },
    methods: {
      addNewParticipant() {
        this.name.push;
      }
    }
  };
</script>




<!---<template>
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

