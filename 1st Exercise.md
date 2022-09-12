
```ts
/* Module 2: Declare variable types in TypeScript
   Lab start  */

/*  EXERCISE 1
    TODO: Modify the code to add types to the variable declarations. 
    The resulting JavaScript should look the same as the original example when you're done. */

let firstName;
let lastName;
let fullName;
let age;
let ukCitizen;

firstName = 'Rebecca';
lastName = 'Smith';
age = 42;
ukCitizen = false;
fullName = firstName + " " + lastName;

if (ukCitizen) {
    console.log("My name is " + fullName + ", I'm " + age + ", and I'm a citizen of the United Kingdom.");
} else {
    console.log("My name is " + fullName + ", I'm " + age + ", and I'm not a citizen of the United Kingdom.");
}

/* EXERCISE 2
   TODO: You can use types to ensure operation outcomes. Run the code as is and then modify 
   it to have strongly typed variables. Then, address any errors you find so that the result 
   returned to a is 12. */


let x: number;
let y: number;
let a: number;

x = 5;
y = 7;
a = x + y;

console.log(a);

/* EXERCISE 3
   TODO: In the following code, implement an enum type called Season that represents 
   the constants "Fall", "Winter", "Spring", and "Summer". Then, update the function so 
   you can pass in the season by referencing an item in the enum, for example 
   Season.Fall, instead of the literal string "Fall". */

   
enum Season {
    Fall = 'Fall',
    Winter = 'Winter',
    Spring = 'Spring',
    Summer = 'Summer'
};

function whichMonths(season: Season) {

    let monthsInSeason: string = '';

    switch (season) {
        case "Fall":
            monthsInSeason = "September to November";
            break;
        case "Winter":
            monthsInSeason = "December to February";
            break;
        case "Spring":
            monthsInSeason = "March to May";
            break;
        case "Summer":
            monthsInSeason = "June to August";
    }

    return monthsInSeason;
}

console.log(Season.Spring + ' = ' + whichMonths(Season.Spring));


/* EXERCISE 4
   TODO: Declare the array as the type to match the type of the items in the array. */

   let randomNumbers: number[] = [];
   let nextNumber;
   
   for (let i = 0; i < 10; i++) {
       nextNumber = Math.floor(Math.random() * (100 - 1)) + 1;
       randomNumbers.push(nextNumber);
   }
   
   console.log(randomNumbers);
   
   
```



<details><summary><b>Output</b></summary>

```ts
"use strict";
/* Module 2: Declare variable types in TypeScript
   Lab start  */
/*  EXERCISE 1
    TODO: Modify the code to add types to the variable declarations.
    The resulting JavaScript should look the same as the original example when you're done. */
let firstName;
let lastName;
let fullName;
let age;
let ukCitizen;
firstName = 'Rebecca';
lastName = 'Smith';
age = 42;
ukCitizen = false;
fullName = firstName + " " + lastName;
if (ukCitizen) {
    console.log("My name is " + fullName + ", I'm " + age + ", and I'm a citizen of the United Kingdom.");
}
else {
    console.log("My name is " + fullName + ", I'm " + age + ", and I'm not a citizen of the United Kingdom.");
}
/* EXERCISE 2
   TODO: You can use types to ensure operation outcomes. Run the code as is and then modify
   it to have strongly typed variables. Then, address any errors you find so that the result
   returned to a is 12. */
let x;
let y;
let a;
x = 5;
y = 7;
a = x + y;
console.log(a);
/* EXERCISE 3
   TODO: In the following code, implement an enum type called Season that represents
   the constants "Fall", "Winter", "Spring", and "Summer". Then, update the function so
   you can pass in the season by referencing an item in the enum, for example
   Season.Fall, instead of the literal string "Fall". */
var Season;
(function (Season) {
    Season["Fall"] = "Fall";
    Season["Winter"] = "Winter";
    Season["Spring"] = "Spring";
    Season["Summer"] = "Summer";
})(Season || (Season = {}));
;
function whichMonths(season) {
    let monthsInSeason = '';
    switch (season) {
        case "Fall":
            monthsInSeason = "September to November";
            break;
        case "Winter":
            monthsInSeason = "December to February";
            break;
        case "Spring":
            monthsInSeason = "March to May";
            break;
        case "Summer":
            monthsInSeason = "June to August";
    }
    return monthsInSeason;
}
console.log(Season.Spring + ' = ' + whichMonths(Season.Spring));
/* EXERCISE 4
   TODO: Declare the array as the type to match the type of the items in the array. */
let randomNumbers = [];
let nextNumber;
for (let i = 0; i < 10; i++) {
    nextNumber = Math.floor(Math.random() * (100 - 1)) + 1;
    randomNumbers.push(nextNumber);
}
console.log(randomNumbers);

```


</details>


<details><summary><b>Compiler Options</b></summary>

