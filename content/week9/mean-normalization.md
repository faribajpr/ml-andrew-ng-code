---
title: "جزئیات پیاده‌سازی: نرمال‌سازی میانگین"
date: 2020-11-06T12:46:39+03:30
draft: false
weight: 140
---

اگر سیستم امتیازدهی فیلم برگرفته از قسمت قبل باشد، به کاربران جدید (که هنوز هیچ فیلمی تماشا نکرده‌اند) فیلم‌های نادرستی اختصاص پیدا می‌کند. به طور خاص، تمام اجزا در $\theta$ اختصاص داده شده به آن‌ها به علت کمینه کردن عبارت منظم‌سازی صفر خواهد بود. در نتیجه فرض می‌کنیم که کاربر جدید به تمامی فیلم‌ها امتیاز صفر داده است، که از نظر شهودی صحیح به نظر نمی‌رسد.

این مشکل را با نرمال‌سازی داده‌ها نسبت به میانگین برطرف می‌کنیم. ابتدا از یک ماتریس Y برای نگه‌داری داده‌ها از امتیازدهی قبلی استفاده می‌کنیم، که سطر iام از Y امتیازهای فیلم iام بوده و ستون jام مربوط به امتیازدهی‌های کاربر jام است.

اکنون می‌توانیم یک بردار تعریف کنیم:

$$\mu =\left [ \mu_{1}, \mu_{2}, ..., \mu_{n_{m}} \right ]$$

به طوری که

$$\mu_{i} = \frac{\sum_{j:r(i,j)=1}^{}Y_{i,j}}{\sum_{j}^{}r(i,j)}$$

که در واقع میانگین امتیازات قبلی برای فیلم iام است (تنها فیلم‌هایی که توسط کاربران تماشا شده‌اند شمارش می‌شوند). اکنون می‌توانیم با کم کردن $\mu$ (امتیاز میانگین) از امتیاز واقعی برای هر کاربر داده‌ها را نرمال‌سازی کنیم (ستون‌های ماتریس Y):

به عنوان مثال، ماتریس Y و میانگین امتیازهای $\mu$ را در نظر بگیرید:

$$\mu = \begin{bmatrix} 2.5 \newline 2 \newline 2.25 \newline 1.25 \end{bmatrix}, Y =\begin{bmatrix} 5 & 5 & 0 & 0 \newline 4 & ? & ? & 0 \newline 0 & 0 & 5 & 4 \newline 0 & 0 & 5 & 0 \end{bmatrix}$$

بردار نتیجه ${Y}'$ به صورت زیر خواهد بود:

$$Y =\begin{bmatrix} 2.5 & 2.5 & -2.5 & -2.5 \newline 2 & ? & ? & -2 \newline -2.25 & -2.25 & 3.75 & 1.25 \newline -1.25 & -1.25 & 3.75 & -1.25 \end{bmatrix}$$

اکنون باید کمی پیش‌بینی رگرسیون خطی را اصلاح کنیم تا شامل عبارت نرمال‌سازی میانگین شود:

$$(\theta^{(j)})^{T}x^{(i)} + \mu_{i}$$

اکنون برای یک کاربر جدید، مقایر پیش‌بینی شده اولیه به جای اینکه با صفر مقداردهی شوند برابر با عبارت $\mu$ خواهند بود که این مقدار دقیق‌تر است.