#### 1. 入口方法的两种定义

```dart
 main(){
    print('你好dart');
  }

void main(){
 print('你好dart');
}
```

#### 2. Dart 变量 常量 命名

```dart
Dart 变量：
  dart是一个强大的脚本类语言，可以不预先定义变量类型 ，自动会类型推倒
  dart中定义变量可以通过var关键字可以通过类型来申明变量
  如：
​    var str='this is var';
​    String str='this is var';
​    int str=123;
  注意： var 后就不要写类型 ，  写了类型 不要var   两者都写   var  a int  = 5;  报错
```

###### 1、dart的命名规则

1.变量名称必须由数字、字母、下划线和美元符($)组成。

2.注意：标识符开头不能是数字

3.标识符不能是保留字和关键字。   

4.变量的名字是区分大小写的如: age和Age是不同的变量。在实际的运用中,也建议,不要用一个单词大小写区分两个   变量。

5、标识符(变量名称)一定要见名思意 ：变量名称建议用名词，方法名称建议用动词  

```dart
void main(){
​    var str1='2134214';
​    //var 2str='xxx';   //错误
​    // var if='124214';  //错误
​    //变量的名字是区分大小写的
​    var age=20;
​    var Age=30;
​    print(age);
​    print(Age);
​    var price=12;
​    var name=124;

}
```

###### 2、 Dart 常量 final 和 const修饰符

const值不变 一开始就得赋值ß

final 可以开始不赋值 只能赋一次 ; 而final不仅有const的编译时常量的特性，最重要的它是运行时常量，并且final是惰性初始化，即在运行时第一次使用前才初始化

永远不改量的量，请使用final或const修饰它，而不是使用var或其他变量类型。

```dart
void main(){

 /*
  var str='this is a str';
  str='你好 str';
  print(str);
  int myNum=1234;
  myNum=4567;
  print(myNum);
 */
 //const常量
  // const PI=3.14159;
  // PI=123.1243; //错误的写法 常量不可以修改
  // print(PI);
// final 常量
​    // final PI=3.14159;
​    // PI=124214.214124;   //错误写法
​    // print(PI);
​    final a=new DateTime.now();
​    print(a);   //2022-07-07 14:27:23.856542
​    //const a=new DateTime.now();   //报错了
​    //区别：final 可以开始不赋值 只能赋一次 ; 而final不仅有const的编译时常量的特性，最重要的它是运行时常量，并且final是惰性初始化，即在运行时第一次使用前才初始化
​    final b;
​    b =10;
​    print(b); //10
}
```

#### 3. 数据类型

	 常用数据类型：
	  Numbers（数值）:
	      int
	      double
	  Strings（字符串）
	      String
	  Booleans(布尔)
	      bool
	  List（数组）
	      在Dart中，数组是列表对象，所以大多数人只是称它们为列表
	  Maps（字典）
	      通常来说，Map 是一个键值对相关的对象。 键和值可以是任何类型的对象。每个 键 只出现一次， 而一个值则可以出现多次

###### 1、字符串类型

```dart
void main(){

  //1、字符串定义的几种方式
  // var str1='this is str1';
  // var str2="this is str2";
  // print(str1);
  // print(str2);
  // String str1='this is str1';
  // String str2="this is str2";
  // print(str1);
  // print(str2);
  // String str1='''this is str1
  // this is str1
  // this is str1
  // ''';
  //  print(str1);
  //   String str1="""
  //   this is str1
  //   this is str1
  //   this is str1
  //   """;
  //  print(str1);
  //2、字符串的拼接
  String str1='你好';
  String str2='Dart';
  // print("$str1 $str2");
  print(str1 + str2);  
  print(str1 +" "+ str2);

}
```

###### 2、数值类型

  //1、int   必须是整型


```dart
int a=123;
a=45;
print(a);
```


  //2、double  既可以是整型 也可是浮点型

```dart
double b=23.5;
b=24;
print(b);
```

  //3、运算符

```dart
// + - * / %

var c=a+b;
print(c);
```

###### 3、布尔类型

```dart
 //1、bool

    // bool flag1=true;
    // print(flag1);

    // bool flag2=false;
    // print(flag2);
```

```dart
//2、条件判断语句
​      // var flag=true;
​      // if(flag){
​      //   print('真');      
​      // }else{
​      //   print('假');
​      // }
​      // var a=123;
​      // var b='123';
​      // if(a==b){
​      //   print('a=b');
​      // }else{
​      //    print('a!=b');
​      // }
​      var a=123;
​      var b=123;
​      if(a==b){
​        print('a=b');
​      }else{
​         print('a!=b');
​      }
```

###### 4、List（数组/集合）

```dart
void main() {
  //1、第一种定义List的方式
  // var l1=["张三",20,true];
  // print(l1);  //[张三, 20, true]
  // print(l1.length);  //3
  // print(l1[0]); //张三
  // print(l1[1]); //20
  //2、第二种定义List的方式 指定类型
  // var l2=<String>["张三","李四"];
  // print(l2);
  // var l3 = <int>[12, 30];
  // print(l3);
  //3、第三种定义List的方式  增加数据 ,通过[]创建的集合它的容量可以变化
  // var l4 = [];
  // print(l4);
  // print(l4.length);
  // l4.add("张三");
  // l4.add("李四");
  // l4.add(20);
  // print(l4);
  // print(l4.length);
  // var l5 = ["张三", 20, true];
  // l5.add("李四");
  // l5.add("zhaosi");
  // print(l5);
  //4 第四种定义List的方式
  ​    //  var l6=new List();  //在新版本的dart里面没法使用这个方法了
    ​   // var l6=List.filled(2, "");  //创建一个固定长度的集合
    ​    // print(l6);
    ​    // print(l6[0]);
    ​    // l6[0]="张三";   //修改集合的内容
    ​    // l6[1]="李四";
    ​    // print(l6);  //[张三, 李四]
    ​    // l6.add("王五");  //错误写法  通过List.filled创建的集合长度是固定  没法增加数据
    ​    //通过List.filled创建的集合长度是固定
    ​    // var l6=List.filled(2, "");
    ​    // print(l6.length);
    ​    // l6.length=0;  //修改集合的长度   报错
    ​    // var l7=<String>["张三","李四"];
    ​    // print(l7.length);  //2
    ​    // l7.length=0;  //可以改变的
    ​    // print(l7);  //[]
    ​    var l8=List<String>.filled(2, "");
  ​    l8[0]="string";
  ​    // l8[0]=222;
    ​    print(l8);
  ​    

}
```

###### 5、Maps（字典）类型

​	//第一种定义 Maps的方式

```dart
// var person={
//   "name":"张三",
//   "age":20,
//   "work":["程序员","送外卖"]
// };

// print(person);
// print(person["name"]);
// print(person["age"]);
// print(person["work"]);
```

   //第二种定义 Maps的方式

```dart
var p=new Map();
p["name"]="李四";
p["age"]=22;
p["work"]=["程序员","送外卖"];
print(p);
print(p["age"]);
```

###### 6、判断数据类型

 	// is 关键词来判断类型

```dart
  // var str='1234';
  // if(str is String){
  //   print('是string类型');
  // }else if(str is int){
  //    print('int');
  // }else{
  //    print('其他类型');
  // }

  var str=123;
  if(str is String){
    print('是string类型');
  }else if(str is int){
     print('int');
  }else{
     print('其他类型');
  }
```

#### 4. Dart运算符

```dart
1、Dart运算符：
    算术运算符
      +    -    *    /     ~/ (取整)     %（取余）
    关系运算符
      ==    ！=   >    <    >=    <=
    逻辑运算符
        !  &&   ||
    赋值运算符
     基础赋值运算符   =   ??=
     复合赋值运算符   +=  -=  *=   /=   %=  ~/=

    条件表达式 
        if  else   switch case 
        三目运算符
        ??运算符：

2、类型转换
    1、Number与String类型之间的转换    
    2、其他类型转换成Booleans类型
```

###### 02 算术运算符

```dart
void main(){
  int a=13;
  int b=5;
  print(a+b);   //加
  print(a-b);   //减
  print(a*b);   //乘
  print(a/b);   //除
  print(a%b);   //其余
  print(a~/b);  //取整
  var c=a*b;
  print('--------');
  print(c);
}
```

###### 03 关系运算符

```dart
void main(){
  //  ==    ！=   >    <    >=    <=
  int a=5;
  int b=3;
  print(a==b);   //判断是否相等
  print(a!=b);   //判断是否不等
  print(a>b);   //判断是否大于
  print(a<b);   //判断是否小于
  print(a>=b);   //判断是否大于等于
  print(a<=b);   //判断是否小于等于

  if(a>b){
    print('a大于b');
  }else{
    print('a小于b');
  }
}
```

###### 04 逻辑运算符

