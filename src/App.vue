<template>
    <div class="container">
    <div class="row">
        <div class="col-xs-12">
            <!--组件的动态加载-选项卡切换-->
            
            <button @click="selectedComponent='appQuote'">Quote</button>
            <button @click="selectedComponent='appAuthor'">Author</button>
            <button @click="selectedComponent='appNew'">New</button>
            
            {{selectedComponent}}

            <!--选中的组件-->
            <component :is="selectedComponent">
                <p>Default content</p>
            </component>

            <!--<app-quote>
                <h1 slot="title">{{quoteTitle}}</h1>
                <p slot='content'>Quote content message</p>
                <p>是是是</p>
                <span>否否否</span>                
                <p slot="subTitle">这是父级的slot=subTitle</p>
            </app-quote>-->
        </div>
    </div>
    </div>
</template>

<script>
   import Quote from './components/Quote.vue'
   import Author from './components/Author.vue'
   import New from './components/New.vue'

   export default {
       data(){
           return {
               quoteTitle:'我是标题党',
               selectedComponent:"default-value"
           }
       },
       components:{
           appQuote:Quote,
           appAuthor:Author,
           appNew:New
       },
       methods:{

       }
   }
</script>

<style>

</style>