# projecteuler-2-ts
```
// Solution:
const LIMIT: number = 4000000;

const isEven = (n: number) => n % 2 === 0;
const last2 = (arr: any[]) => arr.slice(-2);
const sum = (arr: number[]) => arr.reduce((acc, curr) => acc + curr, 0);

const fibo = (limit: number, a?: number[]) => {
  if (!a) {
    return fibo(limit, [1, 2]);
  }
  const s = sum(last2(a));
  if (s > limit) {
    return sum(a.filter(isEven));
  }

  return fibo(limit, [...a, s]);
};

// Display Result
console.log(fibo(LIMIT));
```

[Edit in StackBlitz next generation editor ⚡️](https://stackblitz.com/~/github.com/honorablemention/projecteuler-2-ts)
