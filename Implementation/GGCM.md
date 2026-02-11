Greyson Dobis
Grayson Manis
Camden Brunsma
Mohamed Khalil

Requirments:
- User must input 2 integers
- Program must add the two integers from the users input.
- Program must add the last digit to the remaining digits.
- Program must repeat the previous requirment until the final number is one digit long.

Design:
<img width="724" height="483" alt="image" src="https://github.com/user-attachments/assets/8240f004-3db6-41e8-acbc-d031cd830b49" />

Implementation:
Pseudo Code
1. Prompt user for 2 integer inputs.
2. Check if they provided bad input and make them retry if so. (A bad input is if the input types do not equal integer; list other reasons as found here)
3. Separate least significant digit (LSD) from the number.
4. If no greatest significant digit (GDS) is found from the separation, default it to 0.
5. Add the LSD and GSDs together.
6. Check if the new number is 1 digit. If so, end the loop, display the number, and restart the program entirely. If not, repeat from step 3 until 1 digit found.

Test:
- Run a fuzzer to test many different types of inputs.
