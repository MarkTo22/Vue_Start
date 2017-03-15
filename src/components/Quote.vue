<template>
    <div>
        <div class="title">
            <slot name="title"></slot>
        </div>
        <!--slot的name为content，只有父级中引用当前标签设置slot=content才会显示-->
        <div class="content">
            <slot name="content"></slot>
        </div>

        <!--默认slot会显示父级引用当前标签的其他内容:多个default会显示多个-->
        <!--<div class="default">
            <slot></slot>
        </div>-->
        <!--<div class="default-1">
            <slot></slot>
        </div>-->
        <div class="defaultSlot">
            <slot></slot>
        </div>

        <div class="SlotDefault">
            <slot name="subTitle">The subTitle</slot>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style>
     .title{
         color:red;
     }
     .content{
         color:green;
     }
</style>
