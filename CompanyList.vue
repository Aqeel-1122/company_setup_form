<template> 
    <div class="main container col-md-12 ">
    <b-table
     class="table"
      :items="items"
      :fields="fields"
      responsive="xl"
    >
      <template   #thead-top="">
        <b-tr  variant="info">
          <b-th class="tablehead">ID</b-th>
          <b-th class="tablehead">Caller ID</b-th>
          <b-th class="tablehead">Order </b-th>
          <b-th class="tablehead" >Branch Name</b-th>
          <b-th class="tablehead">Customer Number</b-th>
          <b-th class="tablehead">Debit Account</b-th>
          <b-th class="tablehead">Account Title</b-th>
          <b-th class="tablehead">Customer Category</b-th>
          <b-th class="tablehead">Auth Status</b-th>
          <b-th class="tablehead">Active</b-th>
          <b-th class="tablehead">Remarks</b-th>
          
        </b-tr>
      </template>
    </b-table>
 
  </div>
</template>
<script>
export default {
  name:'CompanyList',
  data(){
    return{
      items:[],
      fields:[
        ' '
      ]
    }
  }
}
</script>
<style>

.table .tablehead
{
 border: rgb(77, 190, 77);
 border-right: 1px solid rgb(77, 190, 77) ;
 border-collapse: collapse;
}
.main
{
  background-color:rgb(77, 190, 77);
  margin-top: 100px;
  border-top: 10px solid rgb(255, 217, 0);
   border-bottom: 10px solid rgb(240, 239, 234);
   border-left:10px solid rgb(77, 190, 77);
   border-right:10px rgb(77, 190, 77);
   border-radius: 10px; 
}
.table{
  margin-top: 10px;
}
</style>