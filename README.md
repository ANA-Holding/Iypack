<div dir="rtl">

## فهرست مطالب

1. [نحوه تنظیم ریپازیتوری PyPack برای استفاده دائمی](#windows)
   - [برای Windows](#windows)
   - [برای Linux (Ubuntu)](#linux)
   - [برای macOS](#macos)
2. [استفاده یکباره از ریپازیتوری PyPack](#python)
3. [نحوه تنظیم ریپازیتوری اوبونتو در Lypack](#Lypack)
4. [نحوه تنظیم ریپازیتوری Maven در Mypack](#Mypack)
   - [برای Android Studio](#AS)
6. [نحوه تنظیم ریپازیتوری npm در Nypack](#Nypack)
</div>

---

<div dir="rtl" id="windows">

## نحوه تنظیم ریپازیتوری PyPack برای استفاده دائمی

### برای Windows:

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
<div dir="rtl" id="linux">

### برای Linux (Ubuntu):

1. پوشه pip را در دایرکتوری خانه خود ایجاد کنید:
</div>

```shell
   mkdir -p ~/.pip && touch ~/.pip/pip.conf
   ```
<div dir="rtl">

2. فایل `pip.conf` را باز کرده و محتوای زیر را وارد کنید:
</div>

```plaintext
   [global]
   index-url = http://download.iypack.ir/repository/pypack/simple
   ```
<div dir="rtl" id="macos">

### برای macOS:

1. پوشه pip را در دایرکتوری خانه خود ایجاد کنید:
</div>

```shell
   mkdir -p ~/.pip && touch ~/.pip/pip.conf
   ```
<div dir="rtl">

2. فایل `pip.conf` را باز کرده و محتوای زیر را وارد کنید:
</div>

```plaintext
   [global]
   index-url = http://download.iypack.ir/repository/pypack/simple
   ```
<div dir="rtl" id="python">

## استفاده یکباره از ریپازیتوری PyPack

برای استفاده یکباره از ریپازیتوری ما، دستور زیر را در ترمینال خود اجرا کنید:
</div>

```shell
pip install [package-name] --index-url http://download.iypack.ir/repository/pypack/simple
```
<div dir="rtl">

🌐 با انتخاب PyPack، به جامعه بزرگ و در حال رشد توسعه‌دهندگان Python بپیوندید!

</div>

---

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

</div>


---

<div dir="rtl" id="Mypack">

## نحوه تنظیم ریپازیتوری Maven در IyPack

برای استفاده از ریپازیتوری Maven در پروژه‌های جاوا خود، دستورالعمل‌های زیر را دنبال کنید:

### 1. ویرایش فایل settings.xml

فایل `settings.xml` موجود در دایرکتوری `~/.m2` را ویرایش کنید. اگر این فایل وجود ندارد، آن را ایجاد کنید:
</div>

```shell
nano ~/.m2/settings.xml
```
<div dir="rtl">

### 2. اضافه کردن ریپازیتوری

داخل فایل را با اطلاعات ریپازیتوری iypack به شکل زیر پر کنید:
</div>

```xml
<?xml version="1.0" encoding="UTF-8"?>

<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 https://maven.apache.org/xsd/settings-1.0.0.xsd">

<pluginGroups></pluginGroups>
<proxies></proxies>


<mirrors>
  <mirror>
    <id>nexus</id>
    <mirrorOf>*</mirrorOf>
    <url>http://download.iypack.ir/repository/maven/</url>
  </mirror>
</mirrors>

<profiles>
  <profile>
    <id>nexus</id>
    <repositories>
      <repository>
        <id>central</id>
        <url>http://central</url>
        <releases><enabled>true</enabled></releases>
        <snapshots><enabled>true</enabled></snapshots>
      </repository>
    </repositories>
    <pluginRepositories>
      <pluginRepository>
        <id>central</id>
        <url>http://central</url>
        <releases><enabled>true</enabled></releases>
        <snapshots><enabled>true</enabled></snapshots>
      </pluginRepository>
    </pluginRepositories>
  </profile>
</profiles>
</settings>

```
<div dir="rtl">

### 3.فایل POM (pom.xml) را با مقادیر زیر در ~/ ایجاد کنید:
</div>

```xml
<project>
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.example</groupId>
  <artifactId>nexus-proxy</artifactId>
  <version>1.0-SNAPSHOT</version>
  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.10</version>
    </dependency>
  </dependencies>
</project>
```
<div dir="rtl">

### 4.دستور زیر را برای تست در ترمینال خود اجرا کنید:
</div>

```shell
mvn package
```

<div dir="rtl">
🌟 با انتخاب ریپازیتوری Maven در PyPack، به جامعه بزرگ توسعه‌دهندگان جاوا بپیوندید و از مزایای دسترسی سریع و امن به کتابخانه‌ها بهره‌مند شوید!
<div dir="rtl" id="AS" >

### راه‌اندازی ریپازیتوری Maven در Android Studio:

1. **باز کردن فایل Gradle پروژه (Project-Level Gradle File):**

   فایل `build.gradle` در سطح پروژه را باز کنید. این فایل معمولا در مسیر `ProjectName/build.gradle` قرار دارد.

2. **افزودن ریپازیتوری به بخش repositories:**

   در بخش `repositories` از `buildscript` و `allprojects`, ریپازیتوری سفارشی Maven را به شکل زیر اضافه کنید:
</div>

   ```groovy
   buildscript {
       repositories {
           maven {
               url 'http://download.iypack.ir/repository/maven-public'
           }
           // سایر ریپازیتوری‌ها
       }
   }

   allprojects {
       repositories {
           maven {
               url 'http://download.iypack.ir/repository/maven-public'
           }
           // سایر ریپازیتوری‌ها
       }
   }
   ```
<div dir="rtl">

3. **همگام‌سازی پروژه:**

   پس از اعمال تغییرات، پروژه را همگام‌سازی کنید تا تغییرات اعمال شوند.


🌟 با استفاده از ریپازیتوری Maven در پروژه‌های اندروید، بهره‌وری و کارایی پروژه‌های خود را افزایش دهید!
</div>

<div dir="rtl" id="NyPack">
   
## نحوه تنظیم ریپازیتوری npm در IyPack


</div>

<div dir="rtl">
   
### 1. شما Node.js را می‌توانید از وب‌سایت رسمی آن در آدرس https://nodejs.org/en/ دانلود و نصب کنید.

### 2. در خط فرمان، دستور
</div>

```shell
npm config set registry http://download.iypack.ir/repository/npmjs
```

<div dir="rtl">

 را اجرا کنید.
 
### 3. یک فایل package.json را در پوشه ~/ با مقادیر زیر ایجاد کنید:
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
