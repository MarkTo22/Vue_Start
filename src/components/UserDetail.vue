<template>
    <div class="component">
        <h3>查看用户详情</h3>
        <p>用户详情</p>
        <p>用户姓名：{{myName}}</p>
        <p>反转姓名：{{ switchName() }}</p>
        <p>用户年龄：{{userAge}}</p>
        <!--<button @click="resetName">重置姓名</button> -->
        <button @click="resetName">重置姓名</button>
    </div>
</template>

<script>
    import {eventBus} from '../main'
    export default {
        // props:['myName'],
        props:{
            myName:{
                type:[String,Number],//type:String,
                required:false,
                default:'默认姓名'
            },
            userAge:Number
            // ,
            // childrenRequest:{
            //     type:Function
            // }
        },
        methods:{
            switchName(){
                return this.myName.split('').reverse().join('');
            },
            resetName(){
                //this.childrenRequest('MarkTo--reset');
                this.myName="MarkTo--reset";
                this.$emit('nameWasReset',this.myName);
            }
        },
        //生命周期
        created(){
            eventBus.$on('ageWasEdited',(age)=>{
                this.userAge = age;
            })
        },
        
    }
</script>

<style scoped>
    div{
        background:gray;
    }
</style>