<template>
  <div>
   <h1>hELLO: {{ msg }} </h1>
   <datepicker v-model="state.date" name="dp"></datepicker>
  </div>
</template>



<script>
import Datetpicker from 'vuejs-datepicker';


export default {
  components: { Datetpicker },
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      state: {
        date: new Date(2021, 24, 10)
      }
    }
  }
}
</script>