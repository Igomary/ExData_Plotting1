d <-read.table("./household_power_consumption.txt", header = TRUE, sep = ";", na.strings = "?")
data <- subset(d, d$Date == "1/2/2007" | d$Date == "2/2/2007")
rm(d)

data$unitedtime = strptime(paste(data$Date, data$Time), "%d/%m/%Y %H:%M:%S")

png(filename = "plot3.png", width = 480, height = 480)

plot(data$unitedtime, data$Sub_metering_1, type = "l", xlab = "", ylab = "Energy sub metering")
lines(data$unitedtime, data$Sub_metering_2, col="red")
lines(data$unitedtime, data$Sub_metering_3, col="blue")
legend("topright", legend = c("Sub_metering_1", "Sub_metering_2", "Sub_metering_3"), lty= 1, col=c("black", "red", "blue"))
 
dev.off()