<template>
    <div>
        <span @click="clicktest">{{msg}}</span>
    </div>
</template>
<script>
import axios from 'axios'
export default {
    data () {
        return {
            msg: '66666'
        }
    },
    methods: {
        clicktest () {
            //发起一个user请求，参数为给定的ID
            axios.get('/envtest/hello')
            .then( ({data}) => {
                alert(data)
            })
            .catch(function(error){
                console.log(error)
            });
 
        }
    }
}
</script>

