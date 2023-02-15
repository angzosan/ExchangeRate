# ExchangeRate
The exchange rate is a single-bit error detection method, in which a ninth bit, the exchange rate bit, is added to the end of each row of 8 bits.The value of the extra bit is used to detect odd errors within the group of 8 bits.This is divided into odd and even (here we consider the case of even). The procedure followed is as follows: We count the number of bits that have a value of "1". If we are in the first case and the number of "1" is odd then we accept the message otherwise we request retransmission. Similarly in the other case for an even number of units."

1.1
The first part being responsible for even parity, checks whether the number of units is odd or even. If it is odd it adds one unit to the end of the message and if it is even it adds a zero.

1.2
The following code section is responsible for error detection and considers three different cases.
1.There is no error
2.There is one error
3.There are two errors

We notice that in the case of two errors it tells us that it accepts the message this is because by toggling the two bits the "balance" between 0 and 1 is restored and the error is not detected.

1.3 
In this case we follow a 2-dimentional exchange rate, the logic is applied is similar to the one earlier but instead of having one single line,
the bits are divided equally into 4 lines. 

1.4 
Following the same logic we did in 1.2, we notice that the 'network' is able to catch the errors.

NOTE(not in the code):
Are there any error patterns that are not detected in two-dimensional parity, and if so which ones?In the case where there is a double toggle in one column and one row then the algorithm will not be able to detect the error due to the "balance" as mentioned in question 1.2.For a better understanding the following example is given.

![image](https://user-images.githubusercontent.com/118728873/219042725-8e9ba098-b27a-4926-a369-b6a9735c463f.png)
![image](https://user-images.githubusercontent.com/118728873/219042764-b382e7aa-fb71-4db9-96e0-910829d838fa.png)
