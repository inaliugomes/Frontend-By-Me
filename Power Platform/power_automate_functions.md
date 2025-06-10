# Power Automate Functions

## Text Functions

| Function | Description | Parameters |
|----------|-------------|------------|
| `chunk` | Split a string or collection into equal-length chunks. | `collection text` |
| `concat` | Combine multiple strings into one. | `text1 text2 …` |
| `endsWith` | Check if a string ends with a specified substring. | `text searchText` |
| `formatNumber` | Convert a number to a string based on a specified format. | `number format locale` |
| `guid` | Generate a globally unique identifier (GUID) as a string. | `format` |
| `indexOf` | Find the starting position of a substring. | `text searchText` |
| `isFloat` | Check if a string is a floating-point number. | `value locale` |
| `isInt` | Check if a string is an integer. | `string` |
| `lastIndexOf` | Find the starting position of the last occurrence of a substring. | `text searchText` |
| `length` | Count the items in a string. | `collection` |
| `nthIndexOf` | Find the starting position of the nth occurrence of a substring. | `text searchText occurence` |
| `replace` | Replace a substring with another string. | `text oldText newText` |
| `slice` | Return a substring based on starting and ending positions. | `text startIndex endIndex` |
| `split` | Split a string into an array of substrings based on a specified delimiter. | `text delimiter` |
| `startsWith` | Check if a string starts with a specified substring. | `text searchText` |
| `substring` | Return characters from a string starting at a specified position. | `text startIndex length` |
| `toLower` | Convert a string to lowercase. | `text` |
| `toUpper` | Convert a string to uppercase. | `text` |
| `trim` | Remove leading and trailing whitespace from a string. | `text` |

## Collection Functions

| Function | Description | Parameters |
|----------|-------------|------------|
| `chunk` | Split a collection into equal-length parts. | `collection length` |
| `contains` | Check if a collection contains an item. | `collection value` |
| `empty` | Check if a collection is empty. | `collection` |
| `first` | Return the first item in a collection. | `first` |
| `intersection` | Return common items in specified collections. | `collection1 collection2 …` |
| `item` | Get the current item in a loop. | `value locale` |
| `join` | Combine array items into a string with a specified delimiter. | `collection delimiter` |
| `last` | Return the last item in a collection. | `collection` |
| `length` | Count the items in an array | `collection` |
| `reverse` | Reverse the order of array items. | `collection` |
| `skip` | Remove and return items after a specified count. | `collection count` |
| `sort` | Sort items in a collection | `collection sortBy` |
| `take` | Return the first few items in a collection. | `collection count` |
| `union` | Combine items from multiple collections. | `collection1 collection2 …` |

## Logical Comparison Functions

| Function | Description | Parameters |
|----------|-------------|------------|
| `and` | Check if all expressions are true. | `expression1 expression2 …` |
| `equals` | Check if both values are equal. | `object1 object2` |
| `greater` | Check if the first value is greater than the second. | `value compareTo` |
| `greaterOrEquals` | Check if the first value is greater than or equal to the second. | `value compareTo` |
| `if` | Return a value based on whether an expression is true or false. | `expression valueIfTrue valueIfFalse` |
| `isFloat` | Check if a string is a floating-point number. | `value locale` |
| `isInt` | Check if a string is an integer. | `string` |
| `less` | Check if the first value is less than the second. | `value compareTo` |
| `lessOrEquals` | Check if the first value is less than or equal to the second. | `value compareTo` |
| `not` | Check if an expression is false. | `expression` |
| `or` | Check if at least one expression is true. | `expression1 expression2 …` |

## Conversion Functions

| Function | Description | Parameters |
|----------|-------------|------------|
| `array` | Convert a single input to an array. | `value` |
| `base64` | Encode a string to base64. | `value` |
| `base64ToBinary` | Convert a base64 string to binary. | `value` |
| `base64ToString` | Convert a base64 string to plain text. | `value` |
| `binary` | Convert an input to binary. | `value` |
| `bool` | Convert an input to a Boolean value. | `value` |
| `createArray` | Convert an input to a Boolean value. | `object1 object2 …` |
| `dataUri` | Get the data URI of an input. | `value` |
| `dataUriToBinary` | Convert a data URI to binary. | `value` |
| `dataUriToString` | Convert a data URI to plain text. | `value` |
| `decimal` | Convert a decimal string to a decimal number. | `value` |
| `decodeBase64` | Decode a base64 string to plain text. | `value` |
| `decodeDataUri` | Convert a data URI to binary. | `value` |
| `decodeUriComponent` | Decode a URI component. | `value` |
| `encodeUriComponent` | Encode a URI component. | `value` |
| `float` | Convert an input to a floating point number. | `value` |
| `int` | Convert a string to an integer. | `value` |
| `json` | Parse a string or XML as JSON. | `value` |
| `string` | Convert an input to a string. | `value` |
| `uriComponent` | Encode an input as a URI component. | `value` |
| `uriComponentToBinary` | Convert a URI component to binary. | `value` |
| `uriComponentToString` | Convert a URI component to plain text. | `value` |
| `xml` | Convert a string to XML. | `value` |

## Math Functions

