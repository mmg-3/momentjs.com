**Note:** `moment.humanizeDuration()` has been deprecated in favor of `moment.duration().humanize()`.

It will be removed shortly in the future. [More documentation on moment.duration().humanize() here.](#/durations/humanize/)

Sometimes, you want all the goodness of `moment.fn.from` but you don't want to have to create two moments, you just want to display a length of time.

Enter `moment.humanizeDuration`. With only a number passed in, it will return the humanized duration of the number as milliseconds.

```javascript
moment.humanizeDuration(1000 * 60); // a minute
```

To use a different time difference, pass it in as a string.

```javascript
moment.humanizeDuration(1, "seconds"); // a few seconds
moment.humanizeDuration(1, "minutes"); // a minute
moment.humanizeDuration(1, "hours");   // an hour
moment.humanizeDuration(1, "days");    // a day
moment.humanizeDuration(1, "weeks");   // 7 days
moment.humanizeDuration(1, "months");  // a month
moment.humanizeDuration(1, "years");   // a year
```

By default, the return string is suffixless. If you want a suffix, pass in true as seen below.

```javascript
moment.humanizeDuration(60000, true);        // in a minute
moment.humanizeDuration(1, "minutes", true); // in a minute
```

For suffixes before now, pass in a negative number.

```javascript
moment.humanizeDuration(-60000, true);        // a minute ago
moment.humanizeDuration(-1, "minutes", true); // a minute ago
```