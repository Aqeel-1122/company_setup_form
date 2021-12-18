<template>
  <div class="wrap">
    <b-container>
      <div class="title col-md-12 mt-3">
        <h3 class="text-center fw-600">
          <b-icon icon="file-text" aria-hidden="true" class="title-icon"></b-icon>
          Company Setup
        </h3>
      </div>
      <b-form @submit.prevent="setupFormSubmit" class="col-md-6 mx-auto company-setup-form px-5 py-3 mb-5">  
        
        <b-form-group id="select-group-type" label="Type:" label-for="typeSelected">
          <b-form-select  id="select-type" v-model="companyName" :options="options" required></b-form-select>
        </b-form-group>

        <b-form-group id="input-group-company-name" label="Company Name: " label-for="input-company-name">
          <b-form-input  class="mt-2" id="input-company-name"></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-company-branch-code" label="Branch Code: " label-for="input-company-branch-code">
          <b-form-input  class="mt-2" id="input-company-branch-code"></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-company-branch-name" label="Branch Name:" label-for="input-company-branch-name">
          <b-form-input disabled class="mt-2" id="input-company-branch-name"></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-company-customer" label="Customer Number" label-for="input-company-customer">
          <b-form-input  class="mt-2" id="input-company-customer"></b-form-input>
        </b-form-group>

        <b-form-group id="select-group-type" label="Debit Account Number: " label-for="typeSelected">
          <b-form-select  id="select-type" v-model="companyName" :options="options" required> </b-form-select>
        </b-form-group>

        <b-form-group id="input-group-company-name" label="Customer category:" label-for="input-company-name">
          <b-form-input disabled class="mt-2" id="input-company-name"></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-company-name" label="Account Title" label-for="input-company-name">
          <b-form-input disabled class="mt-2"  id="input-company-name"></b-form-input>
        </b-form-group>
        
       <div class="app">
        <b-button class="submitbtn" type="submit">submit</b-button>
        <b-button class="resetbtn" type="reset">Reset</b-button>
        
       </div>

      </b-form>
    </b-container>
  </div>
</template>

<script>
export default {
name:'CompanySetupForm',
data(){
  return{
    companyName:null,

    options:[ {
      value:null ,text:'please select a type'
      }, 
      
      {
        text:'Bulk Credit'
      },
      {
        text: "Pensioner"
      },
    ],

  }
}
}
</script>

<style>

.wrap {
overflow: hidden;
position: relative;
text-align: left;

}
 
.title {
  display: inline-flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  vertical-align: middle;
  padding-top: 2px;
  padding-bottom: 2px;
 
}

.title h3 {
  color: #15804f;
  position: relative;
  
}

.company-setup-form {
  background-color: #15804f;
  color: #fff;
  padding: 10px;
  box-shadow: rgb(0 0 0 / 35%) 0px 5px 15px;
  border-radius: 10px;
  font-weight: bol;
}

.company-setup-form select {
  border: solid 1px #fbb040 !important;
  border-radius: 10px;
}

.company-setup-form input {
  border: solid 1px #fbb040 !important;
  border-radius: 10px;
  
}

.company-setup-form input:focus {
  border-color: #fbb040 !important;
  
}

.company-setup-form select:focus {
  border-color: #fbb040 !important;
}
.company-setup-form .submitbtn{
  background: red;
}
</style>