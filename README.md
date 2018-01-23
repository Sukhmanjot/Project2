# Project2

Q1. Read file "data.json", and write a recursive function to convert every value of key "quantity" to 23gm, 50gm and 260gm, presently data is given for 100gm.

Descp: 
1. Read the jason file with the help of pandas package.

2. Get the relevent data into the list for further processing(in our case "data" is relevent), we'll get the data as list containing dictionary.

3. Get the data for 100gm.

4. Drive in the loop till you get the key "Quantity" to get the quantity values changed.

5. After getting to the values of "Quantity", call a user define function "Conversion" to convert the values of Quantity, since the data given here is for 100gms so converting it to the said values with logic:
-> data given is for 100gms
-> for 1gm its 1/100
-> for the given values(23gm,50gm,260gm) its 0.23,0.50,2.60 resp.

6. Print the values recursively if format(value for 23gm,value for 50gm,value for 260gm,#######,orignal value i.e for 100gm).

Q3. Write a custom random number generation algo which should be 73% biased to the higher number. Like if I want ‘a random number between 1 to 10’ 100 times then it should give ‘number more than 5’ 73 times and ‘less than 5’ 27 times. You’re not allowed to use any predefined random number generation function nor use of any kind of third party library to generate random number.

Desc:

1. First take the lower limit and upper limit of range from user. Calculate mid value from these two limits to separate the range into two parts upper range and lower range.

2. Then create two list say min_list which will contain values from lower limit to mid value(excluding) and max_list which will contain values from mid value (excluding) to upper limit.

3. Start the while loop1 until the length of max_list becomes 73. In this loop random number is generated using Linear congruential generator(LCG) method in which an equation is used ie [number = (increment + current time * multiplier) % mod] and then 'number' generated from this equation is put into [value = number / mod] (which will give output value between 0 and 1). And this value is put into a formula [lower limit + value * (upper limit - lower limit] to calculate random number in given desired range. Then add final value to max_list.

4. Start the second while loop2 until the length of min list becomes 27. Same procedure is done as above while loop1 Then add final value to min_list.

5. Print both the max_list and min_list.

6. Then print final_list ie concatenated list of max_list and min_list.
