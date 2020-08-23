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