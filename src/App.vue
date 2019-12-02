<template>
  <div>
    <!---<h1>Clicked {{ title }} times</h1>
    <button @click="iAmClicked()">More</button>
    <button @click="startover()">Start over</button>--->

    <h1>{{happy ? 'Happy :)' : 'Sad :('}}</h1>
    <button @click="changemood()">Click me!</button>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        happy :false
      }
      return {title: 0}
    },
    methods: {
      iAmClicked() {
        this.title = this.title + 1;
      },
      startover(){
        this.title = 0;
      },
      changemood(){
        this.happy = !this.happy;
      }
    }
  };
</script>
