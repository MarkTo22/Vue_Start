<template>
    <div>
       <!--引用子组件-->
       <app-server v-for="server in servers" :server="server"></app-server>
    </div>
</template>

<script>
    import Server from './Server.vue'
    export default {
        data(){
            return {
                servers:[
                    {id:1,status:'Small'},
                    {id:2,status:'Normal'},
                    {id:3,status:'Normal'},
                    {id:4,status:'Small'},
                    {id:5,status:'Normal'},
                ]
            }
        },
        components:{
            appServer:Server
        }
    }
</script>