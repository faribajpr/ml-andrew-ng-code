---
title: "درک حاشیه اطمینان زیاد"
date: 2020-10-22T16:30:25+03:30
draft: false
weight: 20
---

یک راه مفید برای فکر کردن راجع به ماشین های بردار پشتیبان این است که آن ها را به عنوان طبقه بندی کننده هایی که حاشیه اطمینان زیادی دارند در نظر بگیرید.

$$
if \hspace{0.3cm} y=1,\hspace{0.1cm} we\hspace{0.2cm} want \hspace{0.3cm} \theta\ ^ T x \ge 1 \hspace{0.3cm}(not\hspace{0.1cm} just\hspace{0.1cm} \ge 0 )
$$

$$
if \hspace{0.3cm} y=0,\hspace{0.1cm} we\hspace{0.2cm} want \hspace{0.3cm} \theta\ ^ T x \le -1 \hspace{0.3cm}(not\hspace{0.1cm} just\hspace{0.1cm} < 0 )
$$

حالا زمانی که ثابت C را یک مقدار خیلی بزرگ در نظر بگیریم (برای مثال 100,000)، تابع بهینه سازی ما $\theta$ را محدود می کند به طوری که معادله A (مجموع هزینه های هر نمونه) برابر 0 می شود. ما محدودیت زیر را برای $\theta$ در نظر می گیریم:

$$
\theta\ ^ T x \ge 1 \hspace{0.3cm} if \hspace{0.3cm} y=1 \hspace{0.3cm} and \hspace{0.3cm} \theta\ ^ T x \le -1 \hspace{0.3cm} if \hspace{0.3cm} y=0.
$$

اگر C خیلی بزرگ باشد، پارامترهای $\theta$ را باید مطابق فرمول زیر انتخاب کنیم:

$$
\sum_{i=1}^m y^{(i)} \hspace{0.1cm}  cost\_1(\theta^T x)+(1- y^{(i)} ) \hspace{0.1cm}cost\_0(\theta^T x)=0
$$

که تابع هزینه را به شکل زیر کاهش می دهد:

$$
J(\theta) = C.0+\frac{1}{2} \sum_{j=1}^n \theta_j ^ 2
$$

$$
=\frac{1}{2} \sum_{j=1}^n \theta_j ^ 2
$$

مرز تصمیم گیری را از رگریسیون لجستیک به یاد آوردید (خطی که نمونه های مثبت و منفی را از هم جدا می کرد). خصوصیت ویژه ای که مرز تصمیم گیری در ماشین های بردار پشتیبان دارد این است که تا جای ممکن، از نمونه های مثبت و منفی فاصله دارد.

فاصله مرز تصمیم گیری تا نزدیک ترین نمونه، حاشیه اطمینان نامیده می شود. از آن جایی که ماشین های بردار پشتیبان این حاشیه را حداکثر می کنند، اغلب به آن ها طبقه بندی کننده با حاشیه اطمینان زیاد می گویند.

ماشین بردار پشتیبان نمونه های مثبت و منفی را با حاشیه اطمینان زیاد جدا می کند.

این حاشیه اطمینان زیاد تنها زمانی به دست میاید که C خیلی بزرگ باشد.

داده ها زمانی به صورت خطی قابل جدا شدن هستند که یک خط راست بتواند نمونه های مثبت و منفی را از هم جدا کند.

اگر ما داده های خارج از محدوده داریم که نمی خواهیم روی مرز تصمیم گیری ما اثر بگذارند، می توانیم C را کاهش دهیم.

افزایش و کاهش C، به ترتیب مانند کاهش و افزایش $\lambda$ است و می تواند مرز تصمیم گیری ما را ساده کند.