<template>
  <MDBContainer class="my-3">
    <MDBRow class="g-3">
      <MDBCol md="6">
        <Input 
          label='Phone Number' 
          type="phone"
          id="Patient.telecom.phone.value"
        />
      </MDBCol>
      <MDBCol md="6">
        <Input 
          label='Phone Number Type' 
          type="text"
          id="Patient.telecom.phone.type"
          pattern="^[A-Za-z]{1,12}$"
        />
      </MDBCol>
      <MDBCol md="12">
        <Input 
          label='Email' 
          type="email"
          id="Patient.telecom.email"
        />
      </MDBCol>
    </MDBRow>
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

    return { 
      
    }
  }
}
</script>