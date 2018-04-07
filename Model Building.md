# Time Series - ARIMA Function


data = file("stdin")<br />
startDate <- data[1]<br />
endDate <- data[2]<br />

n <- as.numeric(as.character(data[3]))<br />

knownTimestamps <- data[4:(n+3)]<br />
humidity <- as.numeric(as.character(data[(n+5):(2*n+4)]))<br />
pred_per <- as.numeric(as.character(data[(2*n+5)]))<br />
timestamps <- data[(2*n+6):length(data)]<br />

predictMissingHumidity <- function(startDate, endDate, knownTimeStamps, humidity, timestamps)<br />
  {<br />
  m = arima(humidity, order = c(2,1,2), seasonal = list(order = c(0, 1, 1), period = 8), include.mean = F)<br />
  Opt = predict(m, n.ahead = length(timestamps), se.fit = F)<br />
  cat(paste0(as.numeric(Opt),collapse="\n"))<br />
  }<br />
predictMissingHumidity(startDate, endDate, knownTimeStamps, humidity, timestamps)


# Linear Regression
fit <- lm(y ~ x1 + x2 + x3, data=mydata) <br />
predict(lm(y ~ x), new, se.fit = TRUE)

# Logistic Regression 
model <- glm(Survived ~.,family=binomial(link='logit'),data=train) <br />
predict(model,newdata=subset(test,select=c(2,3,4,5,6,7,8)),type='response')
