<template>
  <MDBContainer class="my-3">
    <MDBRow class="g-3">
      <MDBCol md="12">
        <Input 
          label='Address Line 1' 
          type="text"
          id="Patient.address.lineOne"
          pattern="[\s\S]*"
        />
      </MDBCol>
      <MDBCol md="12">
        <Input 
          label='Address Line 2' 
          type="text"
          id="Patient.address.lineTwo"
          pattern="[\s\S]*"
        />
      </MDBCol>
      <MDBCol md="6">
        <Input 
          label='City' 
          type="text"
          id="Patient.address.city"
          pattern="[\s\S]*"
        />
      </MDBCol>
      <MDBCol md="6">
        <Input 
          label='State' 
          type="text"
          id="Patient.address.state"
          pattern="[\s\S]*"
        />
      </MDBCol>
      <MDBCol md="6">
        <Input 
          label='Postal Code' 
          type="text"
          id="Patient.address.postalCode"
          pattern="[\s\S]*"
        />
      </MDBCol>
      <MDBCol md="6">
        <Input 
          label='Country' 
          type="text"
          id="Patient.address.country"
          pattern="[\s\S]*"
        />
      </MDBCol>
      <DatePeriod
        id="Patient.address.period"
      />
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
} from 'mdb-vue-ui-kit'
export default {
  components: {
   Input, 
   Select,
   DatePeriod,
   MDBContainer,
   MDBRow,
   MDBCol,
  }
}
</script>
