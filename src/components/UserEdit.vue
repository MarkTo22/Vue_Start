<template>
    <div class="component">
        <h3>修改编辑用户信息</h3>
        <p>修改资料</p>
        <p>用户年龄:{{userAge}}</p>
        <button @click="editAge">修改年龄</button>
    </div>
</template>

<script>
    import {eventBus} from '../main'

    export default {
        props:['userAge'],
        methods:{
            editAge(){
                this.userAge = 40;
                //bus,移到bus总线里去定义了：main.js中
               //this.$emit('ageWasEdited',this.userAge)                
               //eventBus.$emit('ageWasEdited',this.userAge)
               eventBus.changeAge(this.userAge);
            }
        }
    }
</script>

<style scoped>
    div{
        background:green;
    }
</style>