---
layout: post
title: "مرتب سازی آرایه ها در PHP"
date: 2013-08-21 13:52
comments: true
categories: php-fundamental
author: فاطمه کربلایی
---
عناصر آرایه ها می توانند به صورت الفبایی یا عددی (صعودی یا نزولی) مرتب شوند.

## توابع مرتب سازی در PHP ##

در این قسمت به معرفی توابع مرتب سازی آرایه در PHP پرداخته می شود:

*	()sort: آرایه را به ترتیب صعودی مرتب می کند.

*	()rsort:آرایه را به ترتیب نزولی مرتب می کند.

*	()asort: آرایه انجمنی را با توجه به مقادیر[^1]  آن به صورت صعودی مرتب می کند.
 
*	()ksort:آرایه انجمنی را با توجه به کلید[^2]های  آن به صورت صعودی مرتب می کند.


*	()arsort:آرایه انجمنی را با توجه به مقادیر  آن به صورت نزولی مرتب می کند.


*	()krsort:آرایه انجمنی را با توجه به کلیدهای  آن به صورت نزولی مرتب می کند.

## مرتب¬سازی آرایه به ترتیب صعودی- ()sort ##

**مثال** زیر عناصر آرایه $cars را به ترتیب صعودی بر اساس حروف الفبا مرتب می کند:

{% highlight php linenos %}

<?php
$cars = array("Volvo","BMW","Toyota");
sort($cars);
?>

{% endhighlight %}

**خروجی:**
{% highlight php linenos %}

BMW
Toyota
Volvo

{% endhighlight %}

**مثال:**

 مرتب سازی آرایه $numbers به ترتیب صعودی - عددی

{% highlight php linenos %}

<?php
$numbers = array(4,6,2,22,11);
sort($numbers);
?>

{% endhighlight %}

**خروجی:**
{% highlight php linenos %}

2
4
6
11
22

{% endhighlight %}

## مرتب سازی آرایه به ترتیب نزولی- ()rsort: ##

**مثال:**

 مرتب سازی عناصر آرایه cars$ به ترتیب نزولی

{% highlight php linenos %}

<?php
$cars = array("Volvo","BMW","Toyota");
rsort($cars);

$clength = count($cars);
for($x = 0;$x < $clength;$x++)
   {
   echo $cars[$x];
   echo "<br>";
   }
?>


{% endhighlight %}

**خروجی:**
{% highlight php linenos %}

Volvo
Toyota
BMW

{% endhighlight %}

**مثال:**

 مرتب سازی آرایه numbers$ به ترتیب نزولی – عددی

{% highlight php linenos %}

<?php
$numbers = array(4,6,2,22,11);
rsort($numbers);

$arrlength = count($numbers);
for($x = 0;$x < $arrlength;$x++)
   {
   echo $numbers[$x];
   echo "<br>";
   }
?>

{% endhighlight %}

**خروجی:**
{% highlight php linenos %}

22
11
6
4
2
{% endhighlight %}

## مرتب سازی آرایه انجمنی به ترتیب صعودی و نزولی: ##

**مثال:**

 مرتب سازی صعودی آرایه انجمنی بر اساس مقادیر  آن-  ()assort:

{% highlight php linenos %}

<?php
$age = array("Peter"=>"35","Ben"=>"37","Joe"=>"43");
asort($age);

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

**مثال:**

 مرتب سازی صعودی آرایه انجمنی بر اساس کلیدهای  آن- ()ksort:

{% highlight php linenos %}

<?php
$age = array("Peter"=>"35","Ben"=>"37","Joe"=>"43");
ksort($age);

foreach($age as $x=>$x_value)
    {
    echo "Key = " . $x . ", Value = " . $x_value;
    echo "<br>";
    }
?>

{% endhighlight %}

**خروجی:**
{% highlight php linenos %}


Key = Ben, Value = 37
Key = Joe, Value = 43
Key = Peter, Value = 35

{% endhighlight %}

**مثال:**

 مرتب سازی نزولی آرایه انجمنی بر اساس مقادیر  آن- ()arsort:


{% highlight php linenos %}

<?php
$age = array("Peter"=>"35","Ben"=>"37","Joe"=>"43");
arsort($age);

foreach($age as $x=>$x_value)
    {
    echo "Key = " . $x . ", Value = " . $x_value;
    echo "<br>";
    }
?>


{% endhighlight %}

**خروجی:**
{% highlight php linenos %}

Key = Joe, Value = 43
Key = Ben, Value = 37
Key = Peter, Value = 35

{% endhighlight %}

**مثال:**

 مرتب سازی نزولی آرایه انجمنی بر اساس کلیدهای  آن – ()krsort:

{% highlight php linenos %}

<?php
$age = array("Peter"=>"35","Ben"=>"37","Joe"=>"43");
krsort($age);

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
Key = Joe, Value = 43
Key = Ben, Value = 37

{% endhighlight %}





[^1]:value
[^2]:key
