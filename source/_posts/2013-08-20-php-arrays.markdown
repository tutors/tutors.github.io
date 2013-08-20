---
layout: post
title: "آرایه ها در PHP "
date: 2013-08-20 16:20
comments: true
categories: php-fundamental
author: فاطمه کربلایی
---
## آرایه ها در PHP  ##

**آرایه چیست؟** آرایه یک متغیر ویژه است که در یک لحظه می تواند چندین مقدار را در خود نگهداری کند. 

در صورتیکه شما چندین مقدار یا لیستی از عناصر  (لیستی از نام ماشین ها برای مثال) داشته باشید، ذخیره کردن cars در یک متغیر مشابه زیر است:

{% highlight php linenos %}

<?php
$cars1="Volvo";
$cars2="BMW";
$cars3="Toyota";

?>

{% endhighlight %}

اما اگر شما بخواهید در لیست این عناصر دنبال عنصر خاصی بگردید چه اتفاقی می افتد؟ و اگر به جای سه ماشین 300 ماشین داشته باشید چه اتفاقی می افتد؟ راه حل این است که یک آرایه ایجاد کنید. 

یک آرایه می تواند چندین مقدار را تحت یک نام در خود نگه دارد و شما می توانید توسط اندیس عناصر به آنها دسترسی پیدا کنید.

##  ایجاد آرایه در PHP   ##

در PHP از تابع ()array برای ایجاد آرایه استفاده می شود. در این زبان سه نوع آرایه وجود دارد:

**آرایه های اندیس دار[^1]** : آرایه ای با اندیس های عددی

**آرایه های انجمنی [^2]**: آرایه هایی با کلیدهای نامدار


**آرایه های چند بعدی[^3]** : آرایه های شامل یک یا چند آرایه

## آرایه های اندیس در PHP ##

دو راه برای ایجاد آرایه اندیس وجود دارد:

* 	اندیس به طور اتوماتیک مقداردهی می شود (دقت شود که اندیس همواره از صفر شروع می شود):


{% highlight php linenos %}

<?php
$cars=array("Volvo","BMW","Toyota");
?>

{% endhighlight %}

*	اندیس به صورت دستی مقداردهی می شود:

{% highlight php linenos %}

<?php
$cars[0]="Volvo";
$cars[1]="BMW";
$cars[2]="Toyota";

?>

{% endhighlight %}
**مثال** زیر یک آرایه اندیس دار به نام cars$، ایجاد کرده، عناصر آن را مقداردهی کرده و مقادیر آرایه را چاپ می کند.


{% highlight php linenos %}

<?php
$cars=array("Volvo","BMW","Toyota");
echo "I like " . $cars[0] . ", " . $cars[1] . " and " . $cars[2] . ".";
?>

{% endhighlight %}

**نتیجه اجرا**

{% highlight php linenos %}

I like Volvo, BMW and Toyota.

{% endhighlight %}


## بدست آوردن طول آرایه- تابع ()count ##

تابع ()count برای به دست آوردن طول آرایه (تعداد عناصر آرایه) به کار می رود:



{% highlight php linenos %}

<?php
$cars=array("Volvo","BMW","Toyota");
echo count($cars);
?>

{% endhighlight %}

**نتیجه اجرا**

{% highlight php linenos %}

3

{% endhighlight %}


## آرایه های انجمنی در PHP ##

آرایه انجمنی آرایه ای است از کلیدهای نامدار که می توان به آنها مقدار نسبت داد، استفاده می کند. برای ایجاد این نوع آرایه دو روش وجود دارد:



{% highlight php linenos %}

<?php
$age=array("Peter"=>"35","Ben"=>"37","Joe"=>"43");
?>

{% endhighlight %}

یا


{% highlight php linenos %}

<?php
$age['Peter']="35";
$age['Ben']="37";
$age['Joe']="43";

?>

{% endhighlight %}

**مثال**: می توان از کلیدهای نامدار در یک اسکریپت استفاده نمود:

{% highlight php linenos %}
<?php
$age=array("Peter"=>"35","Ben"=>"37","Joe"=>"43");
echo "Peter is " . $age['Peter'] . " years old.";
?>

{% endhighlight %}


**نتیجه اجرا**

{% highlight php linenos %}

Peter is 35 years old.

{% endhighlight %}















































[^1]: Indexed arrays
[^2]: Associative arrays
[^3]: Multidimensional arrays