| Function | Description | Parameters |
|----------|-------------|------------|
| `add` | Add two numbers. | `number1 number2` |
| `div` | Divide two numbers. | `divided divisor` |
| `max` | Get the highest value in a set or array | `number1 number2 …` |
| `min` | Get the lowest value in a set or array | `number1 number2 …` |
| `mod` | Get the remainder of division. | `divided divisor` |
| `mul` | Multiply two numbers. | `number1 number2` |
| `rand` | Generate a random integer in a specified range | `minValue maxValue` |
| `range` | Create an integer array from a starting number | `startIndex count` |
| `sub` | Subtract two numbers. | `number1 number2` |

## Date And Time Functions

| Function | Description | Parameters |
|----------|-------------|------------|
| `addDays` | Add days to a timestamp. | `timestamp days format` |
| `addHours` | Add hours to a timestamp. | `timestamp hours format` |
| `addMinutes` | Add minutes to a timestamp. | `timestamp minutes format` |
| `addSeconds` | Add seconds to a timestamp. | `timestamp seconds format` |
| `addToTime` | Add specified time units to a timestamp. | `timestamp interval timeUnit format` |
| `convertFromUtc` | Convert UTC to the target time zone. | `timestamp destinationTimeZone format` |
| `convertTimeZone` | Convert between time zones. | `timestamp sourceTimeZone destinationTimeZone format` |
| `convertToUtc` | Convert to UTC from a time zone. | `timestamp sourceTimeZone format` |
| `dateDifference` | Get the difference between two dates. | `startDate endDate` |
| `dayOfMonth` | Get the day of the month. | `timestamp` |
| `dayOfWeek` | Get the day of the week. | `timestamp` |
| `dayOfYear` | Get the day of the year. | `timestamp` |
| `formatDateTime` | Format a timestamp | `timestamp format locale` |
| `getFutureTime` | Get current time plus specified units. | `interval timeUnit format` |
| `getPastTime` | Get current time minus specified units. | `interval timeUnit format` |
| `parseDateTime` | Parse a string to a timestamp. | `timestamp locale format` |
| `startOfDay` | Get the start of the day. | `timestamp format` |
| `startOfHour` | Get the start of the hour. | `timestamp format` |
| `startOfMonth` | Get the start of the month. | `timestamp format` |
| `subtractFromTime` | Subtract time units from a timestamp. | `timestamp interval timeUnit format` |
| `ticks` | Get the ticks value for a timestamp. | `timestamp` |
| `utcNow` | Get the current UTC timestamp. | `format` |

## Workflow Functions

| Function | Description | Parameters |
|----------|-------------|------------|
| `action` | Get the current action’s output. | `property` |
| `actionBody` | Get an action’s body output. | `actionName` |
| `actionOutputs` | Get an action’s output at runtime | `actionName` |
| `actions` | Get an action’s output at runtime, or values from other JSON name-and-value pairs | `actionName property` |
| `body` | Get an action’s body output. | `actionName` |
| `formDataMultiValues` | Create an array with values matching a key name. | `actionName key` |
| `formDataValue` | Get a value matching a key name. | `actionName key` |
| `item` | Get the current item in a loop. | `` |
| `items` | Get the current item in a loop. | `` |
| `iterationIndexes` | Get the index value in an Until loop. | `actionName` |
| `listCallbackUrl` | Get the “callback URL” for a trigger or action. | `text` |
| `multipartBody` | Get the body for a part in a multipart output. | `actionName index` |
| `outputs` | Get an action’s output. | `actionName` |
| `parameters` | Get the value of a parameter. | `parameterName` |
| `result` | Get inputs and outputs from scoped actions. | `scopedActionName` |
| `trigger` | Get a trigger’s output. | `` |
| `triggerBody` | Get a trigger’s body output. | `` |
| `triggerFormDataValue` | Get a value matching a key name in trigger outputs. | `key` |
| `triggerMultipartBody` | Get the body for a part in a trigger’s output. | `index` |
| `triggerFormDataMultiValues` | Create an array with values matching a key name. | `` |
| `triggerOutputs` | Get a trigger’s output. | `key` |
| `variables` | Get the value of a variable. | `variableName` |
| `workflow` | Get details about the workflow. | `property` |

## URI Parsing Functions

| Function | Description | Parameters |
|----------|-------------|------------|
| `uriHost` | Get the host value of a URI. | `uri` |
| `uriPath` | Get the path value of a URI. | `uri` |
| `uriPathAndQuery` | Get the path and query of a URI. | `uri` |
| `uriPort` | Get the port value of a URI. | `uri` |
| `uriQuery` | Get the query value of a URI. | `uri` |
| `uriScheme` | Get the scheme value of a URI. | `uri` |

## JSON & XML Manipulation Functions

| Function | Description | Parameters |
|----------|-------------|------------|
| `addProperty` | Add a property and its value to a JSON object. | `object property value` |
| `coalesce` | Return the first non-null value from one or more parameters | `value1 value2 …` |
| `removeProperty` | Remove a property from a JSON object. | `object property` |
| `setProperty` | Set a property value in a JSON object. | `object property value` |
| `xpath` | Return nodes or values matching an XPath. | `xml path` |

