1. The bug is that num1 and num2 are strings because document.getElementById().value always returns a string. So num1 + num2 is string concatenation instead of addition.

2. The fix is to convert num1 and num2 to numbers before adding them.
