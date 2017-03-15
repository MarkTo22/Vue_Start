<template>
    <div>
        <app-header></app-header>
        <app-servers></app-servers>
        <app-server-details></app-server-details>
        <app-footer></app-footer>
    </div>
</template>

<script>
    import Header from './components/Public/Header.vue'
    import Footer from './components/Public/Footer.vue'
    import Servers from './components/Server/Servers.vue'
    import ServerDetails from './components/Server/ServerDetails.vue'

    export default {
        components:{
            'appHeader':Header,
            'appFooter':Footer,
            'appServers':Servers,
            'appServerDetails':ServerDetails
        }
    }
</script>

<style>

</style>