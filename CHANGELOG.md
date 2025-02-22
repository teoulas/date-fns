# Change Log

All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning].

This change log follows the format documented in [Keep a CHANGELOG].

[Semantic Versioning]: http://semver.org/
[Keep a CHANGELOG]: http://keepachangelog.com/

## [Unreleased]

## [1.18.0] - 2016-12-12

### Added

- [Turkish locale (tr)](https://github.com/date-fns/date-fns/pull/329)
  (kudos to Alpcan Aydın [@alpcanaydin](https://github.com/alpcanaydin))

- [Korean locale (ko)](https://github.com/date-fns/date-fns/pull/327)
  (thanks to Hong Chulju [@angdev](https://github.com/angdev))

### Fixed

- `SS` and `SSS` formats in `format` are now correctly displayed with leading zeros.
  Thanks to Paul Dijou [@pauldijou](https://github.com/pauldijou).
  See PR: [#330](https://github.com/date-fns/date-fns/pull/330)

## [1.17.0] - 2016-12-10

### Added

- [Polish locale (pl)](https://github.com/date-fns/date-fns/pull/294)
  (thanks to Mateusz Derks [@ertrzyiks](https://github.com/ertrzyiks))

- [Portuguese locale (pt)](https://github.com/date-fns/date-fns/pull/316)
  (thanks to Dário Freire [@dfreire](https://github.com/dfreire))

- [Swedish locale (sv)](https://github.com/date-fns/date-fns/pull/311)
  (thanks to Johannes Ulén [@ejulen](https://github.com/ejulen))

- [French locale (fr)](https://github.com/date-fns/date-fns/pull/281)
  (thanks to Jean Dupouy [@izeau](https://github.com/izeau))

- Performance tests. See PR: [#289](https://github.com/date-fns/date-fns/pull/289)

### Fixed

- Fix TypeScript and flow typings for `isValid`.
  See PR: [#310](https://github.com/date-fns/date-fns/pull/310)

- Fix incorrect locale tests that could potentially lead to `format` bugs.
  Kudos to Mateusz Derks [@ertrzyiks](https://github.com/ertrzyiks).
  See related PRs: [#312](https://github.com/date-fns/date-fns/pull/312),
  [#320](https://github.com/date-fns/date-fns/pull/320)

- Minor language fixes in the documentation.
  Thanks to Vedad Šoše [@vedadsose](https://github.com/vedadsose) ([#314](https://github.com/date-fns/date-fns/pull/314))
  and Asia [@asia-t](https://github.com/asia-t) ([#318](https://github.com/date-fns/date-fns/pull/318))

### Changed

- `format` now returns `String('Invalid Date')` if the passed date is invalid.
  See PR: [#323](https://github.com/date-fns/date-fns/pull/323)

- `distanceInWords`, `distanceInWordsToNow`, `distanceInWordsStrict` and `format` functions now
  check if the passed locale is valid, and fallback to English locale otherwise.
  See PR: [#321](https://github.com/date-fns/date-fns/pull/321)

- *Internal*: use a loop instead of `Object.keys` in `buildFormattingTokensRegExp`
  to improve compatibility with older browsers.
  See PR: [#322](https://github.com/date-fns/date-fns/pull/322)

## [1.16.0] - 2016-12-08

### Added

- [Italian locale (it)](https://github.com/date-fns/date-fns/pull/298)
  (thanks to Alberto Restifo [@albertorestifo](https://github.com/albertorestifo))

- For German `buildDistanceInWordsLocale`, add nominative case translations (for distances without a suffix).
  Kudos to Asia [@asia-t](https://github.com/asia-t).
  See related PR: [#295](https://github.com/date-fns/date-fns/pull/295)

## [1.15.1] - 2016-12-07

### Fixed

- Fixed TypeScript imports from individual modules.
  Thanks to [@mattlewis92](https://github.com/mattlewis92).
  See related PR: [#287](https://github.com/date-fns/date-fns/pull/287)

## [1.15.0] - 2016-12-07

### Added

- [Indonesian locale (id)](https://github.com/date-fns/date-fns/pull/299)
  (thanks to Rahmat Budiharso [@rbudiharso](https://github.com/rbudiharso))

- [Catalan locale (ca)](https://github.com/date-fns/date-fns/pull/300)
  (thanks to Guillermo Grau [@guigrpa](https://github.com/guigrpa))

### Fixed

- Fix some inaccuracies in Spanish locale.
  Kudos to [@guigrpa](https://github.com/guigrpa).
  See related PR: [#302](https://github.com/date-fns/date-fns/pull/302)

## [1.14.1] - 2016-12-06

### Fixed

- Fixed broken test for Norwegian Bokmål locale.

## [1.14.0] - 2016-12-06

### Added

- [Norwegian Bokmål locale (nb)](https://github.com/date-fns/date-fns/pull/291)
  (thanks to Hans-Kristian Koren [@Hanse](https://github.com/Hanse))

## [1.13.0] - 2016-12-06

### Added

- [Chinese Traditional locale (zh_tw)](https://github.com/date-fns/date-fns/pull/283)
  (thanks to tonypai [@tpai](https://github.com/tpai)).

- [Dutch language locale (nl)](https://github.com/date-fns/date-fns/pull/278)
  (kudos to Jorik Tangelder [@jtangelder](https://github.com/jtangelder))

## [1.12.1] - 2016-12-05

### Fixed

- Added `distanceInWordsStrict` to the list of supported functions in I18n doc.

## [1.12.0] - 2016-12-05

### Added

- [Spanish language locale (es)](https://github.com/date-fns/date-fns/pull/269)
  (thanks to Juan Angosto [@juanangosto](https://github.com/juanangosto)).

### Fixed

- Fix flow typings for some of the functions.
  See PR: [#273](https://github.com/date-fns/date-fns/pull/273)

## [1.11.2] - 2016-11-28

### Fixed

- Bug in `parse` when it sometimes parses ISO week-numbering dates incorrectly.
  See PR: [#262](https://github.com/date-fns/date-fns/pull/262)

- Bug in some functions which caused them to handle dates earlier than 100 AD incorrectly.
  See PR: [#263](https://github.com/date-fns/date-fns/pull/263)

## [1.11.1] - 2016-11-24

### Fixed

- Include TypeScript typings with npm package.

## [1.11.0] - 2016-11-23

### Added

- `distanceInWordsStrict`.
  Kudos to [@STRML](https://github.com/STRML).
  See related PR: [#254](https://github.com/date-fns/date-fns/pull/254)

- [TypeScript](https://www.typescriptlang.org/) typings for all functions.
  Kudos to [@mattlewis92](https://github.com/mattlewis92).
  See related PR: [#255](https://github.com/date-fns/date-fns/pull/255)

## [1.10.0] - 2016-11-01

### Added

- `parse` now can parse dates that are ISO 8601 centuries (e.g., `19` and `+0019`).

  ```javascript
  var result = parse('19')
  //=> Mon Jan 01 1900 00:00:00
  ```

- In `parse`, added ability to specify the number of additional digits
  for extended year or century format (possible values are 0, 1 or 2; default is 2).

  ```javascript
  parse('+002016-11-01')
  parse('+02016-11-01', {additionalDigits: 1})
  parse('+2016-11-01', {additionalDigits: 0})
  ```

## [1.9.0] - 2016-10-25

### Added

- Got index.js imports to work with SystemJS.

## [1.8.1] - 2016-10-24

### Fixed

- Added Japanese and German language locales to the list in I18n doc.

## [1.8.0] - 2016-10-23

### Added

- [Japanese language locale (ja)](https://github.com/date-fns/date-fns/pull/241)
  (thanks to Thomas Eilmsteiner [@DeMuu](https://github.com/DeMuu) again!)

- `getISODay`

- `setISODay`

## [1.7.0] - 2016-10-20

### Added

- [German language locale (de)](https://github.com/date-fns/date-fns/pull/237)
  (thanks to Thomas Eilmsteiner [@DeMuu](https://github.com/DeMuu)).

## [1.6.0] - 2016-10-16

### Added

- [Chinese Simplified locale (zh_cn)](https://github.com/date-fns/date-fns/pull/235)
  (kudos to Changyu [@KingMario](https://github.com/KingMario) Geng).

## [1.5.2] - 2016-10-13

### Fixed

- Incorrectly generated docs for `format`.

- Fixed typo in I18n doc.

## [1.5.1] - 2016-10-12

### Fixed

- A change log entry for [1.5.0] is added.

## [1.5.0] - 2016-10-12

### Added

- [The initial I18n support](https://date-fns.org/docs/I18n)

## [1.4.0] - 2016-10-09

### Added

- Basic [SystemJS](https://github.com/systemjs/systemjs) support.

### Fixed

- Fix incorrect behaviour of `YYYY` and `YY` for years prior to 1000:
  now `format(new Date('0001-01-01'), 'YYYY-MM-DD')` returns `0001-01-01`
  instead of `1-01-01`.

## [1.3.0] - 2016-05-26

### Added

- `closestIndexTo`

## [1.2.0] - 2016-05-23

### Added

- Add an ability to pass negative numbers to `setDay`.

## [1.1.1] - 2016-05-19

### Fixed

- Fix [Flow](http://flowtype.org/) declarations for some of the functions.

## [1.1.0] - 2016-05-19

### Added

- [Flow](http://flowtype.org/) declarations for each function
  in [the ".js.flow" style](http://flowtype.org/docs/declarations.html#declaration-files).
  Kudos to [@JohnyDays](https://github.com/JohnyDays). See related PRs:

  - [#205](https://github.com/date-fns/date-fns/pull/205)

  - [#207](https://github.com/date-fns/date-fns/pull/207)

## [1.0.0] - 2016-05-18

### Fixed

- `format` now returns the correct result for key `E`.

- Prevent `startOf...`, `endOf...` and `lastDayOf...` functions
  to return dates with an incorrect time when the date is modifying
  into another time zone.

- `parse` now parses years from 1 AD to 99 AD correctly.

- Fix a bug in `getISOWeek` appearing because of a changing time zone
  (e.g., when the given date is in DST and the start of the ISO year is not).

### Changed

- **BREAKING**: all functions are moved to the root of the library, so they
  are now accessible with `require('date-fns/name_of_function')` or
  `import nameOfFunction from 'date-fns/name_of_function'`.

  ```javascript
  // Before v1.0.0
  var addMonths = require('date-fns/src/add_months')

  // v1.0.0 onward
  var addMonths = require('date-fns/add_months')
  ```

- **BREAKING**: functions that had the last optional argument `weekStartsAt`
  (i.e. `endOfWeek`, `isSameWeek`, `lastDayOfWeek`, `setDay`, `startOfWeek`)
  now instead receive the object `options` with the property `options.weekStartsOn`
  as the last argument.

  ```javascript
  // Before v1.0.0
  var result = endOfWeek(new Date(2014, 8, 2), 1)

  // v1.0.0 onward
  var result = endOfWeek(new Date(2014, 8, 2), {weekStartsOn: 1})
  ```

- **BREAKING**: remove the function `getTimeSinceMidnight` that was used inside
  the other functions.

- **BREAKING**: `differenceInDays` now returns the number of full days instead
  of calendar days.

- **BREAKING**: `eachDay` and `isWithinRange` now throw an exception
  when the given range boundaries are invalid.

- Faster `isLeapYear`.

- *Internal*: make the documentation more verbose.

- *Internal*: convert the tests from Chai to power-assert allowing them
  to run against IE8.

### Added

- `addISOYears`

- `closestTo`

- `differenceInCalendarDays`

- `differenceInCalendarISOWeeks`

- `differenceInCalendarISOYears`

- `differenceInCalendarMonths`

- `differenceInCalendarQuarters`

- `differenceInCalendarWeeks`

- `differenceInCalendarYears`

- `differenceInHours`

- `differenceInISOYears`

- `differenceInMilliseconds`

- `differenceInMinutes`

- `differenceInMonths`

- `differenceInQuarters`

- `differenceInSeconds`

- `differenceInWeeks`

- `differenceInYears`

- `distanceInWords`

- `distanceInWordsToNow`

- `endOfISOWeek`

- `endOfISOYear`

- `endOfToday`

- `endOfTomorrow`

- `endOfYesterday`

- `getDaysInYear`

- `isDate`

- `isFriday`

- `isMonday`

- `isSameISOWeek`

- `isSameISOYear`

- `isSaturday`

- `isSunday`

- `isThisHour`

- `isThisISOWeek`

- `isThisISOYear`

- `isThisMinute`

- `isThisMonth`

- `isThisQuarter`

- `isThisSecond`

- `isThisWeek`

- `isThisYear`

- `isThursday`

- `isTomorrow`

- `isTuesday`

- `isValid`

- `isWednesday`

- `isYesterday`

- `lastDayOfISOWeek`

- `lastDayOfISOYear`

- `startOfISOWeek`

- `startOfToday`

- `startOfTomorrow`

- `startOfYesterday`

- `subISOYears`

- Add `Qo`, `W`, `Wo`, `WW`, `GG`, `GGGG`, `Z`, `ZZ`, `X`, `x` keys to `format`.

## [0.17.0] - 2015-09-29

### Fixed

- Fix a lot of bugs appearing when date is modifying into other time zone
  (e.g., when adding months and original date is in DST but new date is not).

- Prevent instances of Date to lose milliseconds value when passed to.
  `parse` in IE10.

### Changed

- `setISOWeek` now keeps time from original date.

- *Internal*: reuse `getDaysInMonth` inside of `addMonths`.

### Added

- `differenceInDays`

- `getTimeSinceMidnight`

- `format` now has new format key `aa`, which returns `a.m.`/`p.m.`
  as opposed to `a` that returns `am`/`pm`.

- Complete UMD package (for Bower and CDN).

## [0.16.0] - 2015-09-01

### Changed

- Use `parse` to clean date arguments in all functions.

- `parse` now fallbacks to `new Date` when the argument
  is not an ISO formatted date.

- *Internal*: reuse `getDaysInMonth` inside of `setMonth`.

### Added

- `addQuarters`

- `addWeeks`

- `endOfQuarter`

- `getDate`

- `getDay`

- `getDaysInMonth`

- `getHours`

- `getISOWeeksInYear`

- `getMilliseconds`

- `getMinutes`

- `getMonth`

- `getSeconds`

- `getYear`

- `isLeapYear`

- `isSameHour`

- `isSameMinute`

- `isSameQuarter`

- `isSameSecond`

- `lastDayOfQuarter`

- `lastDayOfWeek`

- `max`

- `min`

- `setDate`

- `setDay`

- `setHours`

- `setMilliseconds`

- `setMinutes`

- `setSeconds`

- `startOfQuarter`

- `subQuarters`

- `subWeeks`

## [0.15.0] - 2015-08-26

### Changed

- `format` now returns `a.m.`/`p.m.` instead of `am`/`pm`.

- `setMonth` now sets last day of month if original date was last day
  of longer month.

- *Internal*: Fix code style according to ESLint.

- *Internal*: Make tests run through all time zones.

### Added

- `getQuarter`

- `setQuarter`

- `getDayOfYear`

- `setDayOfYear`

- `isPast`

- `addSeconds`

- `subSeconds`

- `startOfSecond`

- `endOfSecond`

- `startOfMinute`

- `endOfMinute`

- `addMilliseconds`

- `subMilliseconds`

- `endOfYear`

- `addYears`

- `subYears`

- `lastDayOfYear`

- `lastDayOfMonth`

## [0.14.11] - 2015-08-21

### Fixed

- `format` now uses `parse` to avoid time zone bugs.

### Changed

- `setIsoWeek` now sets time to the start of the day.

## [0.14.10] - 2015-07-29

### Fixed

- `format` now behaves correctly with 12:00 am.

- `format` now behaves correctly with ordinal numbers.

### Added

- `compareAsc`

- `compareDesc`

- `addHours`

- `subHours`

- `isSameDay`

- `parse`

- `getISOYear`

- `setISOYear`

- `startOfISOYear`

- `getISOWeek`

- `setISOWeek`

## [0.14.9] - 2015-01-14

### Fixed

- `addMonths` now correctly behaves with February
  (see [#18](https://github.com/js-fns/date-fns/pull/18)).

## [0.14.8] - 2014-12-25

### Fixed

- `format` function now behaves correctly with `pm`/`am`.

## [0.14.6] - 2014-12-04

### Fixed

- Fix broken Bower support.

## [0.14.0] - 2014-11-05

### Added

- Bower package.

## [0.13.0] - 2014-10-22

### Added

- `addMinutes`

- `subMinutes`

- `isEqual`

- `isBefore`

- `isAfter`

## [0.12.1] - 2014-10-19

### Fixed

- Incorrect rounding in `DDD` formatter.

## [0.12.0] - 2014-10-15

### Added

- `isSameYear`

## [0.11.0] - 2014-10-15

### Added

- `isWithinRange`

## [0.10.0] - 2014-10-13

### Added

- `format`

- `startOfYear`

## [0.9.0] - 2014-10-10

### Changed

- *Internal*: simplify `isWeekend`

### Added

- `isFuture`

## [0.8.0] - 2014-10-09

### Changed

- *Internal*: reuse `addDays` inside of `subDays`.

### Added

- `addMonths`

- `subMonths`

- `setMonth`

- `setYear`

## [0.7.0] - 2014-10-08

### Added

- `isSameWeek`

## [0.6.0] - 2014-10-07

### Fixed

- Inconsistent behavior of `endOfMonth`.

### Added

- `isFirstDayOfMonth`

- `isLastDayOfMonth`

- `isSameMonth`

## [0.5.0] - 2014-10-07

### Added

- `addDays`

- `subDays`

## [0.4.0] - 2014-10-07

### Added

- `startOfWeek`

- `endOfWeek`

- `eachDay`

## [0.3.0] - 2014-10-06

### Changed

- `startOfDay` now sets milliseconds as well.

### Added

- `endOfDay`

- `startOfMonth`

- `endOfMonth`

## [0.2.0] - 2014-10-06

### Added

- `isToday`

- `isWeekend`

## 0.1.0 - 2014-10-06

### Added

- `startOfDay`

[Unreleased]: https://github.com/date-fns/date-fns/compare/v1.18.0...HEAD
[1.18.0]: https://github.com/date-fns/date-fns/compare/v1.17.0...v1.18.0
[1.17.0]: https://github.com/date-fns/date-fns/compare/v1.16.0...v1.17.0
[1.16.0]: https://github.com/date-fns/date-fns/compare/v1.15.1...v1.16.0
[1.15.1]: https://github.com/date-fns/date-fns/compare/v1.15.0...v1.15.1
[1.15.0]: https://github.com/date-fns/date-fns/compare/v1.14.1...v1.15.0
[1.14.1]: https://github.com/date-fns/date-fns/compare/v1.14.0...v1.14.1
[1.14.0]: https://github.com/date-fns/date-fns/compare/v1.13.0...v1.14.0
[1.13.0]: https://github.com/date-fns/date-fns/compare/v1.12.1...v1.13.0
[1.12.1]: https://github.com/date-fns/date-fns/compare/v1.12.0...v1.12.1
[1.12.0]: https://github.com/date-fns/date-fns/compare/v1.11.2...v1.12.0
[1.11.2]: https://github.com/date-fns/date-fns/compare/v1.11.1...v1.11.2
[1.11.1]: https://github.com/date-fns/date-fns/compare/v1.11.0...v1.11.1
[1.11.0]: https://github.com/date-fns/date-fns/compare/v1.10.0...v1.11.0
[1.10.0]: https://github.com/date-fns/date-fns/compare/v1.9.0...v1.10.0
[1.9.0]: https://github.com/date-fns/date-fns/compare/v1.8.1...v1.9.0
[1.8.1]: https://github.com/date-fns/date-fns/compare/v1.8.0...v1.8.1
[1.8.0]: https://github.com/date-fns/date-fns/compare/v1.7.0...v1.8.0
[1.7.0]: https://github.com/date-fns/date-fns/compare/v1.6.0...v1.7.0
[1.6.0]: https://github.com/date-fns/date-fns/compare/v1.5.2...v1.6.0
[1.5.2]: https://github.com/date-fns/date-fns/compare/v1.5.1...v1.5.2
[1.5.1]: https://github.com/date-fns/date-fns/compare/v1.5.0...v1.5.1
[1.5.0]: https://github.com/date-fns/date-fns/compare/v1.4.0...v1.5.0
[1.4.0]: https://github.com/date-fns/date-fns/compare/v1.3.0...v1.4.0
[1.3.0]: https://github.com/date-fns/date-fns/compare/v1.2.0...v1.3.0
[1.2.0]: https://github.com/date-fns/date-fns/compare/v1.1.1...v1.2.0
[1.1.1]: https://github.com/date-fns/date-fns/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/date-fns/date-fns/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/date-fns/date-fns/compare/v0.17.0...v1.0.0
[0.17.0]: https://github.com/date-fns/date-fns/compare/v0.16.0...v0.17.0
[0.16.0]: https://github.com/date-fns/date-fns/compare/v0.15.0...v0.16.0
[0.15.0]: https://github.com/date-fns/date-fns/compare/v0.14.11...v0.15.0
[0.14.11]: https://github.com/date-fns/date-fns/compare/v0.14.10...v0.14.11
[0.14.10]: https://github.com/date-fns/date-fns/compare/v0.14.9...v0.14.10
[0.14.9]: https://github.com/date-fns/date-fns/compare/v0.14.8...v0.14.9
[0.14.8]: https://github.com/date-fns/date-fns/compare/v0.14.6...v0.14.8
[0.14.6]: https://github.com/date-fns/date-fns/compare/v0.14.0...v0.14.6
[0.14.0]: https://github.com/date-fns/date-fns/compare/v0.13.0...v0.14.0
[0.13.0]: https://github.com/date-fns/date-fns/compare/v0.12.1...v0.13.0
[0.12.1]: https://github.com/date-fns/date-fns/compare/v0.12.0...v0.12.1
[0.12.0]: https://github.com/date-fns/date-fns/compare/v0.11.0...v0.12.0
[0.11.0]: https://github.com/date-fns/date-fns/compare/v0.10.0...v0.11.0
[0.10.0]: https://github.com/date-fns/date-fns/compare/v0.9.0...v0.10.0
[0.9.0]: https://github.com/date-fns/date-fns/compare/v0.8.0...v0.9.0
[0.8.0]: https://github.com/date-fns/date-fns/compare/v0.7.0...v0.8.0
[0.7.0]: https://github.com/date-fns/date-fns/compare/v0.6.0...v0.7.0
[0.6.0]: https://github.com/date-fns/date-fns/compare/v0.5.0...v0.6.0
[0.5.0]: https://github.com/date-fns/date-fns/compare/v0.4.0...v0.5.0
[0.4.0]: https://github.com/date-fns/date-fns/compare/v0.3.0...v0.4.0
[0.3.0]: https://github.com/date-fns/date-fns/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/date-fns/date-fns/compare/v0.1.0...v0.2.0
