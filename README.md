# Typescript

## Types

### boolean
```typescript
const isCompleted: boolean = true;
```
### number
```typescript
const decimal: number = 6;
const integer: number = 6.11;
```

### string
```typescript
const str: string = "My string";
```

### undefined
```typescript
const u: undefined = undefined;
```

### null
```typescript
const n: null = null;
```

### void
```typescript
const greetUser= (): void  => {
    alert("hi")
}
```

### void
```typescript
const greetUser= (): void  => {
    alert("hi")
}
```

### array
```typescript
const list:number[] = [1,2,3]; 
const list2: Array<number> = [1,2,3]; // generic type
```

### tuple
```typescript
// multiple lines
let x:[string, number];
x = ["hello", 10];

// one line
const y:[string, number] = ["hello", 10]

```
### any
```typescript
let x :[any, any] = ["str", 10];
let y :Array<any> = ["str", 10];
let z:any = "any"
```

### enum
```typescript
enum Directions{
    Up,
    Down,
    Left,
    Right = 10
}
Directions.Up //0
Directions.Down //1
Directions[2] // Left
Directions[10] //Right

enum links{
    yt = "youtube.com",
    fb = "fb.com"
}
console.log(links.yt)
console.log(links["fb.com"])
```

### never
```typescript
const error = ():never => {
    throw new Error("error here")
}
const infinitiveLoop = ():never => {
    while(true){}
}

```

### object
```typescript
    const myObj:object = {a:"a"};
```

### Multiple types
```typescript
    let id:string|number = 1;
    let id:string|number = "2";
```

### Custom type
```typescript
    type MyType = string;
    let id:MyType = "12" 
```

## Function example
```typescript
    const sum = (arg1:number, arg2:number):number => arg1+arg2;
```

## Object example
```typescript
   const myObj:{name:string, age:number} = {name:"John", age:20};

    // create type for persons
    type Person = {
        name:string,
        age:number,
        nickName?:string,
    }
    const user1:Person = {name:"James", age:20, nickName:"James123"} 
    const user2:Person = {name:"Smith", age:20} 
```

## Class example
```typescript
    class User {
        public name:string;
        private nickName:string;
        protected age:number;
        readonly pass:string;
        position="developer";
        
        constructor(name:string, nickName:string, age:number, pass:string, position?:string) {
            this.name = name;
            this.nickName = nickName;
            this.age = age;
            this.pass = pass;
        }
    }

const myUser = new User("John", "john123", 20, "123");
```
## Class with static attribute and inheritance example
```typescript
   
class User {
  static secret = 123;
  private nickName:string;

  constructor(public name:string, public age:number){}   

  getFull():string {
    return this.name+User.secret
  }

}
class SecondUser extends User{
    name:string = "second user";

    constructor(age: number){
        super(name, age)
    }

}

const user = new User("aaa", 10);
const secondUser = new SecondUser(100)
```
## abstract Class example
```typescript
abstract class User{
    constructor(public name:string, public age:number) {}
    
    greet():void{
        console.log(this.name)
    }
    abstract getPass():string
}

class MyUser extends User{
    getPass(): string{
        return this.age+this.name
    }
}
```

## interface example
```typescript
interface User{
    name:string,
    age:number
}
const user: User = {name:"John", age:22}


interface User2{
    name:string,
    [propName:string]: any // could contain other props
}
const user2:User2 = {
    name:"user2",
    secondName:"user2sn"
}


interface User3 {
    name:string,
    getPass():string
}
class MyClass implements User3{
    name:string = "userName";
    getPass():string{
        return "string"
    }
}
```
