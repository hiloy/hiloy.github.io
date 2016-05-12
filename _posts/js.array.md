## js 数组总结

Javascript中的数组可以包含任何数据类型的有序集合，通过索引来访问每个元素，数组本质上是对象

### 获取Array的长度通过length属性
举例：
var arr = [1,2,3];
arr.length; //输出数组长度3

注意：给数组length属性赋值会改变数组长度
### indexOf 搜索指定元素的位置
举例：
var arr = [10, 20, '30', 'xyz'];
arr.indexOf(10); // 元素10的索引为0
arr.indexOf(20); // 元素20的索引为1
arr.indexOf(30); // 元素30没有找到，返回-1
arr.indexOf('30'); // 元素'30'的索引为2

注意'30'是字符串非数字，数组不存在时返回-1

### slice 截取数组
说明：返回新的数组，不更改原数组
举例：
var arr = [10,20,30];
arr.slice(0,2); //从0位开始截取两个元素，返回[10,20]
arr.slice(2); //从2位置截取到数组末尾，返回[30]
arr.slice(3); //从3位置截取到数组末尾，超出数组长度，返回空数组[]
arr.slice(); //不带参数返回数组全部元素

### push 和 pop
说明：push从数组末尾插入元素，pop从数组末尾删除元素
举例：
var arr = [10.20,30];
arr.push('China'); //插入一个元素
arr.push('China','Google'); //插入两个元素
arr.pop(); //从数组末尾删除元素，并返回删除元素
arr.pop('Google'); //从末尾删除元素，传入参数直接扔弃

### unshift 和 shift
说明：unshift从数组头部插入元素，shift从数组头部删除元素
举例：
var arr = [10,20,30];
arr.unshift(40); //数组头部插入一个元素
arr.unshift(40,50); //数组头部插入两个元素
arr.shift(); //从数组头部删除一个元素
arr.shift('30'); //从数组头部删除一个元素，传入参数直接扔弃

### sort
说明：给数组元素排序,默认修改数组元素的索引位置
举例：
var arr = [30,10,20];
arr.sort(); //数组排序，索引位置发生变化，输出[10,20,30]

### reverse
说明：数组元素顺序翻转
var arr = [10,20,30];
arr.reverse(); //数组元素顺序翻转，输出为：[30,20,10]

### splice
说明：从数组中截取元素，插入元素，直接影响数组
var arr = [10,20,30];
//既删除又插入元素
arr.splice(0,1,'China','Google'); //返回删除的数组元素，插入传入的元素
//只删除不插入
arr.splice(0,1); //返回删除的数组元素
//直插入不删除
arr.splice(2,0,'China','Google'); //返回删除元素，此时的删除元素为空数组

### concat
说明：连接两个数组，返回新的数组，原数组不受影响
var arr = [10,20,30];
var arr2 = [40,50,60];
var arr3 = [70,80];
arr.concat(arr2).concat(arr3); //连接数组，输出：[10,20,30,40,50,60,70,80]

注意：concat参数可以为任意数据类型，将数组拆分后拼接在一起组成新的数组返回
### join
说明：将数组元素按照给定的元素连接起来，返回值为字符串，不影响原数组
var arr = [10.20,30];
arr.join('-'); //返回新的数组，输出为："10-20-30"

### 多为数组
说明：数组的元素是数组组成多维数组
举例：
var arr = [1,[2,[3]]]; //输出多维数组观察效果