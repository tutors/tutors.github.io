---
layout: post
title: "حلقه های for در PHP"
date: 2013-08-21 12:59
comments: true
categories: php-fundamental
author: فاطمه کربلایی
---
## حلقه for ##
حلقه for هنگامی استفاده می شود که شما تعداد دفعات اجرای یک اسکریپت را بدانید.

**گرامر:**

{% highlight php linenos %}

<?php
for (init; condition; increment)
  {
     ؛کدی که باید اجرا شود
  }
?>

{% endhighlight %}

**پارامترها:**

**init:** معمولاً برای تنظیم شمارنده به کار می رود(البته می تواند هر قطعه کدی باشد که قرار است در ابتدای یک حلقه اجرا شود).


**Condition:** در هر تکرار مورد بررسی قرار می گیرد، در صورتیکه شرط برقرار باشد حلقه ادامه می یابد، در غیر اینصورت حلقه خاتمه می یابد.


**Increment:** معمولاً برای افزایش شمارنده به کار می رود(البته می تواند هر قطعه کدی باشد که قرار است در انتهای یک حلقه اجرا شود)


**نکته:**

 پارامترهای init و increment در بالا می توانند خالی باشند و یا شامل چند عبارت باشند.

**مثال: **

{% highlight php linenos %}

<?php
for ($i = 1; $i <= 5; $i++)
  {
  echo "The number is " . $i . "<br>";
  }
?>


{% endhighlight %}

**خروجی:**
{% highlight php linenos %}

The number is 1
The number is 2
The number is 3
The number is 4
The number is 5
{% endhighlight %}
## حلقه foreach ##

حلقه foreach  برای حرکت روی عناصر آرایه به کار می رود.

**گرامر:**

{% highlight php linenos %}

<?php
foreach ($array as $value)
  {
     ؛کدی که باید اجرا شود
  }
?>

{% endhighlight %}

در هر بار تکرار حلقه مقدار جاری عنصر آرایه برابر با value$ می شود (و اشاره گر آرایه یکی یکی جلو می رود). 

بنابراین در تکرار بعدی حلقه مقدار بعدی آرایه مورد بررسی قرار می گیرد.

**مثال:**


{% highlight php linenos %}

<?php
$x=array("one","two","three");
foreach ($x as $value)
  {
  echo $value . "<br>";
  }
?>

{% endhighlight %}

**خروجی:**

{% highlight php linenos %}
one
two
three

{% endhighlight %}

## استفاده از حلقه در آرایه ها ##

### استفاده از حلقه در آرایه اندیس دار ###
برای اینکه بتوان تمامی عناصر یک آرایه اندیس دار را چاپ نمود، می توان از حلقه for استفاده نمود، مانند زیر:

{% highlight php linenos %}

<?php
$cars = array("Volvo","BMW","Toyota");
$arrlength = count($cars);

for($x = 0;$x < $arrlength;$x++)
  {
  echo $cars[$x];
  echo "<br>";
  }
?>

{% endhighlight %}

**خروجی:**

{% highlight php linenos %}
Volvo
BMW
Toyota

{% endhighlight %}

### استفاده از حلقه در آرایه انجمنی ###

برای اینکه بتوان تمامی عناصر یک آرایه اندیس دار را چاپ نمود، می توان از حلقه foreach استفاده نمود، مانند زیر:

{% highlight php linenos %}

<?php
$age = array("Peter"=>"35","Ben"=>"37","Joe"=>"43");

foreach($age as $x=>$x_value)
  {
  echo "Key = " . $x . ", Value = " . $x_value;
  echo "<br>";
  }
?>

{% endhighlight %}

**خروجی:**

{% highlight php linenos %}

Key = Peter, Value = 35
Key = Ben, Value = 37
Key = Joe, Value = 43

{% endhighlight %}