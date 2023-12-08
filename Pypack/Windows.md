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
   [global]123
   index-url = http://download.iypack.ir/repository/pypack/simple123123
   [global]1234234
   index-url = http://download.iypack.ir/repository/pypack/simple12344353456
   [global]2345
   index-url = http://download.iypack.ir/repository/pypack/simple14353452345
   [global]3456456
   index-url = http://download.iypack.ir/repository/pypack/simple4123412342134
   ```
