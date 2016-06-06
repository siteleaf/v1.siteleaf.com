---
title: Date Formatting
date: 2015-04-09 20:48:00 Z
---

The `date` filter formats a date into another representation.

### Basic Usage

~~~liquid
This was posted on: {{ post.date | date: "%A, %B %-d" }}
~~~

Becomes…

~~~
This was posted on: Thursday, April 9
~~~

We also supply convenience methods for the year, month, and date. These can be especially useful when combined with the [`group_by`](/blog/advanced-liquid-group-by) and [`where`](/blog/advanced-liquid-where) filters.

~~~liquid
This is the same: {{ post.year }} {{ post.month}} {{ post.day }}
As this: {{ post.date | date: "%Y %-m %-d" }}
~~~

~~~
This is the same: 2015 4 9
As this: 2015 4 9
~~~


### Formatting Rules

<small>All results based on the reference date `Thu Apr 9 17:03:07 -0400 EDT 2015`.</small>

| Directive | Description | Result  |
|-----------|-------------|---------|
| `%Y` | Year | `2015` |
| `%y` | Year without century | `15` |
| `%C` | Century | `20` |
| `%m` | Month of year (01–12) | `04` |
| `%B` | Full month name | `April` |
| `%b` | Abbreviated month name | `Apr` |
| `%d` | Day of month (01–31) | `09` |
| `%j` | Day of year (001–366) | `099` |
| `%H` | Hour, 24-hour time (00–23) | `17` |
| `%I` | Hour, 12-hour time (01–12) | `05` |
| `%P` | Meridian indicator, lowercase | `pm` |
| `%p` | Meridian indicator, uppercase | `PM` |
| `%M` | Minute (00–59) | `03` |
| `%S` | Second (00–59) | `07` |
| `%z` | Numeric time zone (±hhmm) | `-0400` |
| `%Z` | Time zone abbreviation | `EDT` |
| `%A` | Weekday | `Thursday` |
| `%a` | Abbreviated weekday | `Thu` |
| `%u` | Day of week starting on Monday (1–7) | `4` |
| `%w` | Day of week starting on Sunday (0–6) | `4` |
| `%W` | Week of year starting on Monday (00–53) | `14` |
| `%U` | Week of year starting on Sunday (00–53) | `14` |
| `%s` | Seconds since Unix Epoch | `1428613387` |
| `%c` | Date and time (`%a %b %e %T %Y`) | `Thu Apr  9 17:03:07 2015` |
| `%D` | Date (`%m/%d/%y`) | `04/09/15` |
| `%F` | ISO 8061 date | `2015-04-09` |
| `%v` | VMS date (`%e-%b-%Y`) | `9-Apr-2015` |
| `%r` | 12-hour time (`%I:%M:%S %p`) | `05:03:07 PM` |
| `%R` | 24-hour time (`%H:%M`) | `17:03` |
| `%T` | 24-hour time with seconds (`%H:%M:%S`) | `17:03:07` |

**Note:** By default, numeric fields are padded with a zero. This can be overridden by some of the following optional flags. Flags are placed immediately after the `%` and before the letter.

| Flag | Description | Result |
|------|-------------|--------|
| `-` (hyphen) | remove padding (`%-d`) | `9` |
| `_` (underscore) | pad with a space (`%_m`) | <pre class="is-code"><code> 4</code></pre> |
| `^` (caret) | up-case if possible (`%^A`) | `THURSDAY` |


<!-- Yuck -->
<style>
.is-code {
  display: inline;
  padding: 0 !important;
}
.is-code code {
  display: inline;
  padding: 4px !important;
  color: #27415a !important;
}
</style>
