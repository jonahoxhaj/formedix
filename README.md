# java app

The libraries used for this application are:

1. 
		<dependency>
			<groupId>com.opencsv</groupId>
			<artifactId>opencsv</artifactId>
			<version>5.3</version>
		</dependency>
		
		
Used to read the file since it is a csv file.

2. 
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>

Used to make the application a web app.

3. 
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency> 

Used in order to build and run tests


***********Run the application*************

****We can retrieve all the data from the browser:
http://localhost:8080/api/formedix/readAllData

****Returns the  reference rate data for a given Date for all available Currencies
http://localhost:8080/api/formedix/ratePerGivenDate?data=2022-08-19

****Returns the Amount given converted from the first to the second Currency as
    it would have been on that Date (assuming zero fees).
http://localhost:8080/api/formedix/amountExchangedPerGivenDate?data=2022-08-19&sourceCurrency=GBP&targetCurrency=USD&amount=8.448179828923811	

http://localhost:8080/api/formedix/amountExchangedPerGivenDate?data=2022-08-19&sourceCurrency=USD&targetCurrency=GBP&amount=10



****Return the highest reference exchange rate that the Currency achieved for the period.
http://localhost:8080/api/formedix/highestExchangedRatePerPeriod?startDate=2022-08-10&endDate=2022-08-19&currency=GBP


****Determine and return the average reference exchange rate of that Currency for the period.
http://localhost:8080/api/formedix/averageExchangedRatePerPeriod?startDate=2022-08-10&endDate=2022-08-19&currency=GBP
