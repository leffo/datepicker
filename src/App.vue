<template>
  <div>
   <h1>hELLO: {{ state.date }} </h1>
   <datepicker 
    :v-model="state.date" 
    name="dp"
    :language="'ru'"
    :typeable="true"
    format="dd.MM.yyyy"
    >
    </datepicker>
  </div>
</template>



<script>
import Datepicker from 'vuejs-datepicker';
import {ru} from 'vuejs-datepicker/dist/locale';


export default {
  components: { Datepicker },
  name: 'app',
  data () {
    return {
      ru: ru,
      msg: 'Welcome to Your Vue.js App',
      state: {
        date: new Date(2021, 24, 10),
      }
    }
  }
}
</script>