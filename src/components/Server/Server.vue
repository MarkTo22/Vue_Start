<template>
    <li @click="serverSelected">{{server.id}} {{server.status}}</li>
</template>

<script>
    import {serverBus} from '../../main'

    export default {
        props:['server'],
        methods:{
            serverSelected(){
                serverBus.$emit('serverSelected',this.server)
            }
        }
    }
</script>