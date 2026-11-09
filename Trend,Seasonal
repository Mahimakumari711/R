# Syntax: ts(data, start, end, frequency )
#Example 1: Monthly data starting in january 2023
sales_data <- c(120, 135, 150, 145, 160, 175, 190, 185, 200, 210, 225, 240)
monthly_ts <- ts(sales_data, start = c(2023, 1), frequency = 12)
print(monthly_ts)

plot(monthly_ts, main = "Monthly Sales", ylab = "Sales", xlab = "Year")

##############################################################

url <- "https://raw.githubusercontent.com/jbrownlee/Datasets/master/airline-passengers.csv"

df <- read.csv(url)

#Inspect the first few rows 
head(df)

#Convert the 'Passangers' column into a monthly time series starting Jan 1949
passengers_ts <- ts(df$Passengers, start = c(1949, 1), frequuency = 12 ) 
plot(passenger_ts)

#1 Load the built-in AirPassengers dataset
data("AirPassengers")

#2 Decompose using a multiplicative model 
# (Required because the seasonal swing increases alongside the trend)
decomposed_ap <- decompose(AirPassengers, type = "multiplicative")

#3 Plot all components together (Observed, Trend, Seasonal, Random)
plot(decomposed_ap)

#4 Access individual numerical components
trend_component <- decomposed_ap$trend
seasonal_component <- decomposed_ap$seasonal
random_component <- decomposed_ap$random

#View the 12 monthly seasonal indices (valus > 1 mean above-average months)
round(decomposed_ap$figure, 3)