```dart
void main(){
  /* ! 取反 */ 
  // bool flag=false;
  // print(!flag);   //取反
 /* &&并且:全部为true的话值为true 否则值为false */ 

  // bool a=true;
  // bool b=true;
  // print(a && b);
  
 /* ||或者：全为false的话值为false 否则值为true */ 

  // bool a=false;
  // bool b=false;
  // print(a || b);

//如果一个人的年龄是20 并且 sex是女的话我们打印这个人

  // int age=20;
  // String sex="女";
  // if(age==20 && sex=="女"){
  //   print("$age --- $sex");
  // }else{
  //   print("不打印");
  // }

//如果一个人的年龄是20 或者 sex是女的话我们打印这个人
  int age=23;
  String sex="女";
  if(age==20 || sex=="女"){
    print("$age --- $sex");
  }else{
    print("不打印");
  }
}
```

###### 05 赋值运算符

```dart
void main(){
//  1、基础赋值运算符   =   ??=      
        // int a=10;
        // int b=3;
        // print(a);
        // int c=a+b;   //从右向左

    // b??=23;  表示如果b为空的话把 23赋值给b
        
        // int b=6;
        // b??=23;
        // print(b);
        // int b;
        // b??=23;
        // print(b);

//2、  复合赋值运算符   +=  -=  *=   /=   %=  ~/=

    // var a=12;
    // a=a+10;
    // print(a);
    // var a=13;
    // a+=10;   //表示a=a+10
    // print(a);
   var a=4;
   a*=3;  //a=a*3;
   print(a);


}
```

###### 06 条件表达式

```dart
void main(){
//1、if  else   switch case 
    // bool flag=true;
    // if(flag){
    //   print('true');
    // }else{
    //   print('false');
    // }

  //判断一个人的成绩 如果大于60 显示及格   如果大于 70显示良好  如果大于90显示优秀
  // var score=41;
  // if(score>90){
  //   print('优秀');
  // }else if(score>70){
  //    print('良好');
  // }else if(score>=60){
  //   print('及格');
  // }else{
  //   print('不及格');
  // }

  // var sex="女";
  // switch(sex){
  //   case "男":
  //     print('性别是男');
  //     break;
  //   case "女":
  //     print('性别是女');
  //     print('性别是女');
  //     break;
  //   default:
  //     print('传入参数错误');
  //     break;
  // }
  
  //2、三目运算符 
  // var falg=true;
  // var c;
  // if(falg){
  //     c='我是true';
  // }else{
  //   c="我是false";
  // }
  // print(c);

  bool flag=false;
  String c=flag?'我是true':'我是false';
  print(c);
  //3  ??运算符
  // var a;
  // var b= a ?? 10;
  // print(b);   10
  var a=22;
  var b= a ?? 10;
  print(b);      
}
```

###### 07 Dart类型转换

```dart
void main(){
    //1、Number与String类型之间的转换
      // Number类型转换成String类型 toString()
      // String类型转成Number类型  int.parse()
      // String str='123';
      // var myNum=int.parse(str);
      // print(myNum is int);

      // String str='123.1';
      // var myNum=double.parse(str);
      // print(myNum is double);
      //  String price='12';
      // var myNum=double.parse(price);
      // print(myNum);
      // print(myNum is double);
      //报错
      // String price='';
      // var myNum=double.parse(price);
      // print(myNum);
      // print(myNum is double);
    // try  ... catch
    //  String price='';
    //   try{
    //     var myNum=double.parse(price);
    //     print(myNum);
    //   }catch(err){
    //        print(0);
    //   } 
    // var myNum=12;
    // var str=myNum.toString();
    // print(str is String);

 // 2、其他类型转换成Booleans类型

        // isEmpty:判断字符串是否为空
        // var str='';
        // if(str.isEmpty){
        //   print('str空');
        // }else{
        //   print('str不为空');
        // }

        // var myNum=123;
        // if(myNum==0){
        //    print('0');
        // }else{
        //   print('非0');
        // }

        // var myNum;
        // if(myNum==0){
        //    print('0');
        // }else{
        //   print('非0');
        // }

        // var myNum;
        // if(myNum==null){
        //    print('空');
        // }else{
        //   print('非空');
        // }
        var myNum=0/0;        
        // print(myNum);
        if(myNum.isNaN){
          print('NaN');
        } 
}
```

#### 5. Dart循环

​    ++  --   表示自增 自减 1

###### 01 Dart for循环以及循环遍历List

```dart
// for基本语法
          for (int i = 1; i<=100; i++) {   
            print(i);
          }

        	//第一步，声明变量int i = 1;
        	//第二步，判断i <=100
        	//第三步，print(i);
        	//第四步，i++
        	//第五步 从第二步再来，直到判断为false

*/
```

//4、定义一个二维数组 打印里面的内容

```dart
    List list=[
      {
          "cate":'国内',
          "news":[
            {"title":"国内新闻1"},
            {"title":"国内新闻2"},
            {"title":"国内新闻3"}
          ]
      },
      {
          "cate":'国际',
          "news":[
            {"title":"国际新闻1"},
            {"title":"国际新闻2"},
            {"title":"国际新闻3"}
          ]
      }
    ];

    /*
    国内
        国内新闻1
        国内新闻2
        国内新闻3
    国际
        国际新闻1
        国际新闻2
    */
        for(var i=0;i<list.length;i++){
        print(list[i]["cate"]);
        print('-------------');
        for(var j=0;j<list[i]["news"].length;j++){
            print(list[i]["news"][j]["title"]);
        }
    }
```

###### 02 while  do...while

```dart
/*
	语法格式:
		while(表达式/循环条件){				
		}			
    		
		do{
			语句/循环体
			
		}while(表达式/循环条件);
		注意： 1、最后的分号不要忘记
			    2、循环条件中使用的变量需要经过初始化
		      3、循环体中，应有结束循环的条件，否则会造成死循环。
*/
```

###### 03 break和continue

```dart
	break语句功能:
      1、在switch语句中使流程跳出switch结构。
      2、在循环语句中使流程跳出当前循环,遇到break 循环终止，后面代码也不会执行
      强调:
      1、如果在循环中已经执行了break语句,就不会执行循环体中位于break后的语句。
      2、在多层循环中,一个break语句只能向外跳出一层
    break可以用在switch case中 也可以用在 for 循环和 while循环中
  continue语句的功能: 
   【注】只能在循环语句中使用,使本次循环结束，即跳过循环体重下面尚未执行的语句，接着进行下次的是否执行循环的判断。
    continue可以用在for循环以及 while循环中，但是不建议用在while循环中，不小心容易死循环
```

#### 6. list set map 循环详解

###### 01 List里面常用的属性和方法

```dart
常用属性：
    length          长度
    reversed        翻转
    isEmpty         是否为空
    isNotEmpty      是否不为空
常用方法：  
    add         增加
    addAll      拼接数组
    indexOf     查找  传入具体值
    remove      删除  传入具体值
    removeAt    删除  传入索引值
    fillRange   修改   
    insert(index,value);            指定位置插入    
    insertAll(index,list)           指定位置插入List
    toList()    其他类型转换成List  
    join()      List转换成字符串
    split()     字符串转化成List
    forEach   
    map
    where
    any
    every
```

```dart
void main(){
  // List myList=['香蕉','苹果','西瓜'];
  // print(myList[1]);
  // var list=new List();  //新版本没法使用
  // list.add('111');
  // list.add('222');
  // print(list);
//List里面的属性：
    // List myList=['香蕉','苹果','西瓜'];
    // print(myList.length);
    // print(myList.isEmpty);
    // print(myList.isNotEmpty);
    // print(myList.reversed);  //对列表倒序排序
    // var newMyList=myList.reversed.toList();
    // print(newMyList);

//List里面的方法：
    // List myList=['香蕉','苹果','西瓜'];
    //myList.add('桃子');   //增加数据  增加一个
    // myList.addAll(['桃子','葡萄']);  //拼接数组
    // print(myList);
    //print(myList.indexOf('苹x果'));    //indexOf查找数据 查找不到返回-1  查找到返回索引值

    // myList.remove('西瓜');
    // myList.removeAt(1);
    // print(myList);
  
    // List myList=['香蕉','苹果','西瓜'];
    // myList.fillRange(1, 2,'aaa');  //修改
    // myList.fillRange(1, 3,'aaa');  

    // myList.insert(1,'aaa');      //插入  一个
    // myList.insertAll(1, ['aaa','bbb']);  //插入 多个
    // print(myList);
    // List myList=['香蕉','苹果','西瓜'];
    // var str=myList.join('-');   //list转换成字符串
    // print(str);
    // print(str is String);  //true
    var str='香蕉-苹果-西瓜';
    var list=str.split('-');
    print(list);
    print(list is List);

}
```

###### 02 set 去除数组重复内容

```dart
//Set 
//用它最主要的功能就是去除数组重复内容
//Set是没有顺序且不能重复的集合，所以不能通过索引去获取值
void main(){
  // var s=new Set();
  // s.add('香蕉');
  // s.add('苹果');
  // s.add('苹果');
  // print(s);   //{香蕉, 苹果}
  // print(s.toList()); 
  List myList=['香蕉','苹果','西瓜','香蕉','苹果','香蕉','苹果'];
  var s=new Set();
  s.addAll(myList);
  print(s);
  print(s.toList());
  
}
```

###### 03 map属性和方法

