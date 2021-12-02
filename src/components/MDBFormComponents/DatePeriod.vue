<template>
  <MDBCol col="6">
    <MDBDatepicker 
      v-model="startDate"
      label="Start Date"
      placeholder="YYYY-MM-DD"
      :id="startID"
      format="YYYY-MM-DD"
      @change="handleStartChange"
      @close="handleStartChange"
    /> 
  </MDBCol>
  <MDBCol col="6">
    <MDBDatepicker 
      v-model="endDate"
      label="End Date"
      placeholder="YYYY-MM-DD"
      :id="endID"
      format="YYYY-MM-DD"
      @change="handleEndChange"
      @close="handleEndChange"
    />
  </MDBCol>
</template>

<script>
import { MDBDatepicker, MDBCol } from 'mdb-vue-ui-kit'
import { ref } from '@vue/reactivity'
export default {
  components:{
    MDBDatepicker, 
    MDBCol
  }, 
  props:{
    id: String
  }, 
  setup(props) {

    const startDate = ref('')
    const endDate = ref('')

    const startID = props.id + '.start'
    const endID = props.id + '.end'

    const handleStartChange = () => {
      console.log(startID + ' change')
    }
    const handleEndChange = () => {
      console.log(endID + ' change')
    }

    return{
      startDate, endDate, startID, endID, 
      handleStartChange, handleEndChange,
    }
  }

}
</script>