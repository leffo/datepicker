<template>
  <div>
   <h1>Hello: {{ state.date }} </h1>
   <datepicker
     v-model="state.date"
    :value="state.date"
    name="dp"
    :language="ru"
    :typeable="true"
    format="dd.MM.yyyy"
    :open-date="state.date"
    >
    </datepicker>
  </div>
</template>



<script>
import Datepicker from 'vuejs-datepicker';
import ru from "vuejs-datepicker/dist/locale/translations/ru";

export default {
  components: { Datepicker },
  name: 'app',
  data () {
    return {
      ru: ru,
      msg: 'Welcome to Your Vue.js App',
      state: {
        // month 0...11
        date: new Date(2021, 9, 24),
      }
    }
  }
}
</script>
