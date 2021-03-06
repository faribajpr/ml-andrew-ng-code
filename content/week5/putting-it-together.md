---
title: "Putting It Together"
date: 2020-10-11T19:45:27+03:30
draft: false
weight: 70
---

ابتدا معماری شبکه خود را انتخاب کنید!

لایه های شبکه عصبی خود را انتخاب کنید،
از جمله اینکه چند گره پنهان در هر لایه و در کل چند لایه می‌خواهد داشته باشید.

- تعداد گره های ورودی = ابعاد ویژگی های $x^{(i)}$
- تعداد گره های خروجی = تعداد کلاس ها (طبقه بندی ها)
- تعداد گره های پنهان در هر لایه = معمولا هر چه بیشتر بهتر (افزایش تعداد گره های پنهان باید با هزینه محاسبه آن ها تعادل داشته باشد)
- پیش فرض ها: ۱ لایه پنهان، اگر بیش از ۱ لایه پنهان دارید پیشنهاد می‌شود که در هر لایه پنهان تعداد گره یکسانی داشته باشید.

### آموزش یک شبکه عصبی

1. مقدار دهی اولیه تصادفی وزن ها
2. برای پیاده سازی <span class="top-dict" data-tipso="forward propagation">انتشار به جلو</span>، محاسبه $h_\Theta(x ^{(i)})$ برای هر $x ^{(i)}$
3. پیاده سازی تابع هزینه
4. پیاده سازی <span class="top-dict" data-tipso="backpropagation">پس انتشار</span> برای محاسبه مشتقات جزئی
5. استفاده از بررسی گرادیان برای اینکه مطمئن شویم پس انتشار کار می‌کند، و بعد از آن توقف بررسی گرادیان.
6. استفاده از گرادیان کاهشی یا یک  تابع توکار بهینه سازی برای به حداقل برساندن تابع هزینه با استفاده از وزن های داخل تتا

هنگام استفاده از انتشار به جلو و پس انتشار  در هر <span class="top-dict" data-tipso="training example">نمونه آموزشی</span> حلقه می‌زنیم:

<div align="left">

```
,for i = 1:m
   Perform forward propagation and backpropagation using example (x(i),y(i))
   Get activations a(l) and delta terms d(l) for l = 2,...,L
```

</div>


تصویر زیر به ما شهودی از آنچه که در حین پیاده سازی شبکه عصبی اتفاق می‌افتد می‌دهد:
![image4.png](../images/image4.png?width=35pc)

در حالت ایده آل، می‌خواهیم:
$$
h_\Theta (x^{(i)}) \approx  y^{(i)}
$$

که این یعنی تابع هزینه ما به حداقل می‌رسد، اما به خاطر داشته باشید که $J(\Theta)$ محدب نیست،
که بنابراین می‌توانیم به جای آن در مینیمم محلی قرار بگیریم.

