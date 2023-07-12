# MKL 函数

## [BLAS 1级例程(向量-向量操作)](https://blog.csdn.net/qq_39036287/article/details/106753802)

## [MKL学习--基本操作C++实现](https://blog.csdn.net/zb1165048017/article/details/70216994)

* 主要使用实数域的操作、也就是说关注单精度float类型的 s 和双精度 double 类型的 d

* 主要流程，使用 mkl_malloc 申请内存，

* 使用 mkl_free 释放内存

* VS 中, 输入 cblas_s 以后, 会自动补全所有单精度操作函数

* axpby 意思是 a*x 加 b *y

* 函数有两种，一种是有返回值、一种无返回值，只能看函数的声明是 void 还是 float 或者 double 类型即可。

## [void main 和 int main 有什么区别](https://blog.csdn.net/z1521985226/article/details/122524126)

int main返回int类型的数据，void main不返回。

但是在C语言推荐写法中，建议使用int main，因为在有的编译器虽然viod main可以通过编译，但在其他编译器就会报错。为了代码拥有更好的可移植性，一般写int main。

至于什么时候需要哪种写法，没必要较真。可以一律都写成 int main ，然后在方法体中最后加个return 0 ；就行了，这样写基本上所有的编译器都可以通过。
