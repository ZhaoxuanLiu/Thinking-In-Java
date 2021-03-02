# 操作符
[3.1](#1) | [3.2](#2) | [3.3](#3) | [3.4](#4)

### <span id = "1">3.1 更简单的语句</span>
* N/A
### <span id = "2">3.2 使用Java操作符</span>
* 几乎所有的操作符都只能作用于 **基本数据类型**, 例外: "=", "==", "!=", 这些操作符也可以作用于 **对象数据类型**
* String类支持 "+"(字符串拼接) 和 "+=";
    ```Java
    class Main {
        public static void main(String[] args) {
            String a = "johnny";
            String b = "hello ";
            int c = 66;
            System.out.println(b + a);  //hello johnny
            System.out.println(a + c);  //johnny66
        }
    }
    ```
### <span id = "3">3.3 优先级</span>
* ![Getting Started](3-1.png)
### <span id = "4">3.4 赋值</span>
* 基本数据类型的赋值比较简单，基本类型储存了实际的数值，而并非指向一个对象的引用。
* 对于对象的赋值，真正操作的是对象的引用，所以将一个对象赋值给另一个对象，实际是将引用从一个地方复制给另一个地方, 两个对象的引用都指向同一个对象，无论改变哪个对象，另外一个也会改变。
    ```Java
    class Main {
        Object c = new Object(1);
        Object d = new Object(2);
        c = d; // c 和 d 都指向 new Object(2)
    }
    ```
### <span id = "5">3.5 算术操作符</span>
* N/A
### <span id = "6">3.6 自动递增和递减</span>
* N/A
### <span id = "7">3.7 关系操作符</span>
* == 和 != 对于基本数据类型比较的是两边基本类型的实际数值
* == 和 != 对于对象比较，比较的对象的引用是否相同，即使如下例子 n1 和 n2的值都是47，但是他们的引用是不同的，在堆中指向不同的对象，只不过这两个的对象里的元素相同而已
    ``` Java
    class Main {
        public static void main(String[] args) {
            Integer n1 = new Integer(47);
            Integer n2 = new Integer(47);
            System.out.println(n1 == n2);  // false
            System.out.println(n1 != n2);  // true
        }
    }
    ```
* 如果想比较两个对象的实际内容是否相同，可以用equals()来比较
    ``` Java
    class Main {
        public static void main(String[] args) {
            Integer n1 = new Integer(47);
            Integer n2 = new Integer(47);
            System.out.println(n1.equals(n2));  // true
        }
    }
    ```
* 但如果是你自己编写创造的类，如果不对默认的equals()方法进行重写覆盖，则不会达到上述例子的效果，因为equals()的默认方法还是比较对象的引用，上述例子之所以可以达到我们的与其效果是因为在Integer 类中的equals()方法已经被重写覆盖了，所以我们实际使用的是Integer.equals()的方法
### <span id = "8">3.8 逻辑操作符</span>





