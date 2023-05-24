title: "Testing"
date: 2015-03-30 13:44:17
tags: Test
---

## Just some testing

This is a paragraph. More text here. The quick brown fox jumps over the lazy dog. The quick brown fox jumps over the lazy dog. The quick brown fox jumps over the lazy dog. The quick brown fox jumps over the lazy dog. The quick brown fox jumps over the lazy dog. The quick brown fox jumps over the lazy dog. The quick brown fox jumps over the lazy dog. The quick brown fox jumps over the lazy dog.

Here are some code snippst: `var myname = 'Tony Liu';`, `#define age 24;`

More codes here:

``` cpp
    #include<stdio.h>

    int main() {
        int n, first = 0, second = 1, next, c;

        printf("Enter the number of terms\n");
        scanf("%d",&n);

        printf("First %d terms of Fibonacci series are :-\n",n);

        for ( c = 0 ; c < n ; c++ ) {
            if ( c <= 1 )
                next = c;
            else {
                next = first + second;
                first = second;
                second = next;
            }
            printf("%d\n",next);
        }
        return 0;
    }
```

And for the math mode: $x^2+3x+1=4$,

Some more complicate ${n! \over k!(n-k)!} = {n \choose k}$

Production? Yes: $$\prod_{i=0}^n \frac{1}{i^2}$$

Limits? Yes: $$\lim_{n \rightarrow +\infty} \frac{1}{n(n+1)}$$

However, it seems doesn't support equations by default, need time to check how to enable it.

### headings

__Strong__, **Strong**

~~Aha this need to be delete~~

Oh should be some list:
- Hello world
- Print Integer
- Addtion
- Odd or Even
- Add, substract, multiply
