### reactive和ref

**注意区别开ref函数与模板ref，ref函数用来声明响应式数据，相当于组合api中的data，模板ref可以用来让父组件获取子组件属性**

在选项api中我们通过data的返回值来实现响应式数据，而在组合api中我们使用reactive和ref

两个函数都用与定义响应式数据。

引用类型用reactive，基本类型用ref

[Vue3 Composition API: 对比ref和reactive](https://zhuanlan.zhihu.com/p/267967246)



### 模板ref

与ref函数不同，模板ref作用于标签上，是一个属性。我们可以用ref属性来获取dom元素。

使用了 `<script setup>` 的组件是**默认私有**的：一个父组件无法访问到一个使用了 `<script setup>` 的子组件中的任何东西，除非子组件在其中通过 `defineExpose` 宏显式暴露，这样就能让父组件获取到子组件的属性了。



### defineProps

在选项api中我们使用props属性来传递prop，在组合api中我们使用