```dart
/*
  映射(Maps)是无序的键值对：
    常用属性：
        keys            获取所有的key值
        values          获取所有的value值
        isEmpty         是否为空
        isNotEmpty      是否不为空
    常用方法:
        remove(key)     删除指定key的数据
        addAll({...})   合并映射  给映射内增加属性
        containsValue   查看映射内的值  返回true/false
        forEach   
        map
        where
        any
        every

*/

void main(){
  // Map person={
  //   "name":"张三",
  //   "age":20
  // };
  // var m=new Map();
  // m["name"]="李四";  
  // print(person);
  // print(m);

//常用属性：
    // Map person={
    //   "name":"张三",
    //   "age":20,
    //   "sex":"男"
    // };
    // print(person.keys.toList());
    // print(person.values.toList());
    // print(person.isEmpty);
    // print(person.isNotEmpty);
//常用方法：
    Map person={
      "name":"张三",
      "age":20,
      "sex":"男"
    };
    // person.addAll({
    //   "work":['敲代码','送外卖'],
    //   "height":160
    // });
    // print(person);
    // person.remove("sex");
    // print(person);
    print(person.containsValue('张三'));
}
```

###### 04 forEach map where any every

```dart
void main(){
      //  List myList=['香蕉','苹果','西瓜'];
      // for(var i=0;i<myList.length;i++){
      //   print(myList[i]);
      // }

      // for(var item in myList){
      //   print(item);
      // }


      // myList.forEach((value){
      //     print("$value");
      // });

      // List myList=[1,3,4];
      // List newList=new List();
      // for(var i=0;i<myList.length;i++){
      //   newList.add(myList[i]*2);
      // }
      // print(newList);

      // List myList=[1,3,4];      
      // var newList=myList.map((value){
      //     return value*2;
      // });
      // print(newList.toList());

      // List myList=[1,3,4,5,7,8,9];
      // var newList=myList.where((value){
      //     return value>5;
      // });
      // print(newList.toList());

      // List myList=[1,3,4,5,7,8,9];
      // var f=myList.any((value){   //只要集合里面有满足条件的就返回true
      //     return value>5;
      // });
      // print(f);

      // List myList=[1,3,4,5,7,8,9];
      // var f=myList.every((value){   //每一个都满足条件返回true  否则返回false
      //     return value>5;
      // });
      // print(f);

      // set
      // var s=new Set();
      // s.addAll([1,222,333]);
      // s.forEach((value)=>print(value));
      //map
       Map person={
          "name":"张三",
          "age":20
        };

        person.forEach((key,value){            
            print("$key---$value");
        });
}
```

#### 7. Dart 的函数

###### 01 方法的定义 变量 方法的作用域

```dart
/*
  内置方法/函数：
      print();
  自定义方法：
      自定义方法的基本格式：
      返回类型  方法名称（参数1，参数2,...）{
        方法体
        return 返回值;
      }
*/

void printInfo(){
  print('我是一个自定义方法');
}

int getNum(){
  var myNum=123;
  return myNum;
}

String printUserInfo(){
  return 'this is str';
}


List getList(){
  return ['111','2222','333'];
}
void main(){
  // print('调用系统内置的方法');
  // printInfo();
  // var n=getNum();
  // print(n);
  // print(printUserInfo());
  // print(getList());
  // print(getList());
//演示方法的作用域
  void xxx(){
      aaa(){
          print(getList());
          print('aaa');
      }
      aaa();
  }

  // aaa();  错误写法 
  xxx();  //调用方法
}
```

###### 02 方法传参 、默认参数、可选参数、命名参数 、方法作为参数

```dart
//调用方法传参
main() {
//1、定义一个方法 求1到这个数的所有数的和      60    1+2+3+。。。+60
  /*
    int sumNum(int n){
      var sum=0;
      for(var i=1;i<=n;i++)
      {
        sum+=i;
      }
      return sum;
    } 
    var n1=sumNum(5);
    print(n1);
    var n2=sumNum(100);
    print(n2);

 */

//2、定义一个方法然后打印用户信息
  // String printUserInfo(String username, int age) {
  //   //行参
  //   return "姓名:$username---年龄:$age";
  // }
  // print(printUserInfo('张三', 20)); //实参

//3、定义一个带可选参数的方法 ，最新的dart定义可选参数需要指定类型默认值

  // String printUserInfo(String username,[int age=0]){  //行参
  //   if(age!=0){
  //     return "姓名:$username---年龄:$age";
  //   }
  //   return "姓名:$username---年龄保密";
  // }
  // print(printUserInfo('张三',21)); //实参
  // print(printUserInfo('张三'));

//4、定义一个带默认参数的方法
  // String printUserInfo(String username,[String sex='男',int age=0]){  //行参
  //   if(age!=0){
  //     return "姓名:$username---性别:$sex--年龄:$age";
  //   }
  //   return "姓名:$username---性别:$sex--年龄保密";
  // }
  // print(printUserInfo('张三'));
  // print(printUserInfo('小李','女'));
  // print(printUserInfo('小李','女',30));

//5、定义一个命名参数的方法，最新的dart定义命名参数需要指定类型默认值

  // String printUserInfo(String username, {int age = 0, String sex = '男'}) {//行参    
  //   if (age != 0) {
  //     return "姓名:$username---性别:$sex--年龄:$age";
  //   }
  //   return "姓名:$username---性别:$sex--年龄保密";
  // }
  // print(printUserInfo('张三', age: 20, sex: '未知'));

//6、实现一个 把方法当做参数的方法

  // var fn=(){
  //   print('我是一个匿名方法');
  // };
  // fn();
  //fn1方法
  fn1() {
    print('fn1');
  }
  //fn2方法
  fn2(fn) {
    fn();
  }
  //调用fn2这个方法 把fn1这个方法当做参数传入
  fn2(fn1);
}
```

###### 03 箭头函数  函数的相互调用 

```dart
void main() {
/*需求：使用forEach打印下面List里面的数据*/

  // List list=['苹果','香蕉','西瓜'];
  // list.forEach((value){
  //   print(value);
  // });
  // list.forEach((value)=>print(value));

  //注意和方法的区别: 箭头函数内只能写一条语句，并且语句后面没有分号(;)
  // list.forEach((value)=>{
  //   print(value)
  // });

/*需求：修改下面List里面的数据，让数组中大于2的值乘以2*/

  // List list=[4,1,2,3,4];
  // var newList=list.map((value){
  //     if(value>2){
  //       return value*2;
  //     }
  //     return value;
  // });
  // print(newList.toList());
  //  var newList=list.map((value)=>value>2?value*2:value);
  //  print(newList.toList());
  

/*
需求：    1、定义一个方法isEvenNumber来判断一个数是否是偶数  
         2、定义一个方法打印1-n以内的所有偶数
*/

// 1、定义一个方法isEvenNumber来判断一个数是否是偶数  
  bool isEvenNumber(int n) {
    if (n % 2 == 0) {
      return true;
    }
    return false;
  }
//  2、定义一个方法打印1-n以内的所有偶数
  printNum(int n) {
    for (var i = 1; i <= n; i++) {
      if (isEvenNumber(i)) {
        print(i);
      }
    }
  }
  printNum(10);
}

```

###### 05 匿名方法 自执行方法 方法的递归

```dart
int getNum(int n) {
  return n;
}

void main() {
  // print(getNum(12));

  //匿名方法
  // var printNum=(){
  //   print(123);
  // };
  // printNum();

  // var printNum=(int n){
  //   print(n+2);
  // };
  // printNum(12);

//自执行方法

  // ((int n){
  //   print(n);
  //   print('我是自执行方法');
  // })(12);

//方法的递归
  // var sum = 1;
  // fn(int n) {
  //   sum *= n;
  //   if (n == 1) {
  //     return;
  //   }
  //   fn(n - 1);
  // }
  // fn(5);
  // print(sum);

//通过方法的递归 求1-100的和

  var sum=0;
  fn(int n){
      sum+=n;
      if(n==0){
        return;
      }
      fn(n-1);
  }

  fn(100);
  print(sum);
}

```

###### 06 闭包

```dart
/*
闭包：

    1、全局变量特点:    全局变量常驻内存、全局变量污染全局
    2、局部变量的特点：  不常驻内存会被垃圾机制回收、不会污染全局  
  /*  想实现的功能：
        1.常驻内存        
        2.不污染全局   
          产生了闭包,闭包可以解决这个问题.....  
          闭包: 函数嵌套函数, 内部函数会调用外部函数的变量或参数, 变量或参数不会被系统回收(不会释放内存)
	        闭包的写法： 函数嵌套函数，并return 里面的函数，这样就形成了闭包。
    */  
*/

/*全局变量*/
var a = 123;
void main() {
  // print(a);
  // fn(){
  //   a++;
  //   print(a);
  // }
  // fn();
  // fn();
  // fn();
//局部变量
  // printInfo() {
  //   var myNum = 123;
  //   myNum++;
  //   print(myNum);
  // }

  // printInfo();
  // printInfo();
  // printInfo();

//闭包
  fn() {
    var a = 123; /*不会污染全局   常驻内存*/
    return () {
      a++;
      print(a);
    };
  }
  var b = fn();
  b();
  b();
  b();
}

```

