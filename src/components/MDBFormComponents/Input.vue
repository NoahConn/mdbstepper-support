<template>
  <MDBInput 
    v-model="input" 
    :label="label"
    :type="type"
    :pattern="pattern"
    :id="id"
    @change="handleChange"
    validationEvent='input'
    validFeedback='Valid'
  />
</template>

<script>
import { MDBInput } from 'mdb-vue-ui-kit'
import { ref } from '@vue/reactivity'
export default {
  components: {
    MDBInput
  }, 
  props: {
    label: String, 
    type: String,
    pattern: String, 
    id: String
  }, 
  setup(props){
    const input = ref('')

    const handleChange = () => {
      console.log(props.id + ' change')
    }

    return{
      input,
      handleChange
    }
  }
}
</script>
