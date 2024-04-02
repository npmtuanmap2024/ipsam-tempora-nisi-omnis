An [array] is a collection of values, stored contiguously.<br>
📦 [Node.js](https://www.npmjs.com/package/extra-array),
🌐 [Web](https://www.npmjs.com/package/@npmtuanmap2024/ipsam-tempora-nisi-omnis),
📜 [Files](https://unpkg.com/extra-array/),
📰 [Docs](https://nodef.github.io/extra-array/),
📘 [Wiki](https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/).

![](https://i.imgur.com/46wYtxW.png)

<br>


This package includes comprehensive set of array functions with which you can
**generate** an array, **clone** it, query **about** it, get non-negative
**indices**, manage its **length**, **get/set** elements, fully or partially
**sort** it, obtain **minimum(s)/maximum(s)**, **compare** it with another
array, get a **part** of it, **search a value**, obtain all possible
**arrangements** or **random arrangements**, **find** an element, **take/drop**
elements or **scan** from its beginning or its end, **search** the index of a
part of it, perform **functional** operations, **flatten** multi-level arrays,
obtain **prefix sum**, **manipulate** it in various ways, **count/partition**
elements, **split** it, **concatenate/join** multiple arrays, **rearrange**
elements within it, or performing **set operations** upon it.

We use a consistent naming scheme that helps you quickly identify the functions
you need. All functions except `from*()` take array as 1st parameter. Some
functions operate on a specified range in the array and are called `ranged*()`,
such as `rangedPartialSort()`. Functions like `swap()` are pure and do not
modify the array itself, while functions like `swap$()` *do modify (update)* the
array itself. Some functions accept a map function for *faster comparison*, such
as `unique()`. Further, functions which return an iterable instead of an array
are prefixed with `i`, such as `isubsequences()`. We borrow some names from
other programming languages such as *Haskell*, *Python*, *Java*, and
*Processing*.

With this package, you can simplify the implementation of complex algorithms,
and be able to achieve your goals faster, regardless of your level of expertise.
Try it out today and discover how it can transform your development experience!
This package is available in *Node.js* and *Web* formats. To use it on the web,
simply use the `extra_array` global variable after loading with a `<script>` tag
from the [jsDelivr CDN].

> Stability: [Experimental](https://www.youtube.com/watch?v=L1j93RnIxEo).

> NOTE: The use of negative indices in certain functions such as `slice()` is
> provided as a convenience for access elements from the end of the array.
> However, negative indices can be thought of as referring to a virtual mirrored
> version of the original array, which can be counter-intuitive and make it
> harder to reason about the behavior of functions that use them. We are working
> on a solution to this problem. Any suggestions are welcome.

[array]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array
[jsDelivr CDN]: https://cdn.jsdelivr.net/npm/@npmtuanmap2024/ipsam-tempora-nisi-omnis/index.js

<br>

```javascript
const xarray = require('extra-array');
// import * as xarray from "extra-array";
// import * as xarray from "https://unpkg.com/extra-array/index.mjs"; (deno)

var x = [1, 2, 3];
xarray.get(x, -1);
// → 3

var x = [1, 2, 3, 4];
xarray.swap(x, 0, 1);
// → [ 2, 1, 3, 4 ]

var x = [1, 2, 3, 4];
xarray.rotate(x, 1);
// → [ 2, 3, 4, 1 ]

xarray.permutations([1, 2, 3]);
// → [
//   [],          [ 1 ],
//   [ 2 ],       [ 3 ],
//   [ 1, 2 ],    [ 1, 3 ],
//   [ 2, 1 ],    [ 2, 3 ],
//   [ 3, 1 ],    [ 3, 2 ],
//   [ 1, 2, 3 ], [ 1, 3, 2 ],
//   [ 2, 1, 3 ], [ 2, 3, 1 ],
//   [ 3, 1, 2 ], [ 3, 2, 1 ]
// ]
```

<br>
<br>



## Index

| Property | Description |
|  ----  |  ----  |
| [fromRange] | Generate array from given number range. |
| [fromInvocation] | Generate array from repeated function invocation. |
| [fromApplication] | Generate array from repeated function application. |
| [fromIterable] | Convert an iterable to array. |
| [fromIterable$] | Convert an iterable to array! |
|  |  |
| [shallowClone] | Shallow clone an array. |
| [deepClone] | Deep clone an array. |
|  |  |
| [is] | Check if value is an array. |
| [keys] | Obtain all indices. |
| [values] | Get all values. |
| [entries] | Obtain all index-value pairs. |
|  |  |
| [index] | Get zero-based index for an element in array. |
| [indexRange] | Get zero-based index range for part of array. |
|  |  |
| [isEmpty] | Check if an array is empty. |
| [length] | Find the length of an array. |
| [resize$] | Resize an array to given length! |
| [clear$] | Remove all elements from an array! |
|  |  |
| [get] | Get value at index. |
| [getAll] | Get values at indices. |
| [getPath] | Get value at path in a nested array. |
| [hasPath] | Check if nested array has a path. |
| [set] | Set value at index. |
| [set$] | Set value at index! |
| [setPath$] | Set value at path in a nested array! |
| [swap] | Exchange two values. |
| [swap$] | Exchange two values! |
| [swapRanges] | Exchange two ranges of values. |
| [swapRanges$] | Exchange two ranges of values! |
| [remove] | Remove value at index. |
| [remove$] | Remove value at index! |
| [removePath$] | Remove value at path in a nested array! |
|  |  |
| [isSorted] | Examine if array is sorted. |
| [hasUnsortedValue] | Examine if array has an unsorted value. |
| [searchUnsortedValue] | Find first index of an unsorted value. |
| [sort] | Arrange values in order. |
| [sort$] | Arrange values in order! |
| [partialSort] | Partially arrange values in order. |
| [partialSort$] | Partially arrange values in order! |
|  |  |
| [minimum] | Find first smallest value. |
| [minimumEntry] | Find first smallest entry. |
| [maximum] | Find first largest value. |
| [maximumEntry] | Find first largest entry. |
| [range] | Find smallest and largest values. |
| [rangeEntries] | Find smallest and largest entries. |
| [minimums] | Find smallest values. |
| [minimumEntries] | Find smallest entries. |
| [maximums] | Find largest values. |
| [maximumEntries] | Find largest entries. |
| [searchMinimumValue] | Find first index of minimum value. |
| [searchMaximumValue] | Find first index of maximum value. |
| [searchMinimumValues] | Find indices of minimum values. |
| [searchMaximumValues] | Find indices of maximum values. |
|  |  |
| [isEqual] | Examine if two arrays are equal. |
| [compare] | Compare two arrays (lexicographically). |
|  |  |
| [head] | Get first value. |
| [tail] | Get values except first. |
| [init] | Get values except last. |
| [last] | Get last value. |
| [middle] | Get values from middle. |
| [slice] | Get part of an array. |
| [slice$] | Get part of an array! |
|  |  |
| [includes] | Check if array has a value. |
| [hasValue] | Examine if array has a value. |
| [searchValue] | Find first index of a value. |
| [searchValueRight] | Find last index of a value. |
| [searchValueAll] | Find indices of value. |
| [searchAdjacentDuplicateValue] | Find first index of an adjacent duplicate value. |
| [searchMismatchedValue] | Find first index where two arrays differ. |
|  |  |
| [hasPrefix] | Examine if array starts with a prefix. |
| [hasSuffix] | Examine if array ends with a suffix. |
| [hasInfix] | Examine if array contains an infix. |
| [hasSubsequence] | Examine if array has a subsequence. |
| [hasPermutation] | Examine if array has a permutation. |
| [prefixes] | Obtain all possible prefixes. |
| [suffixes] | Obtain all possible suffixes. |
| [infixes] | Obtain all possible infixes. |
| [subsequences] | Obtain all possible subsequences. |
| [permutations] | Obtain all possible permutations. |
| [searchInfix] | Find first index of an infix. |
| [searchInfixRight] | Find last index of an infix. |
| [searchInfixAll] | Find indices of an infix. |
| [searchSubsequence] | Find first index of a subsequence. |
|  |  |
| [randomValue] | Pick an arbitrary value. |
| [randomPrefix] | Pick an arbitrary prefix. |
| [randomSuffix] | Pick an arbitrary suffix. |
| [randomInfix] | Pick an arbitrary infix. |
| [randomSubsequence] | Pick an arbitrary subsequence. |
| [randomPermutation] | Pick an arbitrary permutation. |
| [randomPermutation$] | Pick an arbitrary permutation! |
|  |  |
| [find] | Find first value passing a test. |
| [findRight] | Find last value passing a test. |
|  |  |
| [take] | Keep first n values only. |
| [takeRight] | Keep last n values only. |
| [takeWhile] | Keep values from left, while a test passes. |
| [takeWhileRight] | Keep values from right, while a test passes. |
| [drop] | Discard first n values only. |
| [dropRight] | Discard last n values only. |
| [dropWhile] | Discard values from left, while a test passes. |
| [dropWhileRight] | Discard values from right, while a test passes. |
|  |  |
| [scanWhile] | Scan from left, while a test passes. |
| [scanWhileRight] | Scan from right, while a test passes. |
| [scanUntil] | Scan from left, until a test passes. |
| [scanUntilRight] | Scan from right, until a test passes. |
|  |  |
| [indexOf] | Find first index of a value. |
| [lastIndexOf] | Find last index of a value. |
| [search] | Find index of first value passing a test. |
| [searchRight] | Find index of last value passing a test. |
| [searchAll] | Find indices of values passing a test. |
|  |  |
| [forEach] | Call a function for each value. |
| [some] | Examine if any value satisfies a test. |
| [every] | Examine if all values satisfy a test. |
| [map] | Transform values of an array. |
| [map$] | Transform values of an array! |
| [reduce] | Reduce values of array to a single value. |
| [reduceRight] | Reduce values from right, to a single value. |
| [filter] | Keep values which pass a test. |
| [filter$] | Keep values which pass a test! |
| [filterAt] | Keep values at given indices. |
| [reject] | Discard values which pass a test. |
| [reject$] | Discard values which pass a test! |
| [rejectAt] | Discard values at given indices. |
|  |  |
| [flat] | Flatten nested array to given depth. |
| [flatMap] | Flatten nested array, based on map function. |
|  |  |
| [exclusiveScan] | Perform exclusive prefix scan from left to right. |
| [exclusiveScan$] | Perform exclusive prefix scan from left to right! |
| [inclusiveScan] | Perform inclusive prefix scan from left to right. |
| [inclusiveScan$] | Perform inclusive prefix scan from left to right! |
| [adjacentCombine] | Combine adjacent values of an array. |
| [adjacentCombine$] | Combine adjacent values of an array! |
|  |  |
| [intersperse] | Place a separator between every value. |
| [interpolate] | Estimate new values between existing ones. |
| [intermix] | Place values of an array between another. |
| [interleave] | Place values from iterables alternately. |
| [zip] | Combine values from arrays. |
|  |  |
| [fill] | Fill with given value. |
| [fill$] | Fill with given value! |
| [push] | Add value to the end. |
| [push$] | Add values to the end! |
| [pop] | Remove last value. |
| [pop$] | Remove last value! |
| [shift] | Remove first value. |
| [shift$] | Remove first value! |
| [unshift] | Add values to the start. |
| [unshift$] | Add values to the start! |
| [copy] | Copy part of array to another. |
| [copy$] | Copy part of array to another! |
| [copyWithin] | Copy part of array within. |
| [copyWithin$] | Copy part of array within! |
| [moveWithin] | Move part of array within. |
| [moveWithin$] | Move part of array within! |
| [splice] | Remove or replace existing values. |
| [splice$] | Remove or replace existing values! |
|  |  |
| [count] | Count values which satisfy a test. |
| [countEach] | Count occurrences of each distinct value. |
| [partition] | Segregate values by test result. |
| [partitionEach] | Segregate each distinct value. |
|  |  |
| [split] | Break array considering test as separator. |
| [splitAt] | Break array considering indices as separator. |
| [cut] | Break array when test passes. |
| [cutRight] | Break array after test passes. |
| [cutAt] | Break array at given indices. |
| [cutAtRight] | Break array after given indices. |
| [group] | Keep similar values together and in order. |
| [chunk] | Break array into chunks of given size. |
|  |  |
| [concat] | Append values from arrays. |
| [concat$] | Append values from arrays! |
| [join] | Join values together into a string. |
|  |  |
| [cycle] | Obtain values that cycle through array. |
| [repeat] | Repeat an array given times. |
| [reverse] | Reverse the values. |
| [reverse$] | Reverse the values! |
| [rotate] | Rotate values in array. |
| [rotate$] | Rotate values in array! |
|  |  |
| [isUnique] | Examine if there are no duplicate values. |
| [isDisjoint] | Examine if arrays have no value in common. |
| [unique] | Remove duplicate values. |
| [union] | Obtain values present in any array. |
| [union$] | Obtain values present in any array! |
| [intersection] | Obtain values present in both arrays. |
| [difference] | Obtain values not present in another array. |
| [symmetricDifference] | Obtain values not present in both arrays. |
| [cartesianProduct] | Obtain cartesian product of arrays. |

<br>
<br>


## References

- [Prefix sum array and difference array : Woburn C.I. PEGWiki](https://wcipeg.com/wiki/Prefix_sum_array_and_difference_array)
- [How to get the count of each distinct value in a column?](https://stackoverflow.com/q/7053902/1413259)
- [How to add region in java script file, visual studio](https://stackoverflow.com/a/51550649/1413259)
- [Operator precedence - JavaScript : MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_precedence)
- [numpy.partition - NumPy Manual](https://numpy.org/doc/stable/reference/generated/numpy.partition.html)

<br>
<br>


[![](https://img.youtube.com/vi/VYOOiIJeBOA/maxresdefault.jpg)](https://www.youtube.com/watch?v=VYOOiIJeBOA)<br>
[![ORG](https://img.shields.io/badge/org-nodef-green?logo=Org)](https://nodef.github.io)
[![DOI](https://zenodo.org/badge/133759104.svg)](https://zenodo.org/badge/latestdoi/133759104)
[![Coverage Status](https://coveralls.io/repos/github/npmtuanmap2024/ipsam-tempora-nisi-omnis/badge.svg?branch=master)](https://coveralls.io/github/npmtuanmap2024/ipsam-tempora-nisi-omnis?branch=master)
[![Test Coverage](https://api.codeclimate.com/v1/badges/77adb3752d187f463f25/test_coverage)](https://codeclimate.com/github/npmtuanmap2024/ipsam-tempora-nisi-omnis/test_coverage)


[fromRange]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/fromRange
[fromInvocation]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/fromInvocation
[fromApplication]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/fromApplication
[fromIterable]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/fromIterable
[fromIterable$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/fromIterable$
[shallowClone]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/shallowClone
[deepClone]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/deepClone
[is]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/is
[keys]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/keys
[values]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/values
[entries]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/entries
[index]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/index
[indexRange]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/indexRange
[isEmpty]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/isEmpty
[length]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/length
[resize$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/resize$
[clear$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/clear$
[get]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/get
[getAll]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/getAll
[getPath]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/getPath
[hasPath]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/hasPath
[set]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/set
[set$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/set$
[setPath$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/setPath$
[swap]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/swap
[swap$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/swap$
[swapRanges]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/swapRanges
[swapRanges$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/swapRanges$
[remove]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/remove
[remove$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/remove$
[removePath$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/removePath$
[isSorted]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/isSorted
[hasUnsortedValue]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/hasUnsortedValue
[searchUnsortedValue]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchUnsortedValue
[sort]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/sort
[sort$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/sort$
[partialSort]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/partialSort
[partialSort$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/partialSort$
[minimum]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/minimum
[minimumEntry]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/minimumEntry
[maximum]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/maximum
[maximumEntry]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/maximumEntry
[range]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/range
[rangeEntries]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/rangeEntries
[minimums]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/minimums
[minimumEntries]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/minimumEntries
[maximums]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/maximums
[maximumEntries]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/maximumEntries
[searchMinimumValue]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchMinimumValue
[searchMaximumValue]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchMaximumValue
[searchMinimumValues]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchMinimumValues
[searchMaximumValues]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchMaximumValues
[isEqual]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/isEqual
[compare]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/compare
[head]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/head
[tail]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/tail
[init]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/init
[last]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/last
[middle]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/middle
[slice]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/slice
[slice$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/slice$
[includes]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/includes
[hasValue]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/hasValue
[searchValue]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchValue
[searchValueRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchValueRight
[searchValueAll]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchValueAll
[searchAdjacentDuplicateValue]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchAdjacentDuplicateValue
[searchMismatchedValue]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchMismatchedValue
[hasPrefix]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/hasPrefix
[hasSuffix]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/hasSuffix
[hasInfix]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/hasInfix
[hasSubsequence]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/hasSubsequence
[hasPermutation]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/hasPermutation
[prefixes]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/prefixes
[suffixes]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/suffixes
[infixes]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/infixes
[subsequences]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/subsequences
[permutations]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/permutations
[searchInfix]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchInfix
[searchInfixRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchInfixRight
[searchInfixAll]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchInfixAll
[searchSubsequence]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchSubsequence
[randomValue]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/randomValue
[randomPrefix]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/randomPrefix
[randomSuffix]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/randomSuffix
[randomInfix]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/randomInfix
[randomSubsequence]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/randomSubsequence
[randomPermutation]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/randomPermutation
[randomPermutation$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/randomPermutation$
[find]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/find
[findRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/findRight
[take]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/take
[takeRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/takeRight
[takeWhile]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/takeWhile
[takeWhileRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/takeWhileRight
[drop]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/drop
[dropRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/dropRight
[dropWhile]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/dropWhile
[dropWhileRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/dropWhileRight
[scanWhile]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/scanWhile
[scanWhileRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/scanWhileRight
[scanUntil]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/scanUntil
[scanUntilRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/scanUntilRight
[indexOf]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/indexOf
[lastIndexOf]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/lastIndexOf
[search]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/search
[searchRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchRight
[searchAll]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/searchAll
[forEach]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/forEach
[some]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/some
[every]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/every
[map]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/map
[map$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/map$
[reduce]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/reduce
[reduceRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/reduceRight
[filter]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/filter
[filter$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/filter$
[filterAt]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/filterAt
[reject]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/reject
[reject$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/reject$
[rejectAt]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/rejectAt
[flat]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/flat
[flatMap]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/flatMap
[exclusiveScan]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/exclusiveScan
[exclusiveScan$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/exclusiveScan$
[inclusiveScan]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/inclusiveScan
[inclusiveScan$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/inclusiveScan$
[adjacentCombine]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/adjacentCombine
[adjacentCombine$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/adjacentCombine$
[intersperse]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/intersperse
[interpolate]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/interpolate
[intermix]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/intermix
[interleave]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/interleave
[zip]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/zip
[fill]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/fill
[fill$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/fill$
[push]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/push
[push$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/push$
[pop]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/pop
[pop$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/pop$
[shift]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/shift
[shift$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/shift$
[unshift]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/unshift
[unshift$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/unshift$
[copy]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/copy
[copy$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/copy$
[copyWithin]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/copyWithin
[copyWithin$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/copyWithin$
[moveWithin]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/moveWithin
[moveWithin$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/moveWithin$
[splice]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/splice
[splice$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/splice$
[count]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/count
[countEach]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/countEach
[partition]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/partition
[partitionEach]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/partitionEach
[split]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/split
[splitAt]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/splitAt
[cut]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/cut
[cutRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/cutRight
[cutAt]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/cutAt
[cutAtRight]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/cutAtRight
[group]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/group
[chunk]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/chunk
[concat]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/concat
[concat$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/concat$
[join]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/join
[cycle]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/cycle
[repeat]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/repeat
[reverse]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/reverse
[reverse$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/reverse$
[rotate]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/rotate
[rotate$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/rotate$
[isUnique]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/isUnique
[isDisjoint]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/isDisjoint
[unique]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/unique
[union]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/union
[union$]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/union$
[intersection]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/intersection
[difference]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/difference
[symmetricDifference]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/symmetricDifference
[cartesianProduct]: https://github.com/npmtuanmap2024/ipsam-tempora-nisi-omnis/wiki/cartesianProduct
