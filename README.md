# 颜廷举

#include <stdio.h>

// 递归函数计算斐波那契数列
int fibonacci(int n) {
    if (n == 0)
        return 0;
    if (n == 1)
        return 1;
    return fibonacci(n - 1) + fibonacci(n - 2);
}

int main() {
    int n = 10;  // 这里可以修改n的值来获取不同位置的斐波那契数
    int result = fibonacci(n);
    printf("The %d - th Fibonacci number is %d\n", n, result);
    return 0;
}
