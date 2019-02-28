# vue

### 指令

`指令的职责是，当表达式的值改变时，将其产生的连带影响，响应式地作用于 DOM。`

Vue.js 为 `v-bind` 和 `v-on` 这两个最常用的指令，提供了特定简写：

1. v-bind:href="url"   :href=""
2. v-on:click=""  @click=""

| 指令       |                                        |
| ---------- | -------------------------------------- |
| v-bind     | 1.绑定属性v-bind:tite="msg" 2.组件传值 |
| v-if       |                                        |
| V-else     |                                        |
| v-show     | Display:none                           |
| v-on:click |                                        |
| v-once     | 一次性的插值                           |
| v-html     | v-html="html"                          |
| v-text     | {{}}                                   |
|            |                                        |

### 修饰符

- `.prevent` 

  ```html
  <form v-on:submit.prevent="onSubmit"></form>
  <!--event.preventDefault()-->
  ```

- `.native`给组件绑定原生事件时使用

  ```html
  <!-- 会触发原生事件 -->
  <child @click.native="handleClick"></child>
  ```


### is属性

tbody下只能显示tr，用tr代替组件时，使用is

### 组件中的data应该定义为一个函数

```javascript
Vue.component('row', {
    data: function() {
        return {
            content: 'this is'
        }
    }
})
```

### ref

ref可以拿到DOM的引用

```javascript
// <div ref="hello></div>
this.$refs.hello
```

### Vue.set方法

既是一个全局方法，也是一个实例方法

可以向对象和数组添加数据，页面发生改变