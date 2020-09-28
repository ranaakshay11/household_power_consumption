data <- read.table("household_power_consumption.txt", header= TRUE, sep=";", stringsAsFactors=FALSE, dec=".")
summary(data)
##      Date               Time           Global_active_power
##  Length:2075259     Length:2075259     Length:2075259     
##  Class :character   Class :character   Class :character   
##  Mode  :character   Mode  :character   Mode  :character   
##                                                           
##                                                           
##                                                           
##                                                           
##  Global_reactive_power   Voltage          Global_intensity  
##  Length:2075259        Length:2075259     Length:2075259    
##  Class :character      Class :character   Class :character  
##  Mode  :character      Mode  :character   Mode  :character  
##                                                             
##                                                             
##                                                             
##                                                             
##  Sub_metering_1     Sub_metering_2     Sub_metering_3  
##  Length:2075259     Length:2075259     Min.   : 0.000  
##  Class :character   Class :character   1st Qu.: 0.000  
##  Mode  :character   Mode  :character   Median : 1.000  
##                                        Mean   : 6.458  
##                                        3rd Qu.:17.000  
##                                        Max.   :31.000  
##                                        NA's   :25979
subsetdata <- data$Date %in% c("1/2/2007","2/2/2007"),]
globalActivePower <- as.numeric(subsetdata$Global_active_power)
globalReactivePower <- as.numeric(subsetdata$Global_reactive_power)
voltage <- as.numeric(subsetdata$Voltage)
subMetering1 <- as.numeric(subsetdata$Sub_metering_1)
subMetering2 <- as.numeric(subsetdata$Sub_metering_2)
subMetering3 <- as.numeric(subsetdata$Sub_metering_3)
hist(globalActivePower, col="red", main="Global Active Power", xlab="Global Active Power (kilowatts)")