#### 9. dart中的类，对象

###### 01 Dart面向对象的介绍 以及Data内置对象

```dart
/*
面向对象编程(OOP)的三个基本特征是：封装、继承、多态      
      封装：封装是对象和类概念的主要特性。封装，把客观事物封装成抽象的类，并且把自己的部分属性和方法提供给其他对象调用, 而一部分属性和方法则隐藏。
               
      继承：面向对象编程 (OOP) 语言的一个主要功能就是“继承”。继承是指这样一种能力：它可以使用现有类的功能，并在无需重新编写原来的类的情况下对这些功能进行扩展。
           
      多态：允许将子类类型的指针赋值给父类类型的指针, 同一个函数调用会有不同的执行效果 。
Dart所有的东西都是对象，所有的对象都继承自Object类。
Dart是一门使用类和单继承的面向对象语言，所有的对象都是类的实例，并且所有的类都是Object的子类
一个类通常由属性和方法组成。
*/
void main(){        
    // List list=new List();  //最新版本的dart中已没法使用 
    // list.isEmpty;
    // list.add('香蕉');
    // list.add('香蕉1');
    Map m=new Map();
    m["username"]="张三";
    m.addAll({"age":20});
    m.isEmpty;
    Object a=123;
    Object v=true;
    print(a);
    print(v);

}
```

###### 02 Dart中创建义类使用类

```dart
/*
Dart是一门使用类和单继承的面向对象语言，所有的对象都是类的实例，并且所有的类都是Object的子类
*/
class Person{
  String name="张三";
  int age=23;
  void getInfo(){
      // print("$name----$age");
      print("${this.name}----${this.age}");
  }
  void setInfo(int age){
    this.age=age;
  }
}
void main(){
  //实例化
  // var p1=new Person();
  // print(p1.name);
  // p1.getInfo();
  Person p1=new Person();
  // print(p1.name);
  p1.setInfo(28);
  p1.getInfo();
}
```

###### 03 Dart中自定义类的默认构造函数

```dart
// class Person{
//   String name='张三';
//   int age=20; 
//   //默认构造函数
//   Person(){
//     print('这是构造函数里面的内容  这个方法在实例化的时候触发');
//   }
//   void printInfo(){   
//     print("${this.name}----${this.age}");
//   }
// }

//最新版本的dart中需要初始化不可为null的实例字段，如果不初始化的话需要在属性前面加上late
// class Person{
//   late String name;
//   late int age; 
//   //默认构造函数
//   Person(String name,int age){
//       this.name=name;
//       this.age=age;
//   }
//   void printInfo(){   
//     print("${this.name}----${this.age}");
//   }
// }

//最新版本的dart中需要初始化不可为null的实例字段，如果不初始化的话需要在属性前面加上late
class Person{
  late String name;
  late int age; 
  //默认构造函数的简写
  Person(this.name,this.age);
  void printInfo(){   
    print("${this.name}----${this.age}");
  }
}

void main(){
  Person p1=new Person('张三',20);
  p1.printInfo();
  Person p2=new Person('李四',25);
  p2.printInfo();

}
```

###### 04 Dart中自定义类的命名构造函数

```dart
/*
dart里面构造函数可以写多个
注意：最新版本的dart中需要初始化不可为null的实例字段，如果不初始化的话需要在属性前面加上late
*/
class Person {
  late String name;
  late int age;
  //默认构造函数的简写
  Person(this.name, this.age);
  Person.now() {
    print('我是命名构造函数');
  }
  Person.setInfo(String name, int age) {
    this.name = name;
    this.age = age;
  }
  void printInfo() {
    print("${this.name}----${this.age}");
  }
}

void main() {
  // var d=new DateTime.now();   //实例化DateTime调用它的命名构造函数
  // print(d);
  //Person p1=new Person('张三', 20);   //默认实例化类的时候调用的是 默认构造函数
  //Person p1=new Person.now();   //命名构造函数
  Person p1 = new Person.setInfo('李四', 30);
  p1.printInfo();
}
```

###### 05 Dart中把类单独抽离成一个模块

```
-lib
-- Animal.dart
-- Person.dart
-mani.dart
```

Animal.dart

```dart
class Animal{
  late String _name;   //私有属性
  late int age; 
  //默认构造函数的简写
  Animal(this._name,this.age);

  void printInfo(){   
    print("${this._name}----${this.age}");
  }

  String getName(){ 
    return this._name;
  } 
  void _run(){
    print('这是一个私有方法');
  }

  execRun(){
    this._run();  //类里面方法的相互调用
  }
}
```

Person.dart

```dart
// 注意：最新版本的dart中需要初始化不可为null的实例字段，如果不初始化的话需要在属性前面加上late
class Person{
  late String name;
  late int age; 
  //默认构造函数的简写
  Person(this.name,this.age);
  
  Person.now(){
    print('我是命名构造函数');
  }

  Person.setInfo(String name,int age){
    this.name=name;
    this.age=age;
  }

  void printInfo(){   
    print("${this.name}----${this.age}");
  }
}

```

main.dart

```dart
import 'lib/Person.dart';
void main(){
  Person p1=new Person.setInfo('李四1',30);
  p1.printInfo(); 
}
```

###### 06 Dart中的私有方法 和私有属性

```dart
/*
Dart和其他面向对象语言不一样，Data中没有 public  private protected这些访问修饰符合
但是我们可以使用_把一个属性或者方法定义成私有。
*/
import 'lib/Animal.dart';
void main(){
 Animal a=new Animal('小狗', 3);
 print(a.getName());
 a.execRun();   //间接的调用私有方法
}
```

###### 07 类中的getter和setter修饰符的用法

```dart
// class Rect{
//   int height;
//   int width; 
//   getArea(){
//     return this.height*this.width;
//   } 
// }

// class Rect{
//   num height;
//   num width;   
//   Rect(this.height,this.width);
//   area(){
//     return this.height*this.width;
//   }
// }

// void main(){
//   Rect r=new Rect(10,4);
//   print("面积:${r.area()}");   
// }

// class Rect{
//   num height;
//   num width;   
//   Rect(this.height,this.width);
//   get area{
//     return this.height*this.width;
//   }
// }

// void main(){
//   Rect r=new Rect(10,2);
//   print("面积:${r.area}");      //注意调用直接通过访问属性的方式访问area
// }

class Rect{
  late num height;
  late num width;   
  Rect(this.height,this.width);
  get area{
    return this.height*this.width;
  }
  set areaHeight(value){
    this.height=value;
  }
}
void main(){
  Rect r=new Rect(10,4);
  // print("面积:${r.area()}");   
  r.areaHeight=6;
  print(r.area);

}
```

###### 08 类中的初始化列表

```dart
// Dart中我们也可以在构造函数体运行之前初始化实例变量
class Rect{
  int height;
  int width;
  Rect():height=2,width=10{    
    print("${this.height}---${this.width}");
  }
  getArea(){
    return this.height*this.width;
  } 
}
void main(){
  Rect r=new Rect();
  print(r.getArea()); 
   
}
```

#### 10. dart中的类 静态成员 操作符 类的继承

###### 01 Dart 类中的静态成员 静态方法

```dart
/*
Dart中的静态成员:
  1、使用static 关键字来实现类级别的变量和函数
  2、静态方法不能访问非静态成员，非静态方法可以访问静态成员

*/
// class Person {
//   static String name = '张三';
//   static void show() {
//     print(name);
//   }
// }

// main(){
//   print(Person.name);
//   Person.show();  
// }

class Person {
  static String name = '张三';
  int age=20;  
  static void show() {
    print(name);
  }
  void printInfo(){  /*非静态方法可以访问静态成员以及非静态成员*/
      // print(name);  //访问静态属性
      // print(this.age);  //访问非静态属性
      show();   //调用静态方法
  }
  static void printUserInfo(){//静态方法
        print(name);   //静态属性
        show();        //静态方法
        //print(this.age);     //静态方法没法访问非静态的属性
        // this.printInfo();   //静态方法没法访问非静态的方法
        // printInfo();
  }
}
main(){
  // print(Person.name);
  // Person.show(); 
  // Person p=new Person();
  // p.printInfo(); 
  Person.printUserInfo();
}
```

###### 02 Dart 中的对象操作符

```dart
/*
Dart中的对象操作符:
    ?     条件运算符 （了解）   https://dart.dev/tools/diagnostic-messages#invalid_null_aware_operator        
    as    类型转换
    is    类型判断
    ..    级联操作 （连缀）  (记住)
*/

class Person {
  String name;
  num age;
  Person(this.name, this.age);
  void printInfo() {
    print("${this.name}---${this.age}");
  }
}

main() {
  // Person p;
  // p?.printInfo();   //已被最新的dart废弃 了解

  //  Person p=new Person('张三', 20);
  //  p?.printInfo();   //已被最新的dart废弃 了解

  Person p=new Person('张三', 20);
  if(p is Person){
      p.name="李四";
  }
  p.printInfo();
  print(p is Object);

  // var p1;
  // p1='';
  // p1=new Person('张三1', 20);
  // p1.printInfo();
  // (p1 as Person).printInfo();

  //  Person p1=new Person('张三1', 20);
  //  p1.printInfo();
  //  p1.name='张三222';
  //  p1.age=40;
  //  p1.printInfo();

  Person p1 = new Person('张三1', 20);
  p1.printInfo();
  p1
    ..name = "李四"
    ..age = 30
    ..printInfo();
}
```

