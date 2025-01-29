# MongoDB $inc Operator Error with String Value

This repository demonstrates a common error when using the `$inc` operator in MongoDB update operations. The error arises from attempting to increment a numerical field with a string value.

## Problem
The following JavaScript code snippet shows the incorrect use of the `$inc` operator:

```javascript
db.collection('myCollection').updateOne({ _id: 1 }, { $inc: { count: '1' } });
```

This results in a MongoDB error, because the `$inc` operator expects a numerical value.

## Solution
The solution is to use a numerical value instead of a string.  The corrected code is:

```javascript
db.collection('myCollection').updateOne({ _id: 1 }, { $inc: { count: 1 } });
```

This will correctly increment the `count` field by 1.