<template>
  <MDBSelect multiple filter
    v-model:options="options"
    v-model:selected="selected" 
    :label="label"
    :id="id"
    :preselect="preselect"
    @change="handleChange"
  />
</template>

<script>
import { MDBSelect } from 'mdb-vue-ui-kit'
import { ref } from '@vue/reactivity'
export default {
  components: {
    MDBSelect
  }, 
  props: {
    label: String, 
    id: String, 
    optionsProp: Array
  }, 
  setup(props){

    const selected = ref('');
    const options = ref(props.optionsProp)

    const handleChange = () => {
      console.log(props.id + ' change')
    }

    const preselect = ref(false)

    return{
      selected, options, preselect,
      handleChange, 
    }
  }
}
</script>
