<template>
    <div class="component">
        <h1>用户组件</h1>
        <p>我是一个用户</p>
        <p>姓名：{{name}}</p>
        <p>年龄：{{age}}</p>
        <button @click="changeName">修改姓名</button>
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-6">
                <!--<app-user-detail :myName="name" :childrenRequest="letParentResponse"></app-user-detail>-->
                <app-user-detail :myName="name" 
                :userAge="age"
                @nameWasReset="name = $event"></app-user-detail>
            </div>
            <div class="col-xs-12 col-sm-6">
                <app-user-edit :userAge="age" @ageWasEdited="age = $event"></app-user-edit>
            </div>
        </div>
    </div>

</template>

<script>
    import UserDetail from './UserDetail.vue'
    import UserEdit from './UserEdit.vue'

    export default {
        data(){
            return {
                name:'MarkTo',
                age:35
            }
        },
        methods:{
            changeName(){
                this.name = 'Hao'
            }
            // ,
            // letParentResponse(request){
            //     this.name = request;
            // }
        },
        components : {
            appUserDetail:UserDetail,
            appUserEdit:UserEdit
        }
    }
</script>