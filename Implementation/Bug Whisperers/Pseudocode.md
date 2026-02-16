# Pseudocode

In-Class Exercise - Wednesday, 2/11/2026







#### Main Program:



START



Print startup instructions



REPEAT

&nbsp;   stringA ← readValue("Enter first number")

UNTIL validateInput(stringA)



REPEAT

&nbsp;   stringB ← readValue("Enter second number")

UNTIL validateInput(stringB)



num1 ← normalizeToDigits(stringA)

num2 ← normalizeToDigits(stringB)



numSum ← addNumbers(num1, num2)



IF overflow occurred THEN

&nbsp;   print error message

&nbsp;   EXIT

END IF



result ← digitRootSum(numSum)



print "Final single digit result: " + result



END







#### User Input Module:



FUNCTION readValue(promptMessage)

&nbsp;   print promptMessage

&nbsp;   input ← read line from user

&nbsp;   RETURN input

END FUNCTION





FUNCTION validateInput(inputString)



&nbsp;   IF inputString contains invalid characters THEN

&nbsp;       print "Invalid input. Please try again."

&nbsp;       RETURN false

&nbsp;   END IF



&nbsp;   RETURN true



END FUNCTION









#### Normalizer Module:



FUNCTION normalizeToDigits(rawString)



&nbsp;   trim whitespace from rawString



&nbsp;   remove leading + or - sign if present



&nbsp;   remove decimal point if present



&nbsp;   IF result is empty THEN

&nbsp;       RETURN "0"

&nbsp;   END IF



&nbsp;   RETURN digit-only string



END FUNCTION







#### Add Module:



FUNCTION addNumbers(num1, num2)



&nbsp;   convert num1 to integer

&nbsp;   convert num2 to integer



&nbsp;   sum ← num1 + num2



&nbsp;   RETURN sum



END FUNCTION







#### Recursive Digit Reduction Module:



FUNCTION digitRootSum(n)



&nbsp;   IF n < 10 THEN

&nbsp;       RETURN n        // base case

&nbsp;   END IF



&nbsp;   leastDigit ← n MOD 10

&nbsp;   remaining ← n DIV 10



&nbsp;   newSum ← leastDigit + remaining



&nbsp;   RETURN digitRootSum(newSum)



END FUNCTION











