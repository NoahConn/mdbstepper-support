<template>

  <MDBContainer >
    <MDBStepper vertical class="my-3 py-5">

      <MDBStepperStep active >
        <MDBStepperHead icon="1">
          Patient Information
        </MDBStepperHead>
        <MDBStepperContent>
          <PatientInfoComponent />
        </MDBStepperContent>
      </MDBStepperStep>

      <MDBStepperStep active>
        <MDBStepperHead icon="2">
          Name
        </MDBStepperHead>
        <MDBStepperContent :key="newName">
          <NameComponent v-for="name in names" :key="name" />
          <div class="container d-flex justify-content-end">
            <MDBBtn @click="addName">
              Add name
            </MDBBtn>
          </div>
        </MDBStepperContent>
      </MDBStepperStep>

      <MDBStepperStep active>
        <MDBStepperHead icon="3">
          Address
        </MDBStepperHead>
        <MDBStepperContent class="m-auto">
          <AddressComponent />
        </MDBStepperContent>
      </MDBStepperStep>

      <MDBStepperStep active>
        <MDBStepperHead icon="4">
          Contact Information
        </MDBStepperHead>
        <MDBStepperContent>
          <TelecomComponent />
          <div class="container d-flex justify-content-center">
            <MDBBtn @click="submitForm">
              Submit
            </MDBBtn>
          </div>
        </MDBStepperContent>
      </MDBStepperStep>

    </MDBStepper>
  </MDBContainer>

</template>

<script>
import PatientInfoComponent from '@/components/FormComponents/PatientInfoComponent.vue'
import NameComponent from '@/components/FormComponents/NameComponent.vue'
import AddressComponent from '@/components/FormComponents/AddressComponent.vue'
import TelecomComponent from '@/components/FormComponents/TelecomComponent.vue'
import { 
  MDBStepper, 
  MDBStepperStep, 
  MDBStepperHead, 
  MDBStepperContent, 
  MDBContainer, 
  MDBBtn, 
  MDBIcon
} from 'mdb-vue-ui-kit'
import { ref } from '@vue/reactivity'
export default {
  components: {
    PatientInfoComponent,
    NameComponent,
    AddressComponent, 
    TelecomComponent,
    MDBStepper, 
    MDBStepperStep, 
    MDBStepperHead, 
    MDBStepperContent, 
    MDBContainer, 
    MDBBtn, 
    MDBIcon
  },
  setup(){
  
    const newName = ref(0)
    const forceRerender = () => {
      newName.value += 1
    }
    const names = ref([1])
    const addName = () => {
      let length = names.value.length
      let lastIndex = names.value[length - 1]
      names.value.push(lastIndex + 1)
      forceRerender()
    }
    const submitForm = () => {
      console.log('submitted')
    }

    return {  
      names, addName, submitForm,
      newName
    }
  }
}
</script>

