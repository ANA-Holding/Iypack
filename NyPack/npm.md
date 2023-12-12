1
8
## نحوه تنظیم ریپازیتوری npm در IyPack


</div>

<div dir="rtl">
   
### 1. شما Node.js را می‌توانید از وب‌سایت رسمی آن در آدرس https://nodejs.org/en/ دانلود و نصب کنید.

### 2. در خط فرمان، دستور
</div>

```shell
npm config set registry http://download.iypack.ir/repository/NyPack/
```

<div dir="rtl">

 را اجرا کنید.
 
### 3. یک فایل package.json را در پوشه ~/ با مقادیر زیر ایجاد کنید: (اگر این فایل وجود داشت این مرحله و مرحله 4 رو رد کن)
</div>


```json
{
"name": "sample_project1",
"version": "0.0.1",
"description": "Test Project 1",
"dependencies" : {
  "commonjs" : "0.0.1"
}
}
```

<div dir="rtl">


### 4. از طریق دستور 
</div>


```shell
npm install
```

<div dir="rtl">

  فرآیند npm build را اجرا کنید.
</div>

---
