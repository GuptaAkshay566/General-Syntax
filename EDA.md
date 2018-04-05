# Sampling <br />

**Random Sampling** <br />
df1 <- df[sample(1:nrow(df), 50, replace=FALSE),]
df1 <- sample(df, size, replace = FALSE, prob = NULL)


# Descriptive Analysis <br />
**mean,median,25th and 75th quartiles,min,max** <br />
summary(mydata)

**mean**  <br />
m1 <- mean(as.numeric(data[2, ]))

**median**  <br />
m2 <- median(as.numeric(data[2, ]))

**mode**  <br />
Mode <- function(x) {  <br />
  ux <- unique(x)  <br />
  ux[which.max(tabulate(match(x, ux)))]  <br />
}  <br />
m3 <- Mode(as.numeric(sort(data[2, ])))

**standard deviation**  <br />
m4 <- round(sqrt(sd((data[2, ]))^2*(n-1)/n), digits = 1)

**Confidence interval**  <br />
interim <- m4/sqrt(n)
Lower <- round(m1 - 1.96*interim, digits = 1)
Upper <- round(m1 + 1.96*interim, digits = 1)

**Quantile**
quantile(x, probs = seq(0, 1, 0.25), na.rm = FALSE) <br />

**Correlation**
cor(df) <br \>

# Charts and Visualization

**Box Plot**

**Histogram**

**Scatter Plot**