###### 03 Dart 类的继承-简单继承

```dart
/*
面向对象的三大特性：封装 、继承、多态
Dart中的类的继承：  
    1、子类使用extends关键词来继承父类
    2、子类会继承父类里面可见的属性和方法 但是不会继承构造函数
    3、子类能复写父类的方法 getter和setter

*/
class Person {
  String name='张三';
  num age=20; 
  void printInfo() {
    print("${this.name}---${this.age}");  
  } 
}
class Web extends Person{
}

main(){   
  Web w=new Web();
  print(w.name);
  w.printInfo(); 
}
```

###### 04 Dart 类的继承 super关键词的使用  实例化自类给父类构造函数传参 

```dart
/*
面向对象的三大特性：封装 、继承、多态
Dart中的类的继承：  
    1、子类使用extends关键词来继承父类
    2、子类会继承父类里面可见的属性和方法 但是不会继承构造函数
    3、子类能复写父类的方法 getter和setter

*/
class Person {
  late String name;
  late num age; 
  Person(this.name,this.age);
  void printInfo() {
    print("${this.name}---${this.age}");  
  }
}
class Web extends Person{
  Web(String name, num age) : super(name, age){    
  }  
}

main(){ 
  // Person p=new Person('李四',20);
  // p.printInfo();
  // Person p1=new Person('张三',20);
  // p1.printInfo();
  Web w=new Web('张三', 12);
  w.printInfo();
}
```

###### 05 Dart 类的继承 super关键词的使用  实例化自类给父类构造函数传参

```dart
/*
面向对象的三大特性：封装 、继承、多态
Dart中的类的继承：  
    1、子类使用extends关键词来继承父类
    2、子类会继承父类里面可见的属性和方法 但是不会继承构造函数
    3、子类能复写父类的方法 getter和setter
   注意:最新版本的dart中需要初始化不可为null的实例字段，如果不初始化的话需要在属性前面加上late
*/

class Person {
  String name;
  num age; 
  Person(this.name,this.age);
  void printInfo() {
    print("${this.name}---${this.age}");  
  }
}

class Web extends Person{
  late String sex;
  Web(String name, num age,String sex) : super(name, age){
    this.sex=sex;
  }
  run(){
   print("${this.name}---${this.age}--${this.sex}");  
  }  
}

main(){ 
  // Person p=new Person('李四',20);
  // p.printInfo();

  // Person p1=new Person('张三',20);
  // p1.printInfo();


  Web w=new Web('张三', 12,"男");
  w.printInfo();
  w.run();
}
```

###### 06 Dart 类的继承 实例化自类给命名构造函数传参

```dart
/*
面向对象的三大特性：封装 、继承、多态
Dart中的类的继承：  
    1、子类使用extends关键词来继承父类
    2、子类会继承父类里面可见的属性和方法 但是不会继承构造函数
    3、子类能复写父类的方法 getter和setter
注意:最新版本的dart中需要初始化不可为null的实例字段，如果不初始化的话需要在属性前面加上late
*/

class Person {
  String name;
  num age;
  Person(this.name, this.age);
  Person.xxx(this.name, this.age);
  void printInfo() {
    print("${this.name}---${this.age}");
  }
}

class Web extends Person {
  late String sex;
  Web(String name, num age, String sex) : super.xxx(name, age) {
    this.sex = sex;
  }
  run() {
    print("${this.name}---${this.age}--${this.sex}");
  }
}

main() {
  // Person p=new Person('李四',20);
  // p.printInfo();
  // Person p1=new Person('张三',20);
  // p1.printInfo();
  Web w = new Web('张三', 12, "男");
  w.printInfo();
  w.run();
}

```

###### 07 Dart 类的继承 覆写父类的方法

```dart
/*
面向对象的三大特性：封装 、继承、多态
Dart中的类的继承：  
    1、子类使用extends关键词来继承父类
    2、子类会继承父类里面可见的属性和方法 但是不会继承构造函数
    3、子类能复写父类的方法 getter和setter

*/

class Person {
  String name;
  num age; 
  Person(this.name,this.age);
  void printInfo() {
    print("${this.name}---${this.age}");  
  }
  work(){
    print("${this.name}在工作...");
  }
}

class Web extends Person{
  Web(String name, num age) : super(name, age);
  run(){
    print('run');
  }
  //覆写父类的方法
  @override       //可以写也可以不写  建议在覆写父类方法的时候加上 @override 
  void printInfo(){
     print("姓名：${this.name}---年龄：${this.age}"); 
  }
  @override
  work(){
    print("${this.name}的工作是写代码");
  }
}

main(){
  Web w=new Web('李四',20);
  w.printInfo();
  w.work(); 
}
```

###### 08 Dart 自类里面调用父类的方法

```dart
/*
面向对象的三大特性：封装 、继承、多态
Dart中的类的继承：  
    1、子类使用extends关键词来继承父类
    2、子类会继承父类里面可见的属性和方法 但是不会继承构造函数
    3、子类能复写父类的方法 getter和setter

*/
class Person {
  String name;
  num age; 
  Person(this.name,this.age);
  void printInfo() {
    print("${this.name}---${this.age}");  
  }
  work(){
    print("${this.name}在工作...");
  }
}

class Web extends Person{
  Web(String name, num age) : super(name, age);
  run(){
    print('run');
    super.work();  //子类调用父类的方法
  }
  //覆写父类的方法
  @override       //可以写也可以不写  建议在覆写父类方法的时候加上 @override 
  void printInfo(){
     print("姓名：${this.name}---年龄：${this.age}"); 
  }
}

main(){
  Web w=new Web('李四',20);
  // w.printInfo();
  w.run(); 
}
```

#### 11. Dart中的抽象类 多态 和接口

###### 01 Dart中的抽象类

```dart
/*
Dart中抽象类: Dart抽象类主要用于定义标准，子类可以继承抽象类，也可以实现抽象类接口。
  1、抽象类通过abstract 关键字来定义
  2、Dart中的抽象方法不能用abstract声明，Dart中没有方法体的方法我们称为抽象方法。
  3、如果子类继承抽象类必须得实现里面的抽象方法
  4、如果把抽象类当做接口实现的话必须得实现抽象类里面定义的所有属性和方法。
  5、抽象类不能被实例化，只有继承它的子类可以
extends抽象类 和 implements的区别：
  1、如果要复用抽象类里面的方法，并且要用抽象方法约束自类的话我们就用extends继承抽象类
  2、如果只是把抽象类当做标准的话我们就用implements实现抽象类
案例：定义一个Animal 类要求它的子类必须包含eat方法
*/
abstract class Animal{
  eat();   //抽象方法
  run();  //抽象方法  
  printInfo(){
    print('我是一个抽象类里面的普通方法');
  }
}

class Dog extends Animal{
  @override
  eat() {
     print('小狗在吃骨头');
  }

  @override
  run() {
    // TODO: implement run
    print('小狗在跑');
  }  
}
class Cat extends Animal{
  @override
  eat() {
    // TODO: implement eat
    print('小猫在吃老鼠');
  }

  @override
  run() {
    // TODO: implement run
    print('小猫在跑');
  }

}

main(){
  Dog d=new Dog();
  d.eat();
  d.printInfo();

  Cat c=new Cat();
  c.eat();
  c.printInfo();

  // Animal a=new Animal();   //抽象类没法直接被实例化
}
```

###### 02 Dart中多态

```dart
/*
Datr中的多态：
    允许将子类类型的指针赋值给父类类型的指针, 同一个函数调用会有不同的执行效果 。
    子类的实例赋值给父类的引用。 
    多态就是父类定义一个方法不去实现，让继承他的子类去实现，每个子类有不同的表现。
*/
abstract class Animal{
  eat();   //抽象方法 
}

class Dog extends Animal{
  @override
  eat() {
     print('小狗在吃骨头');
  }
  run(){
    print('run');
  }
}
class Cat extends Animal{
  @override
  eat() {   
    print('小猫在吃老鼠');
  }
  run(){
    print('run');
  }
}

main(){
  // Dog d=new Dog();
  // d.eat();
  // d.run();
  // Cat c=new Cat();
  // c.eat();
  Animal d=new Dog();
  d.eat();
  Animal c=new Cat();
  c.eat();
}
```

###### 03 接口

```
-lib
-- Db.dart
-- MsSql.dart
-- Mysql.dart
-main.dart
```

- Db.dart

```dart
abstract class Db{   //当做接口   接口：就是约定 、规范
    late String uri;      //数据库的连接地址
    add(String data);
    save();
    delete();
}
```

- MsSql.dart

