1
2
<div dir="rtl" id="Lypack">

## نحوه تنظیم ریپازیتوری اوبونتو در iypack

برای افزودن ریپازیتوری اوبونتو به لیست منابع بسته‌های خود، دستورالعمل‌های زیر را دنبال کنید:

### 1. باز کردن فایل sources.list

ابتدا، فایل `sources.list` را باز کنید:
</div>

```shell
sudo nano /etc/apt/sources.list
```
<div dir="rtl">

### 2. افزودن ریپازیتوری

در فایل باز شده، خطوط زیر را اضافه کنید:
</div>

```plaintext
deb http://download.iypack.ir/repository/Ubuntu/ubuntu [distribution] main restricted
deb-src http://download.iypack.ir/repository/Ubuntu/ubuntu [distribution] main restricted
```
<div dir="rtl">

در اینجا `[distribution]` را با نام توزیع اوبونتوی خود (مانند `focal`, `bionic` و غیره) جایگزین کنید.

### 3. به‌روزرسانی لیست بسته‌ها

پس از اضافه کردن ریپازیتوری جدید، لیست بسته‌های خود را به‌روز کنید:
</div>

```shell
sudo apt update
```
<div dir="rtl">

## استفاده از ریپازیتوری

پس از به‌روزرسانی، شما می‌توانید بسته‌های مورد نیاز خود را از ریپازیتوری جدید نصب کنید:
</div>

```shell
sudo apt install [package-name]
```
<div dir="rtl">

🌟 با استفاده از ریپازیتوری اوبونتو در PyPack، از تجربه‌ی به‌روز و امن لذت ببرید!
