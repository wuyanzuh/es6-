# let和const
## let
作用：声明变量,
用法:类似于var,但是所声明的边梁，只在let命令所在的代码块中有效

        {
            let a = 10;
            var b = 1;
        }
        a //is not defined
        b //1
### 1.不存在变量提升

        console.log(foo); //输出undefined
        var foo = 2;

        console.log(bar) //报错
        let bar = 2;
### 2.暂时性死区

如果区块中存在let和const命令，

这个区块对这些命令声明的变量，从一开始就形成了封闭作用域。凡是在声明之前使用这些变量，就会报错

3.不允许重复声明\

        let a = 0;
        let a = 1; //报错

### 4.块级作用域

        function f1() {
            let n = 5;
            if (true) {
                let n = 10;
            }
            console.log(n); //5
        }



## const
介绍：const声明一个只读的常量，一旦声明，常量的值就不能改变

const声明的变量不能改变值，意味着const一旦声明变量，就必须立刻初始化,不能留到以后赋值
特性与let相似