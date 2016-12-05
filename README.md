# NUSModerator

A lightweight library with helpful functions for NUS-related matters.

## Installation

```sh
npm i nusmoderator --S
# or if you use yarn:
yarn add nusmoderator
```

## API

### getAcadYear

Computes the current acad year and return an object of acad year and start date for that year.
If the date is too far into the future (not within supported range),
the last-supported academic year is returned.
If the date is too early (not within supported range), null is returned.

**Parameters**

-   `date` **[Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)** 

Returns **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** acadYearObject - { year: "15/16", startDate: Date }

### getAcadSem

Computes the current academic semester.
Expects a week number of a year.

**Parameters**

-   `acadWeekNumber` **[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

**Examples**

```javascript
acadWeekNumber(3)
```

Returns **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** semester - "Semester 1"

### getAcadWeekName

Computes the current academic week of the semester
Expects a week number of a semester.

**Parameters**

-   `acadWeekNumber` **[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

**Examples**

```javascript
acadWeekNumber(3)
```

Returns **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** semester - "Recess" | "Reading" | "Examination"

### getAcadWeekInfo

Computes the current academic week and return in an object of acad date components

**Parameters**

-   `date` **[Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)** 

Returns **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** {
year: "15/16",
sem: 'Semester 1'|'Semester 2'|'Special Sem 1'|'Special Sem 2',
type: 'Instructional'|'Reading'|'Examination'|'Recess'|'Vacation'|'Orientation',
num: weekNum
}
