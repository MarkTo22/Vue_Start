<template>
    <div>
        New.vue
        <button @click="counter++">Counter++</button>
        {{counter}}
    </div>
</template>

<script>
    export default {
        data(){
                return {
                counter:0
            }
        },
        // 生命周期
        destroyed(){
            console.log('destroyed');
        },
        deactivated(){
            console.log('deactivated');
        },
        activated(){
            console.log('activated');
        }    
    }
</script>