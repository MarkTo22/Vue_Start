this is for Vue-component-communication!

content:
    1. A componentized UI layout, cover contains UserDetail and UserEdit under User group
Need to transfer data from the User the parent component to the child components, through property transfer in the form of: prop = "data", need to receive in UserDetail child component properties, need through the props: [' prop] to receive property, expression for display by interpolation operation;
2. Properties in our children, we can go to the operation and the use of passed attribute values, if you are using?And we are of the same model of traditional methods such as direct use enclosing propsName invoked in function or other places;
3. The binding on the attribute value for operation, such as can constraint data types, whether must pass and the default operation;
4.1 transfer data from the child component to the parent component, one of the ways and the react, adopt the way of the callback function to solve;
4.2 pass events way from child components for data transfer to the parent component, child components by $emit submit event, in the parent component events by @ receiving components, and use the $event to receive parameters;
4.3 called Bus Bus way, in the main, js define an eventBus Bus, then carries on the Bus in the edit $emit commits, and then through the eventBus Bus events to monitor, and the listening is in the detail information for listening, listening to the data changes or trigger later we will call event data change accordingly;
4.4 the eventBus bus vue instance object, you can build the corresponding method, so, in the child components only needs simple call.

内容：
1.布局一个组件化的UI界面，涵盖User组下包含UserDetail和UserEdit
需要从User父组件中向子组件传递数据，通过属性方式进行传递，:prop="data"，需要在UserDetail子组件进行属性的接收，需要通过props:['prop']去接收属性，通过插值表达式进行显示操作；
2.属性在我们子组件里了，我们可以去操作与使用传递过来的属性值，如果使用呢？和我们传统方法等模式一致，直接利用this.propsName在function或者其它地方进行调用；
3.对属性值进行约束性操作，比如可以约束数据的类型、是否必须传递以及默认值等操作；
4.1 从子组件传递数据到父组件中，其中一种方式和react一致，采用回调函数的方式进行解决；
4.2 传递事件方式从子组件向父组件里进行数据的传递，子组件通过$emit提交事件，父组件中通过@接收组件事件，并且利用$event进行参数接收；
4.3 叫Bus总线的方式，在main.js定义一个eventBus的总线，然后在edit里进行总线的$emit提交，然后通过eventBus总线进行事件的监听，而这个监听是在detail详情里面进行监听，监听到数据变化或者叫事件的触发以后我们就进行相应数据的修改；
4.4 在eventBus总线的vue实例对象中，可以构建相应的方法，那么，在子组件中只需要进行简单的调用就可以了。



# mypro

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

For detailed explanation on how things work, consult the [docs for vue-loader](http://vuejs.github.io/vue-loader).