```json
{
  "compilerOptions": {
    "strict": true,
    "noImplicitAny": true,
    "strictNullChecks": true,
    "strictFunctionTypes": true,
    "strictPropertyInitialization": true,
    "strictBindCallApply": true,
    "noImplicitThis": true,
    "noImplicitReturns": true,
    "alwaysStrict": true,
    "esModuleInterop": true,
    "declaration": true,
    "experimentalDecorators": true,
    "emitDecoratorMetadata": true,
    "target": "ES2017",
    "jsx": "react",
    "module": "ESNext",
    "moduleResolution": "node"
  }
}
```


</details>

**Playground Link:** [Provided](https://www.typescriptlang.org/play?#code/PQKgBAsg9gJgrgGwKZgEwC4wBEkGMECGATigG7ECWBARsmAC4CeADkgM5gUB2YAKi0gDKuIhWb0AUGGkAZGmDb1i9aSGASJoaQFEAGtoBKAYQCSg7WACMU6XwDyWO5mgwKAM0YMAFilywU9FBgBDAwDAIcgd5klDR0MHiERAT0FFBcbAB0YDbSvD5gJGyIqVwA5mAAUgTkwqLiCl5QiGEIUFAA1tEKBAC2KASRBVCiZdwECGBIAB59zHQA7j48jM0A5CRgMOlI2WoayCpuFESKAHJ9SADcEodghOeXN3duiAgX-c9IKgRl17ffMBwDpGCipABeSC4Nwkx1O9A+KAAvGA1gYkNQ8LgCGtnoMEZcwCi1oJemCvLiJL9kWAACyoG7A0EQqFEsBuCZsf6vBDvQkouGPfpgADUYAARBLRfd8YiYe4wAAKJlgiiQrgASjAAG9cmA-BkoMhMm0yorxRBPFxCRQOJKxTy+cKxeKADRgExrXpSsXU6Vu4JcMKe70EfWq9VgKBuboAVS4YKQYQA0twytteplxRqbgBfKYILk6vUGthG3am82WsDW4W2n3st6I-3ukMNv0u90EIMer01qA-cMsnjRuMJ+hJsCp8oZrM5iS5jRaPSGUzmNC5XgOJxgACazX13aBRaYrEiQShxU2UFYyVS6SjcHofn6WTABjgPHoBT8CWCHHrbswm-VlelgdxPFyMEGCCLwahQRQiHSMoEE8U9J3IUQ4nYbJ8ihLtQiKDhu08JAiCQ04wFWOB2W4MIy28FJuiKEoclsEh6DgIguEnKIw3rSxUD2dQDkBaZMC4OBekxIgvhURgJKkmS5OCRTpLImFpjZABWG5PBRAB2G4wxRLSxUYGFS3LE0oDNAh500cAV2MMwLAAZk3bdMBML8CjcI02gWNN9X8d0KF6eYkH6Lgfh4KEpPCVhD15SdBCQQYH2-JiSGYIooXoDhchAkKMiUGK7QAMQmBAA3FAB1bgJyIWrBFytMAyAiVBCk-pmtw5Z3TgZgYBSAI-M-XB7x4Bjcmow8eGYQYAN8hD0rLHhqE8Eg3DIqFcGCo9E29bhuni3p3X8ogplmCK6FyNKMq4TIqt5MLSvSsJR2KhBE2SSZEOC8UXpq4SNFsCQzrAB71uLWwwGBtk1mBtZXT1BqYrIxH0aalG9Va0RykR-G01xuHut6XqiZ6si1gXGFXi4Sa0h4JYKFwLxoBirw2EVLlHswaH0i1XU9TuMCubYHzBa4TAAcJ4lKT1NggufLwlT59bhb1OHsSLIHqvFdBtbh2xxe-SWuGltlxTS8QopkmCwDOKBSHtsjxRuE2vbAagSAIDpPe93WUHqxr3aN72TbN7mpbWh8UXFHBcDdq6ogqjEiDgYhGA942vd99KA7zw89eJ8pDeLuHo4tq2E4gYh2cd+uc8DyPpAL-3W5N4Ouup5qI7b6Rq9jx7rcqT8AiCABBOAyjgRRc7hxc9Q4rieGHy24+hBcNCs41K2lzIy4qMU1kR6VWfZznzcVQ-j41BzHLAZy1wsWlPMcTAk6SMaBnIghPCDG6OhR2vQUiN2KiAr6BQjrLW6MQZIjBQa5DuMkIMUBehnCUmRNgakZIAG0AC6bIiGtzuDxaYCJsGyVyLkS6So7gUDZAABiuJwMAAAeKwrDOAihFFrb2FCqHqSuiieu35MhuDaCMRU4ivCZDQRmRUWpwCKksMw5hYAAC0VgH7SksF3diQEMFYJEVkZg88vCKiEaYmS85bCLnBrYPeFZbKKkUSY6hbB7HSFyEAA)
      
