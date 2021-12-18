<template>
 <div class=" main container col-lg-12">
        <div class="d-flex justify-content-center align-items-center">
          <b-icon icon="grid3x3-gap-fill" scale="3" variant="success"></b-icon>
          <h1 class="CompanyRecord">&nbsp;&nbsp;Company Records</h1>
        </div>
        <b-table 
          :fields="fields" class="table" :items="items" responsive="xl" >
        </b-table>
    </div>
</template>

<script>
export default {
name:'DynamicTable',
data(){
    return{
        fields:[
             'SetupType',
             'CompanyName',
             'BranchCode',
             'BranchName',
             'CustomerNumber',
             'DebitAccount',
             'AccountTitle',
             'Customer Category',
             'Auth Status',
             'Active',
             'Remarks',  
        ]
    }
}
}
</script>

<style>
.table
{
    background-color: rgb(0, 149, 0);
    font-weight: bold;
}
.main
{
    border-left: 10px rgb(47, 122, 10)  solid;
    border-right:10px rgb(47, 122, 10) solid;
    border-top:10px rgb(255, 145, 0)solid;
    border-bottom:10px rgb(255, 145, 0) solid; 
    border-radius: 10px;
    background-color: rgb(231, 218, 218);
}
.CompanyRecord{
    text-align: center;
    color:rgb(47, 122, 10);
    padding-top: 5px;
    font-size: 40px;
   font-weight: bold;
   padding-top: 10px;


}

</style>