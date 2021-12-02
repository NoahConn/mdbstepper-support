<template>
  <MDBContainer class="my-3">
    <MDBRow class="g-3">
      <MDBCol md="3">
        <Input 
          label='Given Name' 
          type="text"
          id="Patient.name.given"
          pattern="^[A-Za-z]{1,12}$"
        />
      </MDBCol>
      <MDBCol md="6">
        <Input 
          label='Family Name' 
          type="text"
          id="Patient.name.family"
          pattern="[A-Za-z]{1,20}$"
        />
      </MDBCol>
      <MDBCol md="3">
        <Input 
          label='Suffix' 
          type="text"
          id="Patient.name.suffix"
          pattern="[A-Za-z]{1,20}$"
        />
      </MDBCol>
      <MDBCol md="12">
        <Select 
          label='Name Use'
          id="Patient.name.use"
          :optionsProp="nameUseOptions"
        />
      </MDBCol>
      
      <DatePeriod
        id="Patient.name.period"
      />
    </MDBRow>
    <hr class="my-4">
  </MDBContainer>
</template>

<script>
import Input from '@/components/MDBFormComponents/Input.vue'
import Select from '@/components/MDBFormComponents/Select.vue'
import DatePeriod from '@/components/MDBFormComponents/DatePeriod.vue'
import { 
  MDBContainer,
  MDBRow,  
  MDBCol, 
  MDBBtn 
} from 'mdb-vue-ui-kit'
export default {
  components: {
   Input, 
   Select,
   DatePeriod,
   MDBContainer,
   MDBRow,
   MDBCol,
   MDBBtn 
  },
  setup(){

    const nameUseOptions = [
      {text: 'Usual', value: 'usual'},
      {text: 'Official', value: 'official'},
      {text: 'Temp', value: 'temp'},
      {text: 'Nickname', value: 'nickname'},
      {text: 'Anonymous', value: 'anonymous'},
      {text: 'Old', value: 'old'},
      {text: 'Usual', value: 'usual'},
    ]

    return { 
      nameUseOptions
    }
  }
}
</script>

<style>

</style>