# TypeScript 是什么?
TypeScript 是一种由微软开发的自由和开源的编程语言。它是 JavaScript 的一个超集，而且本质上向这个语言添加了可选的静态类型和基于类的面向对象编程。
TypeScript 提供最新的和不断发展的 JavaScript 特性，包括那些来自 2015 年的 ECMAScript 和未来的提案中的特性，比如异步功能和 Decorators，以帮助建立健壮的组件。
# TypeScript 初体验
新建一个 `hello.ts` 文件，并输入以下内容：
```typescript
function greet(person: string) {
  return 'Hello, ' + person;
}
console.log(greet("TypeScript"));
```
然后执行 tsc hello.ts 命令，之后会生成一个编译好的文件 hello.js：
```typescript
function greet(person) {
  return 'Hello, ' + person;
}
console.log(greet("TypeScript"));
```
# TypeScript 基础类型
# Boolean类型
``` typescript
let isLoading: boolean = false;
console.log('🚀 => isLoading:', isLoading);
​```typescript
# Number类型
​```typescript
let age: number = 23;
console.log('🚀 => age:', age);
​```typescript
# String类型
​```typescript
let userName: string = 'typeScript';
console.log('🚀 => userName:', userName);
```
# Symbol类型
```typescript
const sym = Symbol();
let obj = {
  [sym]: "semlinker",
};
console.log('🚀 => obj[sym]:', obj[sym]);
```
# Array类型
```typescript
let numbers: number[] = [1, 3, 4, 5]
console.log('🚀 => numbers:', numbers);
let numberList: Array<number> = [1, 24, 666, 44] // Array<number>泛型语法
console.log('🚀 => numberList:', numberList);
let strArray: Array<number | string> = [434, 4, '45', '423', 97]
console.log('🚀 => strArray:', strArray);
```
# Enum 枚举类型 
使用枚举可以清晰地表达意图或创建一组有区别的用例。 TypeScript 支持数字的和基于字符串的枚举。
字符串枚举 使用字符串枚举。在一个字符串枚举里，每个成员都必须用字符串字面量，或另外一个字符串枚举成员进行初始化。
```typescript
enum requestEnum {
  GET = "GET",
  POST = "POST",
  PATCH = "PATCH",
  PUT = "PUT",
  DELETE = "DELETE",
}
let request: requestEnum = requestEnum.GET; 
console.log('🚀 => request:', request);
```
数字枚举  默认情况下，NORTH 的初始值为 0，其余的成员会从 1 开始自动增长。换句话说，Direction.SOUTH 的值为 1，Direction.EAST 的值为 2，Direction.WEST 的值为 3。
```typescript
enum Direction {
  NORTH,
  SOUTH,
  EAST,
  WEST,
}
let dir: Direction = Direction.NORTH; 
console.log('🚀 => dir:', dir);
```
常量枚举 使用 const 关键字修饰的枚举，常量枚举会使用内联语法，不会为枚举类型编译生成任何 JavaScript
```typescript
const enum azimuth {
  TOP,
  RIGHT,
  BOTTOM,
  LEFT,
}
let azi: azimuth = azimuth.TOP;
console.log('🚀 => azi:', azi);
```
异构枚举 异构枚举的成员值是数字和字符串的混合
```typescript
enum strEnum{
  test,
  str,
  name = 'test',
  age = '89',
  weight = 220,
}
console.log('🚀 => strEnum.age:', strEnum.age); //异构枚举
console.log('🚀 => strEnum.weight:', strEnum.weight); //异构枚举
console.log('🚀 => strEnum.test:', strEnum.test); //异构枚举
```
Any 类型 在 TypeScript 中，任何类型都可以被归为 any 类型。这让 any 类型成为了类型系统的顶级类型（也被称作全局超级类型）
```typescript
let strName: any = 19;
strName = false;
strName = '石头人'
console.log('🚀 => strName:', strName);
Unknown 类型 所有类型都可以赋值给 any，所有类型也都可以赋值给 unknown
```


