# Persian Date(Jalali)
[![forthebadge](https://forthebadge.com/images/badges/built-for-android.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)
<br/>
[![platform](https://img.shields.io/badge/platform-Android-yellow.svg)](https://www.android.com)
[ ![Download](https://api.bintray.com/packages/mrnuke/maven/PersianDate/images/download.svg) ](https://bintray.com/mrnuke/maven/PersianDate/_latestVersion)
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-PersianDate-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/6141)
[![Method and size](https://img.shields.io/badge/Methods%20and%20size-100%20|%2011%20KB-e91e63.svg)](http://www.methodscount.com/?lib=com.github.samanzamani.persiandate%3APersianDate%3A0.1)
# ![attention](https://samanzamani.ir/wp-content/uploads/2019/04/warning.png)  Important update  ![attention](https://samanzamani.ir/wp-content/uploads/2019/04/warning.png)
If you use a version below 0.5 you should upgrade your library to version 0.5 or higher.
There will be an error in the version before 0.5 in the calculation of the date after 2029.
# About
This is a simple android calendar converter for Convert Jalali date to Gregorian date.
# Gradle
```groovy
dependencies {
    implementation 'com.github.samanzamani.persiandate:PersianDate:0.8'
}
```
# what's new
### version 0.8
* Fix date formatting in year 1989 [#29](https://github.com/samanzamani/PersianDate/issues/29)
* add three new methods to get month name in `Afghan`, `Kurdish`, and `Pashto` name and from version 0.8 you can use `X`, `C`, and `E` to display month name in `Afghan`, `Kurdish` and `Pashto` in `PersianDateFormat` [#28](https://github.com/samanzamani/PersianDate/issues/28)

### version 0.7
* Fix addDate - addYear - addMonth methods [#20](https://github.com/samanzamani/PersianDate/issues/20)
* add new method for calculate month length => `getMonthLength`


## Let's convert some date :)

### Step 1

```java
PersianDate pdate = new PersianDate();
```

### step2

```java
PersianDateFormat pdformater = new PersianDateFormat();
pdformater.format(pdate);
```
[More example](#example)

***PersianDate***
---
+ **PersianDate class methods**

| method        | description  |
| ------------- | -----|
| PersianDate(Long timestamp)      | make time with timestamp |
| PersianDate(DATE date)      |   Constractor for make PersianDate object from Date object  |
| setShYear(int year) |    Set Jalali year |
| setShMonth(int month) |    Set Jalali month |
| setShDay(int day) |    Set Jalali day |
| setGrgYear(int year) |    Set Gregorian year |
| setGrgMonth(int month) |    Set Gregorian month |
| setGrgDay(int day) |    Set Gregorian day |
| setHour(int hour) |    Set hour of day |
| setMinute(int minute) |    Set minute of day |
| setSecond(int second) |    Set second of day |
| getShYear() |    (int) return Jalali year |
| getShMonth() |    (int) return Jalali month |
| getShDay() |    (int) return Jalali day |
| getGrgYear() |    (int) return Gregorian year |
| getGrgMonth() |    (int) return Gregorian month |
| getGrgDay() |    (int) return Gregorian day |
| getHour() |    (int) return hour of day |
| getMinute() |    (int) return minute of day |
| getSecond() |    (int) return second of day |
| getTime() |    (Long) return timestamp |
| initGrgDate() |   init date from Gregorian |
| initJalaliDate() |   init date from Jalali |
| isLeap() |   Check Jalali year is leap (TRUE-FALSE) |
| grgIsLeap() |   Check Gregorian year is leap (TRUE-FALSE) |
| toJalali(int year, int month, int day) |  Convert  Gregorian to Jalali (return int[3]) |
| toGregorian(int year, int month, int day) |  Convert  Jalali to Gregorian (return int[3]) |
| dayOfWeek() |   0-6 (0=sat) |
| getDayInYear() |   1-366 |
| dayName() |   شنبه-جمعه |
| monthName() |   فروردین-اسفند |
| getMonthDays() |   return month lenght |
| addDate() |   add some date to object |
| after(PersianDate dateInput) |   Compare 2 date (true=if input date after this) |
| before(PersianDate dateInput) |   Compare 2 date (true=if input date before this) |
| equals(PersianDate dateInput) |   Compare 2 date (true=if input date equals this) |
| untilToday() |   Cal year,month,day until now |
| getDayuntilToday() |   Cal day until now |
| toDate |   convert to Date object |


***PersianDateFormat***
---
+ **PersianDate class methods for display and parse date**

| method        | description  |
| ------------- | -----|
| format()      | (String) Display date |
| parse(String date,String pattern)      | (PersianDate) Convert string Jalali date (1396-05-05 & 'YYYY-MM-dd') to Persiandate |
| parseGrg(String date,String pattern)      | (PersianDate) Convert string Gregorian date (1396-05-05 & 'YYYY-MM-dd') to Persiandate |
| format()      | (String) Display date |

+ **Item for parse date**

| String key        | Role  |
| ------------- | -----|
| yyyy      | Year (1396-2012-...) |
| MM      | Month number (12-01-02-...) |
| dd      | Day number (21-01-02-...) |
| HH      | Hour  (21-01-02-...) |
| mm      | Minute  (21-01-02-...) |
| ss      | Second  (21-01-02-...) |

+ **Pattern item for format date**

| Pattern key   | Role  |
| ------------- | -----|
| l      | Day name in week (شنبه و ....) |
| j      | Day number in month(1-10-20...) |
| F      | Month name (فروردین) |
| Y      | Year  (1396...) |
| H      | Hour in day |
| i      | Minutes in hour |
| s      | Second in minute |
| d      | day in month (01-02-21...) |
| g      | Hour in day 1-12 |
| n      | Month of year 1-12 |
| m      | Month of year 01-12 |
| t      | number day of month |
| w      | day in week 0-6 |
| y      | year with 2 digits |
| z      | Number of days (full) past the year |
| L      | Is leap year (0-1) |

# Example
```java
PersianDate pdate = new PersianDate();
PersianDateFormat pdformater1 = new PersianDateFormat('Y/m/d');
pdformater1.format(pdate);//1396/05/20

PersianDateFormat pdformater2 = new PersianDateFormat('y F j');
pdformater2.format(pdate);//۱۹ تیر ۹۶
```