```dart
import 'Db.dart';
class MsSql implements Db{
  @override
  late String uri;
  @override
  add(String data) {
    print('这是mssql的add方法'+data);
  }

  @override
  delete() {
    // TODO: implement delete
    return null;
  }
  
  @override
  save() {
    // TODO: implement save
    return null;
  }
}
```

- Mysql.dart

```dart
import 'Db.dart';
class Mysql implements Db{  
  @override
  String uri;
  Mysql(this.uri);

  @override
  add(data) {   
    print('这是mysql的add方法'+data);
  }

  @override
  delete() {   
    return null;
  }
  
  @override
  save() {   
    return null;
  }
}
```

```dart
/*
和Java一样，dart也有接口，但是和Java还是有区别的。
  首先，dart的接口没有interface关键字定义接口，而是普通类或抽象类都可以作为接口被实现。
  同样使用implements关键字进行实现。
  但是dart的接口有点奇怪，如果实现的类是普通类，会将普通类和抽象中的属性的方法全部需要覆写一遍。
  而因为抽象类可以定义抽象方法，普通类不可以，所以一般如果要实现像Java接口那样的方式，一般会使用抽象类。
  建议使用抽象类定义接口。
*/

/*
定义一个DB库 支持 mysql  mssql  mongodb
mysql  mssql  mongodb三个类里面都有同样的方法
*/
abstract class Db{   //当做接口   接口：就是约定 、规范
    late String uri;      //数据库的链接地址
    add(String data);
    save();
    delete();
}

class Mysql implements Db{
  @override
  String uri;
  Mysql(this.uri);
  @override
  add(data) {
    // TODO: implement add
    print('这是mysql的add方法'+data);
  }
  @override
  delete() {
    // TODO: implement delete
    return null;
  }
  @override
  save() {
    // TODO: implement save
    return null;
  }
  remove(){
  }
}

class MsSql implements Db{
  @override
  late String uri;
  @override
  add(String data) {
    print('这是mssql的add方法'+data);
  }

  @override
  delete() {
    // TODO: implement delete
    return null;
  }

  @override
  save() {
    // TODO: implement save
    return null;
  }
}

main() {
  Mysql mysql=new Mysql('xxxxxx');
  mysql.add('1243214'); 
}
```

###### 04 接口 文件分离

```dart
/*
和Java一样，dart也有接口，但是和Java还是有区别的。
  首先，dart的接口没有interface关键字定义接口，而是普通类或抽象类都可以作为接口被实现。
  同样使用implements关键字进行实现。
  但是dart的接口有点奇怪，如果实现的类是普通类，会将普通类和抽象中的属性的方法全部需要覆写一遍。
  而因为抽象类可以定义抽象方法，普通类不可以，所以一般如果要实现像Java接口那样的方式，一般会使用抽象类。
  建议使用抽象类定义接口。
*/

/*
定义一个DB库 支持 mysql  mssql  mongodb
mysql  mssql  mongodb三个类里面都有同样的方法
*/

// import 'lib/Mysql.dart';
import 'lib/MsSql.dart';
main() {
  // Mysql mysql=new Mysql('xxxxxx');
  // mysql.add('1243214');
  MsSql mssql=new MsSql();
  mssql.uri='127.0.0.1';
  mssql.add('增加的数据'); 
}
```

#### 12. Dart中一个类实现多个接口 以及Dart中的Mixins

###### 01 Dart中implements实现多个接口

```dart
/*
Dart中一个类实现多个接口：
*/

abstract class A{
  late String name;
  printA();
}

abstract class B{
  printB();
}

class C implements A,B{  
  @override
  late String name;  
  @override
  printA() {
    print('printA');
  }
  @override
  printB() {
    // TODO: implement printB
    return null;
  }

  
}


void main(){
  C c=new C();
  c.printA();
}
```

###### 02 Dart中的mixins

```dart
/*
mixins的中文意思是混入，就是在类中混入其他功能。
在Dart中可以使用mixins实现类似多继承的功能
因为mixins使用的条件，随着Dart版本一直在变，这里讲的是Dart2.x中使用mixins的条件：
  1、作为mixins的类只能继承自Object，不能继承其他类
  2、作为mixins的类不能有构造函数
  3、一个类可以mixins多个mixins类
  4、mixins绝不是继承，也不是接口，而是一种全新的特性
*/
class A {
  String info="this is A";
  void printA(){
    print("A");
  }
}

class B {
  void printB(){
    print("B");
  }
}
class C with A,B{ 
}
void main(){
  var c=new C();  
  c.printA();
  c.printB();
  print(c.info);

}
```

###### 03 Dart中的mixins

```dart
/*
mixins的中文意思是混入，就是在类中混入其他功能。
在Dart中可以使用mixins实现类似多继承的功能
因为mixins使用的条件，随着Dart版本一直在变，这里讲的是Dart2.x中使用mixins的条件：
  1、作为mixins的类只能继承自Object，不能继承其他类
  2、作为mixins的类不能有构造函数
  3、一个类可以mixins多个mixins类
  4、mixins绝不是继承，也不是接口，而是一种全新的特性
*/
class Person{
  String name;
  num age;
  Person(this.name,this.age);
  printInfo(){
    print('${this.name}----${this.age}');
  }
  void run(){
    print("Person Run");
  }
}

class A {
  String info="this is A";
  void printA(){
    print("A");
  }
  void run(){
    print("A Run");
  }
}

class B {  
  void printB(){
    print("B");
  }
  void run(){
    print("B Run");
  }
}

class C extends Person with B,A{
  C(String name, num age) : super(name, age);
  
}

void main(){  
  var c=new C('张三',20);  
  c.printInfo();
  // c.printB();
  // print(c.info);
  c.run();
}
```

###### 04 Dart中的mixins 的类型

```dart
/*
mixins的实例类型是什么？
很简单，mixins的类型就是其超类的子类型。
*/
class A {
  String info="this is A";
  void printA(){	
    print("A");
  }
}
class B {
  void printB(){
    print("B");
  }
}
class C with A,B{
}
void main(){  
   var c=new C();  
  print(c is C);    //true
  print(c is A);    //true
  print(c is B);   //true
  // var a=new A();
  // print(a is Object);
}
```

#### 13. dart 泛型 范型方法 范型类 范型接口

###### 01 Dart中的泛型 泛型方法

```dart
/*
通俗理解：泛型就是解决 类 接口 方法的复用性、以及对不特定数据类型的支持(类型校验)
*/

//只能返回string类型的数据
  // String getData(String value){
  //     return value;
  // }
//同时支持返回 string类型 和int类型  （代码冗余）

  // String getData1(String value){
  //     return value;
  // }
  // int getData2(int value){
  //     return value;
  // }
//同时返回 string类型 和number类型       不指定类型可以解决这个问题
  // getData(value){
  //     return value;
  // }
//不指定类型放弃了类型检查。我们现在想实现的是传入什么 返回什么。比如:传入number 类型必须返回number类型  传入 string类型必须返回string类型
 
  // T getData<T>(T value){
  //     return value;
  // }
  getData<T>(T value){
      return value;
  }

void main(){
    // print(getData(21));
    // print(getData('xxx'));
    // getData<String>('你好');
    print(getData<int>(12));
}
```

###### 02 Dart中的泛型 泛型类

```dart
//集合List 泛型类的用法
//案例：把下面类转换成泛型类，要求MyList里面可以增加int类型的数据，也可以增加String类型的数据。但是每次调用增加的类型要统一
/*
class MyList {
  List list = <int>[];
  void add(int value) {
    this.list.add(value);
  }
  List getList() {
    return list;
  }
}
MyList l = new MyList();
l.add(1);
l.add(12);
l.add(5);
print(l.getList());
*/
class MyList<T> {
  List list = <T>[];
  void add(T value) {
    this.list.add(value);
  }
  List getList() {
    return list;
  }
}

main() {
  // MyList l1=new MyList();
  // l1.add("张三");
  // l1.add(12);
  // l1.add(true);
  // print(l1.getList());

  // MyList l2 = new MyList<String>();
  // l2.add("张三1");
  // // l2.add(11);  //错误的写法
  // print(l2.getList());

  // MyList l3 = new MyList<int>();
  // l3.add(11);
  // l3.add(12);
  // l3.add("aaaa");
  // print(l3.getList());

  // List list = List.filled(2, "");
  // list[0] = "张三";
  // list[1] = "李四";
  // print(list);

  // List list = new List.filled(2, "");
  // list[0] = "张三1";
  // list[1] = "李四";
  // print(list);

  // List list = new List<String>.filled(2, "");
  // list[0] = "张三1";
  // list[1] = "李四";
  // print(list);

  List list2 = new List<int>.filled(2, 0);
  list2[0] = 12;
  list2[1] = 13;
  print(list2);
}
```

###### 03 Dart中的泛型 泛型接口

