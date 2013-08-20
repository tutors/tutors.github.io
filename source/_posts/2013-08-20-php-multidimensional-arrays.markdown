---
layout: post
title: "آرایه های چند بعدی در PHP"
date: 2013-08-20 17:54
comments: true
categories: php-fundamental
author: فاطمه کربلایی
---
مقدار یک آرایه می تواند علاوه بر مقدار یک آرایه دیگر باشد و بنابراین می تواند آرایه دیگر را در خود نگهدارد. در این حالت می توان آرایه های دو یا سه بعدی ایجاد نمود.

**مثال:**

{% highlight php linenos %}

<?php
// A two-dimensional array
$cars = array
   (
   array("Volvo",100,96),
   array("BMW",60,59),
   array("Toyota",110,100)
   );
   
echo $cars[0][0].": Ordered: ".$cars[0][1].". Sold: ".$cars[0][2]."<br>";
echo $cars[1][0].": Ordered: ".$cars[1][1].". Sold: ".$cars[1][2]."<br>";
echo $cars[2][0].": Ordered: ".$cars[2][1].". Sold: ".$cars[2][2]."<br>";
?>


{% endhighlight %}

**نتیجه اجرا:**
{% highlight php linenos %}

Volvo: Ordered: 100. Sold: 96
BMW: Ordered: 60. Sold: 59
Toyota: Ordered: 110. Sold: 100

{% endhighlight %}

## آرایه های چند بعدی  ##

یک آرایه چندبعدی آرایه ای است که شا مل یک یا چند آرایه دیگر است.

در یک آرایه چندبعدی هر عنصر در آرایه اصلی می تواند یک آرایه باشد و هر عنصر در زیر آرایه نیز می تواند یک آرایه باشد و به همین ترتیب.

**مثال 1:**

در مثال يک آرايه چند بعدي با کليدهاي اختصاص داده شده اتوماتيک ايجاد مي شود. 

{% highlight php linenos %}
<?php
$families = array
  (
  "Griffin"=>array
  (
  "Peter",
  "Lois",
  "Megan"
  ),
  "Quagmire"=>array
  (
  "Glenn"
  ),
  "Brown"=>array
  (
  "Cleveland",
  "Loretta",
  "Junior"
  )
  );
?>

{% endhighlight %}

آرايه بالا در صورتي که در خروجي نوشته شود به صورت زير مي باشد:

{% highlight php linenos %}
<?php
Array
(
[Griffin] => Array
  (
  [0] => Peter
  [1] => Lois
  [2] => Megan
  )
[Quagmire] => Array
  (
  [0] => Glenn
  )
[Brown] => Array
  (
  [0] => Cleveland
  [1] => Loretta
  [2] => Junior
  )
)

?>

{% endhighlight %}


**مثال 2:**

مي خواهيم يک مقدار يکتا از آرايه بالا را نشان دهيم:

{% highlight php linenos %}
<?php

echo "Is " . $families['Griffin'][2] . " a part of the Griffin family?";

?>

{% endhighlight %}

**نتيجه اجرا**

{% highlight php linenos %}

Is Megan a part of the Griffin family?

{% endhighlight %}