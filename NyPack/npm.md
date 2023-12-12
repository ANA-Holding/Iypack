1
8
## نحوه تنظیم ریپازیتوری npm در IyPack


</div>

<div dir="rtl">
   
### 1. در خط فرمان، دستور
</div>

```shell
npm config set registry http://download.iypack.ir/repository/NyPack/
```

<div dir="rtl">

 را اجرا کنید.
 
### 2. یک فایل package.json را در پوشه ~/ با مقادیر زیر ایجاد کنید: (اگر این فایل وجود داشت این مرحله و مرحله 4 رو رد کن)
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


### 3. از طریق دستور 
</div>


```shell
npm install
```

<div dir="rtl">

  فرآیند npm build را اجرا کنید.
</div>

---
