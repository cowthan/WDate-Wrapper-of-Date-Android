# WDate - Wrapper of Date

This is an utility class that wraps the standard `Date` class
providing some useful methods without using the `Calendar` object.

![Alt text](https://img.shields.io/badge/license-MIT-green.svg?style=flat)
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-WDate%20--%20Wrapper%20of%20Date-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/5136)


## Getting Started

#### Gradle

```groovy
dependencies {
  compile 'com.llollox.androidprojects:wdate:1.0.3'
}
```

#### Maven
```xml
<dependency>
  <groupId>com.llollox.androidprojects</groupId>
  <artifactId>wdate</artifactId>
  <version>1.0.3</version>
  <type>pom</type>
</dependency>
```

## Usage

The first thing to do is set the date for our
`WDate` object. This can be done in the following manner:

```java
// Set its date as now
WDate wdate = new WDate();

// Set as its date the one passed as argument
WDate wdate = new WDate(yourDate);

// Set as its date the one passed as argument
wDate.setDate(yourDate);
```


##### Checkers

```java
boolean isToday()

boolean isTomorrow()

boolean isYesterday()
```




##### Comparators

```java
// Returns the number of days (absolute value) between the dates.
// The wdate's date is included, the other one not.
int getNumDaysBetween(Date date)

// Returns the number of months (absolute value) between the dates.
// The wdate's date is included, the other one not.
int getNumMonthsBetween(Date date)

// Returns the number of years (absolute value) between the dates.
// The wdate's date is included, the other one not.
int getNumYearsBetween(Date date)

// Returns the number of milliseconds (absolute value) between the dates.
long getMilliSecondsDifference(Date date)

// Checks if the wdate's date is contained in the period.
// Both start and end date limits are excluded.
boolean isInRange (Date start, Date end)

// Checks if both dates have same day, month and year.
boolean isSameDay(Date date)
```

##### Converters

```java
// Returns the date setting its time to 00:00:00.000
Date getWithoutTime()
```


##### Formatter

```java
// Format string following the Simple Date Format pattern.
String format (String sdfPattern)
```


### Getters

##### Date

```java
int getDay () // Day number in the month

int getMonth () // Months start from 0

int getYear ()
```

### Time

```java
int getHours () // 24h format

int getMinutes ()

int getSeconds ()

int getMilliSeconds ()
```



### Modifiers
All modifiers supports method chaining.

##### Date

```java
WDate addDays (int numDays)

WDate addMonths (int numMonths)

WDate addYears (int numYears)
```

### Time

```java
WDate addHours (int numHours)

WDate addMinutes (int numMinutes)

WDate addSeconds (int numSeconds)

WDate addMilliSeconds (int numMilliSeconds)
```




### Setters
All setters supports method chaining.

##### Date

```java
WDate setDay (int days)

WDate setMonth (int months)

WDate setYear (int years)
```

### Time

```java
WDate setHours (int hours)

WDate setMinutes (int minutes)

WDate setSeconds (int seconds)

WDate setMilliSeconds (int milliSeconds)
```
