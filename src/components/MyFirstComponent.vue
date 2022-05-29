<script>

import axios from 'axios';


export default {
  data() {
    return {
        text: '',
        text2: '',
        apiReturn: '',
        countdown: 0,
    }
  },
  methods: {
      apiTest() {
          console.log("apiTest called");
          let returnValue = 'nothing yet';
          //doStuff

          axios
            .get('http://localhost/helloApi.php')
            .then(
                response => (this.apiReturn = JSON.stringify(response.data))
            )
      }
  }
}
</script>


<template>
    <h1>My First Component!</h1>

    <div>
        <input
            :value="text"
            @input="event => text = event.target.value">

        <br>
        <input v-model="text2">
        <p>t1: {{text}}, t2 {{text2}}</p>
    </div>
    <hr>
    <div>
        <button @click="apiTest()">apiTest</button>
        <p>Return data: {{apiReturn}}</p>
    </div>
    <hr>
    <div>
        <h2>some spinning</h2>
        <button @click="countdown=1">Start Spinning</button>
        <button @click="countdown=0">Stop Spinning</button>
        <p>{{countdown}}</p>
        <b-spinner label="Spinning" v-if="countdown"></b-spinner>
    </div>
</template>



<style>

</style>