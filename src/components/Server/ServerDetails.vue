<template>
    <div>
        <p v-if="!server">请选择一个server</p>
        <p v-else>
            server #{{server.id}} status:{{server.status}}
        </p>
        <button @click="resetStatus">change to normal</button>
    </div>
</template>


<script>
    import {serverBus} from '../../main'

    export default {
        data(){
            return {
                server:null
            }
        },
        methods:{
            resetStatus(){
                this.server.status = 'normal';
            }
        },
        created(){
            serverBus.$on('serverSelected',(server)=>{
                this.server = server;
            })
        }
    }
</script>