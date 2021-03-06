---
layout: post
title: "فرم ها و ورودی کاربر"
date: 2013-08-21 15:23
comments: true
categories: php-fundamental
author: فاطمه کربلایی
---
متغیرهای POST _ $  و GET _ $ به منظور بازیابی اطلاعات از فرم [^1] (مانند ورودی کاربر) به کار می روند.



## مدیریت فرم ها در PHP ##

مهمترین نکته ای که هنگام کار با فرم های HTML و PHP با آن برخورد می کنید،
این است که:

 هر عنصر فرم در صفحه HTML به طور اتوماتیک در اسکریپت های PHP شما وجود خواهند داشت.

**مثال:**

 مثال زیر شامل یک فرم HTML با دو فیلد برای ورود اطلاعات و یک دکمه می باشد.

{% highlight html lineones %}
<html>
<body>

<form action="welcome.php" method="post">
Name: <input type="text" name="fname">
Age: <input type="text" name="age">
<input type="submit">
</form>

</body>
</html>

{% endhighlight %}

هنگامی که کاربر فرم بالا را پر کرده و روی دکمه submit کلیک می کند،

 داده فرم به یک فایل PHP  به نام welcome.php فرستاده می شود.

 کد فایل welcome.php مشابه زیر است:

{% highlight php lineones %}
<html>
<body>

Welcome <?php echo $_POST["fname"]; ?>!<br>
You are <?php echo $_POST["age"]; ?> years old.

</body>
</html>

{% endhighlight %}


** نتیجه اجرا: **
{% highlight sh linenos %}

Welcome John!
You are 28 years old.


{% endhighlight %}

متغیرهای POST _ $  و GET _ $  در قسمت بعدی توضیح داده خواهند شد.

## اعتبار سنجی فرم ##

لازم به ذکر است که کاربر باید داده های معتبر در فرم وارد کند. 

اعتبارسنجی ورودی کاربر باید در مرورگر و در جای مناسب انجام گیرد (بوسیله اسکریپت های مشتری ). 

اعتبارسنجی مرورگر سریع تر است و میزان لود سرور را کاهش می دهد.

هنگامی که کاربر داده وارد می کند شما باید اعتبارسنجی سرور  انجام داده و 
مطمئن شوید که اطلاعات به پایگاه داده وارد شده اند.

 یک روش مناسب برای اعتبارسنجی یک فرم بر روی سرور این است که: 

فرم را به خود سرور بفرستید نه به یک صفحه دیگر.

سپس کاربر پیغام های خطا را در همان صفحه دریافت می کند و بنابراین یافتن خطا بسیار سریعتر انجام می گیرد.



[^1]:Form 