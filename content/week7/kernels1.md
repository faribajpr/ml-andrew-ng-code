---
title: " کرنل ها (قسمت اول)"
date: 2020-11-03T11:24:39+03:30
draft: false
weight: 40
---

کرنل ها به ما این اجازه را می دهند تا با استفاده از ماشین بردار پشتیبان، طبقه بندی کننده های پیچیده و غیرخطی بسازیم.

با توجه به x ، ویژگی جدید را بسته به نزدیکی به نقاط عطف $l^{(3)}, l^{(2)}, l^{(1)}$ محاسبه کنید.

برای انجام این کار ، ما "شباهت" x و برخی از نقاط عطف \$l^{(i)}\$ را پیدا می کنیم.

$$
f_i=similarity(x,l^{(i)})=exp(-\frac{||x-l^{(i)}||^2}{2\sigma^2})
$$

به این تابع "شباهت" کرنل گاوسی گفته می شود. این یک نمونه خاص از کرنل است.

تابع شباهت را می توان به صورت زیر نیز نوشت:

$$
f_i=similarity(x,l^{(i)})=exp(-\frac{\sum_{j=1}^{n} (x_j - l_j^{(i)})^2}{2\sigma^2})
$$

تابع شباهت دو ویژگی دارد:

$$
if \hspace{0.3cm} x\approx l^{(i)}, then \hspace{0.3cm} f_i=exp(-\frac{\approx 0^2}{2\sigma^2})\approx 1
$$

$$
if \hspace{0.3cm} x  \hspace{0.15cm} is \hspace{0.15cm} far \hspace{0.15cm}  from \hspace{0.15cm} l^{(i)}, then \hspace{0.3cm} f_i=exp(-\frac{(large \hspace{0.15cm} number)^2}{2\sigma^2})\approx 0
$$

به عبارت دیگر، اگر x و نقطه عطف نزدیک به هم باشند، در این صورت شباهت نزدیک به 1 خواهد بود، و اگر x و نقطه عطف از یکدیگر دور باشند ،
شباهت نزدیک به 0 خواهد بود.
هر نقطه عطف ویژگی های فرضیه ما را به ما می دهد:

$$
l^{(1)} \rightarrow f_1
$$

$$
l^{(2)} \rightarrow f_2
$$

$$
l^{(3)} \rightarrow f_3
$$

$$
...
$$

$$
h_\Theta(x)= \Theta_1f_1+\Theta_2f_2+\Theta_3f_3+...
$$

$\sigma^2$ یک پارامتر کرنل گاوسی است و می توان آن را تغییر داد تا drop-off ویژگی $f_i$ ما را کم یا زیاد کند. همراه با نگاه کردن
مقادیر داخل $\Theta$ ، ما می توانیم این نقاط عطف را انتخاب کنیم تا شکل کلی مرز تصمیم گیری را بدست آوریم.