<script>
export default {
  data() {
    return {
        text: '',
        text2: '',
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
        <hr>
        <p>t1: {{text}}, t2 {{text2}}</p>
    </div>
</template>



<style>

</style>