19
10
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
               url 'http://download.iypack.ir/repository/MyPack/'
               allowInsecureProtocol = true
           }
           // سایر ریپازیتوری‌ها
       }
   }

   allprojects {
       repositories {
           maven {
               url 'http://download.iypack.ir/repository/MyPack/'
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
            url = java.net.URI("http://download.iypack.ir/repository/MyPack/")
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
