<template>
  
</template>

<script>
import Vue from 'vue';
import VueAxios from 'vue-axios';
import axios from 'axios';
Vue.use(VueAxios,axios)
export default {
data(){
    return {
        list:undefined
    }
},
mounted(){
Vue.axios.get()
}

}
</script>

<style>

</style>