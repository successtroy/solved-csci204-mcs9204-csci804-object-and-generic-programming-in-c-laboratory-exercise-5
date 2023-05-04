Download Link: https://assignmentchef.com/product/solved-csci204-mcs9204-csci804-object-and-generic-programming-in-c-laboratory-exercise-5
<br>
<strong>Task: Class inheritance (1.0) </strong>




Consider the following diagram.

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/08/508.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/08/508.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>

Define the classes include insertion operators (&lt;&lt;) for each of them shown in the diagram above in a file <strong>Bank.h</strong> and implement the functions in a file <strong>Bank.cpp</strong>. Implement main() and other functions in a file <strong>taskMain.cpp</strong>, create instances of accounts for customers of follows:

<ul>

 <li>Alice has a saving account, BSB# is 123456, account# is 12345678, address is 1 Northfields Avenue, Wollongong, phone# is 1234567, and balance is $1000, saving card number 1234567890123456.</li>

 <li>Bob has a credit card account, BSB# is 123123, Account# is 12341234, address is 20 Moore Street, North Wollongong, Phone# is 12341234, balance is $1000 debt, credit card# is 0987654321123456, limitation $2000, due by 15 April 2016.</li>

</ul>

To make it simple, assume it is the end of the month, every month has 30 days, no matter it is February or March, every year has 360 days. The member function <strong>interest()</strong> computes interests for the above accounts according to the following algorithms, and change the balances of those accounts. 0.5 cents or over shall be round up to 1 cent.

Assume it is end of the month.

<ul>

 <li>Interest rate for a saving account is 0.3% per year. Add the interest to the balance of saving account every month. Use following expression to compute interest for a saving account (A month has 30 days):</li>

</ul>

interest-rate-per-day = 0.2% / 360, interest = balance * interest-rate-per-day * 30.

<ul>

 <li>If the credit card over due days less than or equals to 15 days, interest rate is 12.5% per year, 18% per year for over due more than 15 days. Add interest to the account. Use the following expressions to compute the penalty interest for a credit card account:</li>

</ul>

There are 15 days expired from 15/04/2016 to the end of the month. The interest rate is 12.5% per year.

interest-rate-per-day = 12.5% / 360, interest = balance * interest-rate-per-day * 15.




<strong>Testing: </strong>




Compile the files by g++ –o interest taskMain.cpp Bank.cpp




And execute

./interest




The output details are following:




BSB#: 123456, Account#: 12345678, Alice, Saving, Card#: 1234567890123456,

Balance: $1000.25 CR, Interest paid: $0.25

BSB#: 123123, Account#:12341234, Bob, Credit, Card#: 0987654321123456, Balance: $1003.47 DR, Interest charges: $3.47







<strong>Note: No input required for testing. </strong>

<strong> </strong>


