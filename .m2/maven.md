
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

### 3.فایل POM (pom.xml) را با مقادیر زیر در ~/ ایجاد کنید: (اگر فایل POM وجود داشت این مرحله رو انجام نده)
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


## نحوه تنظیم ریپازیتوری Maven در IyPack

برای استفاده از ریپازیتوری Maven در پروژه‌های جاوا خود، دستورالعمل‌های زیر را دنبال کنید:

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
               allowInsecureProtocol = true
           }
           // سایر ریپازیتوری‌ها
       }
   }

   allprojects {
       repositories {
           maven {
               url 'http://download.iypack.ir/repository/maven-public'
               allowInsecureProtocol = true
           }
           // سایر ریپازیتوری‌ها
       }
   }
   ```

for kotlin settings.gradle.kts:

```kotlin
pluginManagement {
    repositories {
        google()
        mavenCentral{
            url = java.net.URI("http://download.iypack.ir/repository/maven/")
            isAllowInsecureProtocol = true // add this line
        }
        gradlePluginPortal()
    }
}
```
<div dir="rtl">

3. **همگام‌سازی پروژه:**

   پس از اعمال تغییرات، پروژه را همگام‌سازی کنید تا تغییرات اعمال شوند.


🌟 با استفاده از ریپازیتوری Maven در پروژه‌های اندروید، بهره‌وری و کارایی پروژه‌های خود را افزایش دهید!
