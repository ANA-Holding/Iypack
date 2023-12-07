<div dir="rtl">

1. پوشه pip را در پوشه کاربری خود ایجاد کنید:

</div>

```shell
mkdir %USERPROFILE%\pip && type nul > %USERPROFILE%\pip\pip.ini
```
<div dir="rtl">   
2. فایل `pip.ini` را باز کرده و محتوای زیر را وارد کنید:

</div>

   ```plaintext
   [global]
   index-url = http://download.iypack.ir/repository/pypack/simple
   ```
