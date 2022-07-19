# Vue 学习

## 第一章 基础语法

### 1.1 基础模板

```vuevue
<!-- 开发环境版本，包含了有帮助的命令行警告 -->
<script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
<script>

    var app = new Vue({
        el: '#app',
        data: {
            message: 'Hello Vue!'
        }
    })
</script>
```

### 1.2 生命周期



### 1.3 计算属性



### 1.4 const

![image-20220719090047859](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719090047859.png)

### 1.5 属性的增强写法

![image-20220719091540139](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719091540139.png)

### 1.6 函数增强写法

![image-20220719091655095](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719091655095.png)

### 1.7 事件监听

![image-20220719092900822](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719092900822.png)

如果函数需要参数，但是没有传，就会使用默认值，undefined

![image-20220719093903777](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719093903777.png)

![image-20220719093943173](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719093943173.png)

![image-20220719094205599](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719094205599.png)

注意，在实参传值时候，如果不加' ',就是变量，那么就会去data当中找值

### 1.8 v-on的修饰符

.stop:阻止事件传递

![image-20220719094854715](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719094854715.png)

### 1.9 v-if和v-else和v-show

![image-20220719101656083](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719101656083.png)

![image-20220719104721208](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719104721208.png)

![image-20220719104833589](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719104833589.png)

![image-20220719114050697](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719114050697.png)

![image-20220719120013022](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719120013022.png)

![image-20220719120114066](C:\Users\26414\AppData\Roaming\Typora\typora-user-images\image-20220719120114066.png)
