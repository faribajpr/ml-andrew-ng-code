---
title: "کاهش ابعاد"
date: 2020-10-25T12:57:20+03:30
draft: false
weight: 60
---

### انگیزه ۱: فشرده سازی داده ها
- اگر داده های زائد زیادی داشته باشیم ممکن است بخواهیم ابعاد ویژگی های خود را کاهش دهیم.
- برای انجام این کار، دو ویژگی بسیار مرتبط پیدا می‌کنیم، آنها را رسم می‌کنیم و یک خط جدید ایجاد می‌کنیم که به نظر می‌رسد هر دو ویژگی را به طور دقیق توصیف می‌کند. ما همه ویژگی های جدید را روی این خط واحد قرار می‌دهیم.

انجام کاهش ابعاد باعث کاهش کل داده هایی می‌شود که باید در حافظه کامپیوتر ذخیره کنیم و الگوریتم یادگیری ما را تسریع می‌کند.

{{%notice note%}}
در کاهش ابعاد ، ما در حال کاهش ویژگی های خود هستیم تا تعداد نمونه های خود.
متغیر $m$ ما در همان اندازه قبلی خواهد ماند،
$n$ یعنی تعداد ویژگی های هر نمونه از $x ^{(1)}$ تا $x ^ {(m)}$ کاهش خواهد یافت.
{{% /notice %}}


### انگیزه ۲: مصور سازی

مصور سازی داده هایی که بیش از سه بعد هستند آسان نیست.
ما می‌توانیم ابعاد داده های خود را به ۳ یا کمتر کاهش دهیم تا آنها را ترسیم کنیم.

ما نیاز داریم که ویژگی های جدید پیدا کنیم،
$z_1, z_2$ (و شاید $z_3$)، که می‌توانند به طور موثر همه ویژگی های دیگر را خلاصه کنند.

به طور مثال:
صدها ویژگی مرتبط با سیستم اقتصادی یک کشور ممکن است همه در یک ویژگی که شما آن را "فعالیت اقتصادی" می‌نامید، ترکیب شوند.