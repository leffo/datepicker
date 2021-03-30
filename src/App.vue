<template>
  <div>
   <h1>Hello: {{ state.date }} </h1>
   <datepicker
     v-model="state.date"

    name="dp"
    :language="ru"
    :typeable="true"
    format="dd.MM.yyyy"
    :open-date="state.date"
    >
    </datepicker>
    <date-picker-vue2
      v-model="time1"
      valueType="DD.MM.YYYY"
      :time-title-format="'DD.MM.YYYY'"
    ></date-picker-vue2>
  </div>
</template>



<script>
import Datepicker from 'vuejs-datepicker';
import ru from "vuejs-datepicker/dist/locale/translations/ru";
import DatePickerVue2 from 'vue2-datepicker';
import 'vue2-datepicker/index.css';

export default {
  components: { Datepicker, DatePickerVue2 },
  name: 'app',
  data () {
    return {
      ru: ru,
      msg: 'Welcome to Your Vue.js App',
      state: {
        // month 0...11
        date: new Date(2021, 9, 24),
      },
      time1: '24.10.1966',
    }
  }
}
</script>