```dart
/*
Dart中的泛型接口:
    实现数据缓存的功能：有文件缓存、和内存缓存。内存缓存和文件缓存按照接口约束实现。
    1、定义一个泛型接口 约束实现它的子类必须有getByKey(key) 和 setByKey(key,value)
    2、要求setByKey的时候的value的类型和实例化子类的时候指定的类型一致
*/
// abstract class ObjectCache {
//   getByKey(String key);
//   void setByKey(String key, Object value);
// }

// abstract class StringCache {
//   getByKey(String key);
//   void setByKey(String key, String value);
// }

// abstract class Cache<T> {
//   getByKey(String key);
//   void setByKey(String key, T value);
// }

abstract class Cache<T> {
  getByKey(String key);
  void setByKey(String key, T value);
}

class FileCache<T> implements Cache<T> {
  @override
  getByKey(String key) {
    return null;
  }
  @override
  void setByKey(String key, T value) {
    print("我是文件缓存 把key=${key}  value=${value}的数据写入到了文件中");
  }
}

class MemoryCache<T> implements Cache<T> {
  @override
  getByKey(String key) {
    return null;
  }
  @override
  void setByKey(String key, T value) {
    print("我是内存缓存 把key=${key}  value=${value} -写入到了内存中");
  }
}

void main() {
  // MemoryCache m=new MemoryCache<String>();
  //  m.setByKey('index', '首页数据');
  MemoryCache m = new MemoryCache<Map>();
  m.setByKey('index', {"name": "张三", "age": 20});
}
```

#### 14. Dart 中的库 自定义库 系统库 第三方库

###### 00 Dart中的库

```dart
/*
前面介绍Dart基础知识的时候基本上都是在一个文件里面编写Dart代码的，但实际开发中不可能这么写，模块化很重要，所以这就需要使用到库的概念。
在Dart中，库的使用时通过import关键字引入的。
library指令可以创建一个库，每个Dart文件都是一个库，即使没有使用library指令来指定。
Dart中的库主要有三种：
    1、我们自定义的库     
          import 'lib/xxx.dart';
    2、系统内置库       
          import 'dart:math';    
          import 'dart:io'; 
          import 'dart:convert';
    3、Pub包管理系统中的库  
        https://pub.dev/packages
        https://pub.flutter-io.cn/packages
        https://pub.dartlang.org/flutter/
        1、需要在自己想项目根目录新建一个pubspec.yaml
        2、在pubspec.yaml文件 然后配置名称 、描述、依赖等信息
        3、然后运行 pub get 获取包下载到本地  
        4、项目中引入库 import 'package:http/http.dart' as http; 看文档使用
*/
```

###### 01 Dart中导入自己本地库

```dart
import 'lib/Animal.dart';
main(){
  var a=new Animal('小黑狗', 20);
  print(a.getName());
}
```

###### 02 导入系统内置库 math库 

```dart
// import 'dart:io';
import "dart:math";
main(){
    print(min(12,23));
    print(max(12,25));   
}
```

###### 03 导入系统内置库实现请求数据httpClient

```dart
import 'dart:io';
import 'dart:convert';
void main() async{
  var result = await getDataFromZhihuAPI();
  print(result);
}
//api接口： http://news-at.zhihu.com/api/3/stories/latest
getDataFromZhihuAPI() async{
  //1、创建HttpClient对象
  var httpClient = new HttpClient();  
  //2、创建Uri对象
  var uri = new Uri.http('news-at.zhihu.com','/api/3/stories/latest');
  //3、发起请求，等待请求
  var request = await httpClient.getUrl(uri);
  //4、关闭请求，等待响应
  var response = await request.close();
  //5、解码响应的内容
  return await response.transform(utf8.decoder).join();
}
```

###### 04 关于 Async Await

```dart
/*
async和await
  这两个关键字的使用只需要记住两点：
    只有async方法才能使用await关键字调用方法
    如果调用别的async方法必须使用await关键字
async是让方法变成异步。
await是等待异步方法执行完成。
*/
void main() async{
  var result = await testAsync();
  print(result);
}
//异步方法
testAsync() async{
  return 'Hello async';
}
```

###### 05 Dart 导入Pub包管理系统中的库

```dart
/*
pub包管理系统:
1、从下面网址找到要用的库
        https://pub.dev/packages
        https://pub.flutter-io.cn/packages
        https://pub.dartlang.org/flutter/
2、创建一个pubspec.yaml文件，内容如下
    name: xxx
    description: A new flutter module project.
    dependencies:  
        http: ^0.12.0+2
        date_format: ^1.0.6
3、配置dependencies
4、运行pub get 获取远程库
5、看文档引入库使用
*/
import 'dart:convert' as convert;
import 'package:http/http.dart' as http;
import 'package:date_format/date_format.dart';
main() async {
  // var url = "http://www.phonegap100.com/appapi.php?a=getPortalList&catid=20&page=1";
  //   // Await the http get response, then decode the json-formatted responce.
  //   var response = await http.get(url);
  //   if (response.statusCode == 200) {
  //     var jsonResponse = convert.jsonDecode(response.body);
  //     print(jsonResponse);
  //   } else {
  //     print("Request failed with status: ${response.statusCode}.");
  //   }
    print(formatDate(DateTime(1989, 2, 21), [yyyy, '*', mm, '*', dd]));
}
```

###### 06 Dart库的重命名 Dart冲突解决

```dart
/*
1、冲突解决
当引入两个库中有相同名称标识符的时候，如果是java通常我们通过写上完整的包名路径来指定使用的具体标识符，甚至不用import都可以，但是Dart里面是必须import的。当冲突的时候，可以使用as关键字来指定库的前缀。如下例子所示：
    import 'package:lib1/lib1.dart';
    import 'package:lib2/lib2.dart' as lib2;
    Element element1 = new Element();           // Uses Element from lib1.
    lib2.Element element2 = new lib2.Element(); // Uses Element from lib2.
*/
import 'lib/Person1.dart';
import 'lib/Person2.dart' as lib;
main(List<String> args) {
  Person p1=new Person('张三', 20);
  p1.printInfo();
  lib.Person p2=new lib.Person('李四', 20);
  p2.printInfo();
}
```

###### 07 部分导入

```dart
/*
部分导入
  如果只需要导入库的一部分，有两种模式：
     模式一：只导入需要的部分，使用show关键字，如下例子所示：
      import 'package:lib1/lib1.dart' show foo;
     模式二：隐藏不需要的部分，使用hide关键字，如下例子所示：
      import 'package:lib2/lib2.dart' hide foo;      
*/
// import 'lib/myMath.dart' show getAge;
 import 'lib/myMath.dart' hide getName;
void main(){
//  getName();
  getAge();
}
```

###### 08 延迟加载

```dart
/*
延迟加载
    也称为懒加载，可以在需要的时候再进行加载。
    懒加载的最大好处是可以减少APP的启动时间。
    懒加载使用deferred as关键字来指定，如下例子所示：
    import 'package:deferred/hello.dart' deferred as hello;
    当需要使用的时候，需要使用loadLibrary()方法来加载：
    greet() async {
      await hello.loadLibrary();
      hello.printGreeting();
    }
*/
```

- pubspec.yaml

```yaml
name: xxx
description: A new flutter module project.
dependencies:
  http: ^0.12.0+2
  date_format: ^1.0.6
environment:
  sdk: '>=2.10.0 <3.0.0'
```

#### 15. Dart2.13之后的一些新特性

###### 01 Null safety 以及可空类型 非空断言

```dart
/*
  Null safety翻译成中文的意思是空安全。
  null safety 可以帮助开发者避免一些日常开发中很难被发现的错误，并且额外的好处是可以改善性能。
  Flutter2.2.0（2021年5月19日发布） 之后的版本都要求使用null safety。
  ? 可空类型
  ! 类型断言
*/
String? getData(apiUrl){
  if(apiUrl!=null){
    return "this is server data";
  }
  return null;
}
// void printLength(String? str){
//   // print(str!.length);
//   if (str!=null){
//     print(str.length);
//   }
// }

void printLength(String? str){
  try {
    print(str!.length); 
  } catch (e) {
     print("str is null"); 
  }
}

void main(args) {

//1、 ? 可空类型
  // int a=123;
  // print(a);
  // String username="张三";
  // print(username);
  // List<String> l1=["张三","李四","王五"];
  // print(l1);
  // int a=123;  //非空的int类型
  // a=null;  //A value of type 'Null' can't be assigned to a variable of type 'int'
  // String username="张三";  //非空的String类型
  // username=null;   //A value of type 'Null' can't be assigned to a variable of type 'String'.
  // String? username="张三";   // String?  表示username是一个可空类型
  // username=null;
  // print(username);
  // int? a=123;  //  int? 表示a是一个可空类型
  // a=null; 
  // print(a);
  // List<String> l1=["张三","李四","王五"];
  // l1=null;  //A value of type 'Null' can't be assigned to a variable of type 'List<String>'.
  // List<String>? l1=["张三","李四","王五"];
  // l1=null;  
  // print(l1);
  //调用方法
  // print(getData("http://www.itying.com"));
  // print(getData(null));
// ! 类型断言
  // String? str="this is str";
  // str=null;
  // print(str!.length);  
   //类型断言: 如果str不等于null 会打印str的长度，如果等于null会抛出异常
  //  printLength("str");
   printLength(null);
}
```

