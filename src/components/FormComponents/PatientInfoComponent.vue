<template>
  <MDBContainer class="my-3">

    <MDBRow class="g-3">
      <MDBCol md="4">
        <DatePicker 
          label='Date of Birth' 
          id="Patient.birthDate"
        />
      </MDBCol>
      <MDBCol md="4">
        <MultipleSelect
          label='Language' 
          id="Patient.communication.language"
          :options="langaugeOptions"
        />
      </MDBCol>
      <MDBCol md="4">
        <!-- Add auto fill -->
        <Select 
          label='Race' 
          id="Patient.extension:race"
          :optionsProp="raceOptions"
        />
      </MDBCol>
      <MDBCol md="6">
        <Select 
          label='Ethnicity' 
          id="Patient.extension:ethnicity"
          :optionsProp="ethnicityOptions"
        />
      </MDBCol>
      <MDBCol md="6">
        <Select 
          label='Gender Identity' 
          id="Patient.genderIdentity"
          :optionsProp="genderIdentityOptions"
        />
      </MDBCol>
      <MDBCol md="6">
        <Select 
          label='Birth Sex' 
          id="Patient.extension:birthsex"
          :optionsProp="birthSexOptions"
        />
      </MDBCol>
      <MDBCol md="6">
        <Select 
          label='Sexual Orientation' 
          id="Patient.sexualOrientation"
          :optionsProp="sexualOrientationOptions"
        />
      </MDBCol>
    </MDBRow>

  </MDBContainer>
</template>

<script>
import Input from '@/components/MDBFormComponents/Input.vue'
import Select from '@/components/MDBFormComponents/Select.vue'
import MultipleSelect from '@/components/MDBFormComponents/MultipleSelect.vue'
import DatePicker from '@/components/MDBFormComponents/DatePicker.vue'
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
   MultipleSelect,
   DatePicker,
   DatePeriod,
   MDBContainer,
   MDBRow,
   MDBCol,
   MDBBtn 
  },
  setup(){

    const genderIdentityOptions = [
      {text: 'Male', value: '446151000124109'},
      {text: 'Female', value: '446141000124107'},
      {text: 'Female-to-Male', value: '407377005'},
      {text: 'Male-to-Female', value: '407376001'},
      {text: 'Genderqueeer', value: '446131000124102'},
      {text: 'Other', value: 'OTH'},
      {text: 'Choose not to disclose', value: 'ASKU'}
    ]

    const birthSexOptions = [
      {text: 'Male', value: 'M'},
      {text: 'Female', value: 'F'},
      {text: 'Unknown', value: 'UNK'}
    ]

    const sexualOrientationOptions = [
      {text: 'Lesbian, gay or homosexual', value: '38628009'}, 
      {text: 'Straight or heterosexual', value: '20430005'}, 
      {text: 'Bisexual', value: '42035005'}, 
      {text: 'Something else, please describe', value: 'OTH'}, 
      {text: 'Dont know', value: 'UNK'}, 
      {text: 'Choose not to disclose', value: 'ASKU'} 
    ]

    const raceOptions = [
      {text: 'Hispanic or Latino', value: '2135-2'},
      {text: 'Not Hispanic or Latino', value: '2186-5'}
    ]

    const ethnicityOptions = [
      {text: 'American Indian or Alaska Native', value: '1002-5'},
      {text: 'Asian', value: '2028-9'},
      {text: 'Black or African American', value: '2054-5'},
      {text: 'Native Hawaiian or Other Pacific Islander', value: '2076-8'},
      {text: 'Other Race', value: '2131-1'},
      {text: 'White', value: '2106-3'}
    ]

    const langaugeOptions = [
      {text: 'Arabic', value: 'ar'},	
      {text: 'Bengali', value: 'bn'},	
      {text: 'Czech', value: 'cs'},	
      {text: 'Danish', value: 'da'},	
      {text: 'German', value: 'de'},	
      {text: 'Greek', value: 'el'},	
      {text: 'English', value: 'en'},	
      {text: 'Spanish', value: 'es'},	
      {text: 'Finnish', value: 'fi'},	
      {text: 'French', value: 'fr'},	
      {text: 'Frysian', value: 'fy'},	
      {text: 'Hindi', value: 'hi'},	
      {text: 'Croatian', value: 'hr'},	
      {text: 'Italian', value: 'it'},	
      {text: 'Japanese', value: 'ja'},	
      {text: 'Korean', value: 'ko'},	
      {text: 'Dutch', value: 'nl'},	
      {text: 'Norwegian', value: 'no'},	
      {text: 'Punjabi', value: 'pa'},	
      {text: 'Polish', value: 'pl'},	
      {text: 'Portuguese', value: 'pt'},	
      {text: 'Russian', value: 'ru'},	
      {text: 'Serbian', value: 'sr'},	
      {text: 'Swedish', value: 'sv'},	
      {text: 'Telegu', value: 'te'},	
      {text: 'Chinese', value: 'zh'}
    ]

    return { 
      genderIdentityOptions,
      birthSexOptions,
      sexualOrientationOptions,
      raceOptions,
      ethnicityOptions, 
      langaugeOptions
    }
  }
}
</script>

<style>

</style>