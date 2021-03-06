<a href="https://996.icu"><img src="https://img.shields.io/badge/link-996.icu-red.svg" alt="996.icu"></a>
[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)
[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE_CN)
# generics
泛型 即参数化类型<br>
通过泛型 可以将list中的元素限制在某一类型<br>
例如 list< String > list中的元素必须是字符串型<br>
但是不能用于基本类型 list< int >错误 需要写成 list< Integer > 基本类型对应包转类的形式<br>
泛型类：class className< T >{...}<br>
T是自定义的类型参数 用于传递参数<br>
泛型方法：放在修饰符之后 返回类型前<br>
与普通方法相比 仅仅是定义方式不同 不必在调用泛型方法时指明参数类型<br>
泛型接口：接口的泛型针对接口中的抽象方法的类型<br>
泛型只在编译时有效 不会带入到运行阶段<br>
限制泛型范围：< T extends Number>泛型被限制在Number的子类中<br>
运算符不能直接用于泛型中<br>
泛型的类型必须是某一类 即将对象类型限制在某一类中 而基本数据类型不是类 所以 泛型的类型不能是基本数据类型<br>
## 基本数据类型与对象类型
存储方式不同 基本数据类型存放在栈 对象类型在栈中存放引用 值存放在堆<br>
在传递参数时 如果参数是基本数据类型 则传递值 对象类型 则传递引用<br>
基本数据类型不是类的对象 无法创建实例 对象类型(包括包装类)是类的对象<br>
### 区分基本数据类型与对象类型的原因
主要是基于程序性能的考量 基本类型定义定义的变量是存放在栈中 比如<br> ```int i = 5；```
<br>```Integer j = new Integer（10）；```<br>
j则只是一个对象的引用 存放在栈中 而实际的数值10则是放在堆里 堆的读写速度远不及栈了<br>
再有就是基本类型定义的变量创建和销毁很快 而类定义的变量还需要JVM去销毁 
