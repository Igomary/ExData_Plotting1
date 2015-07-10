d <-read.table("./household_power_consumption.txt", header = TRUE, sep = ";", na.strings = "?")
data <- subset(d, d$Date == "1/2/2007" | d$Date == "2/2/2007")
rm(d)

data$unitedtime = strptime(paste(data$Date, data$Time), "%d/%m/%Y %H:%M:%S")

png(filename = "plot2.png", width = 480, height = 480)
plot(data$unitedtime, data$Global_active_power, type = "l", ylab = "Global Active Power (kilowatts)", xlab="")
dev.off()