###### 02 late关键词

```dart
/*
Null safety翻译成中文的意思是空安全。
late 关键字主要用于延迟初始化。
*/
class Person {
  late String name;
  late int age;
  void setName(String name, int age) {
    this.name = name;
    this.age = age;
  }
  String getName() {
    return "${this.name}---${this.age}";
  }
}

void main(args) {
  Person p = new Person();
  p.setName("张三", 20);
  print(p.getName());
}
```

###### 03 late接口

```dart
/*
和Java一样，dart也有接口，但是和Java还是有区别的。
  首先，dart的接口没有interface关键字定义接口，而是普通类或抽象类都可以作为接口被实现。
  同样使用implements关键字进行实现。
  但是dart的接口有点奇怪，如果实现的类是普通类，会将普通类和抽象中的属性的方法全部需要覆写一遍。
  而因为抽象类可以定义抽象方法，普通类不可以，所以一般如果要实现像Java接口那样的方式，一般会使用抽象类。
  建议使用抽象类定义接口。
*/
/*
定义一个DB库 支持 mysql  mssql  mongodb
mysql  mssql  mongodb三个类里面都有同样的方法
*/
abstract class Db{   //当做接口   接口：就是约定 、规范
    late String uri; //数据库的链接地址    
    add(String data);
    save();
    delete();
}

class Mysql implements Db{
  @override
  String uri;
  Mysql(this.uri);
  @override
  add(data) {
    // TODO: implement add
    print('这是mysql的add方法'+data);
  }

  @override
  delete() {
    // TODO: implement delete
    return null;
  }

  @override
  save() {
    // TODO: implement save
    return null;
  }

  remove(){    
  }  
}

class MsSql implements Db{
  @override
  late String uri;
  @override
  add(String data) {
    print('这是mssql的add方法'+data);
  }

  @override
  delete() {
    // TODO: implement delete
    return null;
  }
  
  @override
  save() {
    // TODO: implement save
    return null;
  }
}
main() {
  Mysql mysql=new Mysql('xxxxxx');
  mysql.add('1243214');  
}
```

###### 04 required 

```dart
/*
Null safety翻译成中文的意思是空安全。
required翻译成中文的意思是需要、依赖
required关键词:
    最开始 @required 是注解 
    现在它已经作为内置修饰符。
    主要用于允许根据需要标记任何命名参数（函数或类），使得它们不为空。因为可选参数中必须有个 required 参数或者该参数有个默认值。
*/
String printUserInfo(String username, {int age=10, String sex="男"}) {//行参    
  return "姓名:$username---性别:$sex--年龄:$age";
}

String printInfo(String username, {required int age, required String sex}) {//行参    
  return "姓名:$username---性别:$sex--年龄:$age";
}

void main(args) {
    print(printUserInfo('张三'));
    print(printUserInfo('张三',age: 20,sex: "女"));
    //age 和 sex必须传入
    print(printInfo('张三',age: 22,sex: "女"));
}
```

###### 05 required 命名参数 

```dart
/*
Null safety翻译成中文的意思是空安全。
required翻译成中文的意思是需要、依赖
required关键词:
    最开始 @required 是注解
    现在它已经作为内置修饰符。
    主要用于允许根据需要标记任何命名参数（函数或类），使得它们不为空。因为可选参数中必须有个 required 参数或者该参数有个默认值。
*/
//表示 name 和age 是必须传入的命名参数
class Person {
  String name;
  int age;
  Person({required this.name,required this.age});  //表示 name 和age 必须传入
  String getName() {
    return "${this.name}---${this.age}";
  }
}

void main(args) {
   Person p=new Person(
     name: "张三",
     age: 20
   );
   print(p.getName());
}
```

###### 06 required  命名参数 命名可选参数

```dart
/*
Null safety翻译成中文的意思是空安全。
required翻译成中文的意思是需要、依赖
required关键词:
    最开始 @required 是注解
    现在它已经作为内置修饰符。
    主要用于允许根据需要标记任何命名参数（函数或类），使得它们不为空。因为可选参数中必须有个 required 参数或者该参数有个默认值。
*/
// name 可以传入也可以不传入   age必须传入
class Person {
  String? name;   //可空属性
  int age;
  Person({this.name,required this.age});  //表示 name 和age 必须传入
  String getName() {
    return "${this.name}---${this.age}";
  }
}

void main(args) {
   Person p=new Person(
     name: "张三",
     age: 20
   );
   print(p.getName());  //张三---20

  Person p1=new Person(    
     age: 20
   );
   print(p1.getName());  //null---20
}
```

#### 16. dart 性能优化之常量、常量构造函数

###### 01 回顾Dart常量

```dart
/*
Dart 常量: final 和 const修饰符  
  const 声明的常量是在编译时确定的，永远不会改变
  final 声明的常量允许声明后再赋值，赋值后不可改变，final 声明的变量是在运行时确定的;
  final不仅有const的编译时常量的特性，最重要的它是运行时常量，并且final是惰性初始化，即在运行时第一次使用前才初始化
*/
void main(){    
//const常量
//const PI=3.14;
// PI=3.14159;  //const定义的常量没法改变
//print(PI);
// final 常量
// final PI=3.14;
// print(PI);
//final和const区别：final 可以开始不赋值 只能赋一次 ; 而final不仅有const的编译时常量的特性，最重要的它是运行时常量，并且final是惰性初始化，即在运行时第一次使用前才初始化
 final a;
 a=13;
//  a=14;
 print(a);
final d=new DateTime.now();
}
```

###### 02 Dart中的const  identical 函数

```dart
/*
dart:core 库中identical 函数的用法介绍如下。
用法:
bool identical(
   Object? a,    
   Object? b   
)
检查两个引用是否指向同一个对象。
var o = new Object();
  var isIdentical = identical(o, new Object()); // false, different objects.
  print(isIdentical);

  isIdentical = identical(o, o); // true, same object
  print(isIdentical);

  isIdentical = identical(const Object(), const Object()); // true, const canonicalizes
  print(isIdentical);

  isIdentical = identical([1], [1]); // false
  print(isIdentical);

  isIdentical = identical(const [1], const [1]); // true
  print(isIdentical);

  isIdentical = identical(const [1], const [2]); // false
  print(isIdentical);
  
  isIdentical = identical(2, 1 + 1); // true, integers canonicalizes
  print(isIdentical);
*/

void main(){
  // var o1 = new Object();
  // var o2 = new Object();
  // print(identical(o1,o2));  //false  不共享存储空间
  // print(identical(o1,o1));   //true 共享存储空间
  // var o1 = Object();
  // var o2 = Object();
  // print(identical(o1,o2));  //false
  // print(identical(o1,o1));  //true
  //表示实例化常量构造函数
  //o1 和 o2共享了存储空间
  // var o1 = const Object();
  // var o2 = const Object();
  // print(identical(o1,o2));  //true 共享存储空间
  // print(identical(o1,o1));  //true 共享存储空间
  // print(identical([2],[2])); //false
  // var a=[2];
  // var b=[2];
  // print(identical(a,b)); //false 不共享存储空间
  // print(identical(const [2],const [2])); //true
  const a=[2];
  const b=[2];
  print(identical(a,b)); //true 共享存储空间
  const c=[2];
  const d=[3];
  print(identical(c,d)); //false  不共享存储空间
}
// 发现：const关键词在多个地方创建相同的对象的时候，内存中只保留了一个对象
// 共享存储空间条件：1、常量   2、值相等
```

###### 03 Dart普通构造函数

```dart
class Container{
  int width;
  int height;
  Container({required this.width,required this.height});
}

void main(){
  var c1=new Container(width: 100,height: 100);
  var c2=new Container(width: 100,height: 100);
  print( identical(c1, c2));  //false   c1和c2在内存中存储了2份
}
```

###### 04 Dart常量构造函数

```dart
/*
常量构造函数总结如下几点：
  1、常量构造函数需以const关键字修饰
  2、const构造函数必须用于成员变量都是final的类
  3、如果实例化时不加const修饰符，即使调用的是常量构造函数，实例化的对象也不是常量实例
  4、实例化常量构造函数的时候，多个地方创建这个对象，如果传入的值相同，只会保留一个对象。
  5、Flutter中const 修饰不仅仅是节省组件构建时的内存开销，Flutter 在需要重新构建组件的时候，由于这个组件是不应该改变的，重新构建没有任何意义，因此 Flutter 不会重建构建 const 组件  
*/

//常量构造函数
class Container{
  final int width;
  final int height;
  const Container({required this.width,required this.height});
}

void main(){
  var c1=Container(width: 100,height: 100);
  var c2=Container(width: 100,height: 100);
  print(identical(c1, c2)); //false
  
  var c3=const Container(width: 100,height: 100);
  var c4=const Container(width: 100,height: 100);
  print(identical(c3, c4)); //true

  var c5=const Container(width: 100,height: 110);
  var c6=const Container(width: 120,height: 100);
  print(identical(c5, c6)); //false
}
// 实例化常量构造函数的时候，多个地方创建这个对象，如果传入的值相同，只会保留一个对象。
```

