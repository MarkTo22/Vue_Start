<template>
    <div class="component">
        <h3>查看用户详情</h3>
        <p>用户详情</p>
        <p>用户姓名：{{myName}}</p>
        <p>反转姓名：{{ switchName() }}</p>
        <!--<button @click="resetName">重置姓名</button> -->
        <button @click="resetName">重置姓名</button>
    </div>
</template>

<script>
    export default {
        // props:['myName'],
        props:{
            myName:{
                type:[String,Number],//type:String,
                required:false,
                default:'默认姓名'
            }
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
        }
    }
</script>

<style scoped>
    div{
        background:gray;
    }
</style>