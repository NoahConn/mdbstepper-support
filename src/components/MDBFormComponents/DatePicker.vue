<template>
  <MDBDatepicker 
    v-model="date"
    :label="label"
    :id="id"
    format="YYYY-MM-DD"
    @change="handleChange"
    @close="handleChange"
  />
</template>

<script>
import { MDBDatepicker } from 'mdb-vue-ui-kit'
import { ref } from '@vue/reactivity'
export default {
  components:{
    MDBDatepicker
  }, 
  props:{
    label: String,
    id: String
  }, 
  setup(props) {
    
    const date = ref('')
    
    const handleChange = () => {
      console.log(props.id + ' change')
    }

    return{
      date, 
      handleChange 
    }
  }

}
</script>