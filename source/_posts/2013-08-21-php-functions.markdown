---
layout: post
title: "توابع PHP"
date: 2013-08-21 14:36
comments: true
categories: php-fundamental
author: فاطمه کربلایی
---
قدرت واقعی php برگرفته از توابع[^1]  آن است.

 در Php بیش از 7000 تابع از پیش ساخته شده  وجود دارد.

 در این فصل نحوه ایجاد تابع در php توضیح داده خواهد شد.

برای جلوگیری از اینکه هنگامی که یک صفحه لود می شود، اسکریپت اجرا شود، می توانید اسکریپت را در یک تابع قرار دهید.

 یک تابع زمانی اجرا می شود که آنرا فراخوانی کنید و شما می توانید تابع را در هرجایی از کد فراخوانی کنید.

## ایجاد تابع در PHP ##

یک تابع زمانی اجرا می شود که آن را فراخوانی کنید.

**گرامر:**
{% highlight php linenos %}

<?php
function functionName()
{
؛کدی که باید اجرا شود
{

?>

{% endhighlight %}

### اصولی راجع به توابع PHP: ###

*	به تابع نامی بدهید که نشاندهنده عملکرد تابع باشد.

*	نام تابع می تواند با یک حرف یا _ شروع شود (نه عدد).

**مثال:**

 تابع ساده ای که هنگامی که فراخوانی می شود، اسم را می نویسد.

{% highlight php linenos %}

<?php
function writeName()
{
echo "Kai Jim Refsnes";
}

echo "My name is ";
writeName();
?>

{% endhighlight %}

** نتیجه اجرا: **

{% highlight sh linenos %}

My name is Kai Jim Refsnes

{% endhighlight %}

## اضافه کردن پارامتر به تابع ##

برای اینکه یک تابع بتواند کارهای بیشتری انجام دهد، می توان به آن پارامتر اضافه نمود.

 یک پارمتر مانند یک متغیر  است. پارامترها بعد از نام تابع و در داخل پرانتز نوشته می شوند.

**مثال1:**

 مثال زیر نام های متفاوت و با نام خانوادگی یکسان را چاپ می کند.

{% highlight php linenos %}

<?php
function writeName($fname)
{
echo $fname . " Refsnes.<br>";
}

echo "My name is ";
writeName("Kai Jim");
echo "My sister's name is ";
writeName("Hege");
echo "My brother's name is ";
writeName("Stale");
?>

{% endhighlight %}

** نتیجه اجرا: **

{% highlight sh linenos %}

My name is Kai Jim Refsnes.
My sister's name is Hege Refsnes.
My brother's name is Stale Refsnes.

{% endhighlight %}

**مثال2:**

 تابعی با دو پارامتر

{% highlight php linenos %}

<?php
function writeName($fname,$punctuation)
{
echo $fname . " Refsnes" . $punctuation . "<br>";
}

echo "My name is ";
writeName("Kai Jim",".");
echo "My sister's name is ";
writeName("Hege","!");
echo "My brother's name is ";
writeName("Ståle","?");
?>

{% endhighlight %}

** نتیجه اجرا: **

{% highlight sh linenos %}

My name is Kai Jim Refsnes.
My sister's name is Hege Refsnes!
My brother's name is Ståle Refsnes?


{% endhighlight %}

## مقادیر بازگشتی در تابع ##

برای اینکه یک تابع بتواند مقدار بازگشتی داشته باشد، می توان از عبارت return استفاده نمود.

**مثال:**

{% highlight php linenos %}

<?php
function add($x,$y)
{
$total = $x+$y;
return $total;
}

echo "1 + 16 = " . add(1,16);
?>

{% endhighlight %}

** نتیجه اجرا: **

{% highlight sh linenos %}
1 + 16 = 17

{% endhighlight %}
[^1]:functions