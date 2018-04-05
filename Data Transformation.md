## Creating empty Data Frame <br />

colClasses = c("Date", "character", "character")
col.names = c("Date", "File", "User")
df <- read.table(text = "", colClasses = colClasses, col.names = col.names)

## Filtering data frame <br />
newdata <- subset(mydata, age >= 20 | age < 10, select=c(ID, Weight))
newdata <- subset(mydata, sex=="m" & age > 25, select=weight:income)

**first n observations** <br />
df1 <- df[1:n,]

**based on variable values - and** <br />
df1 <- df[ which(df$gender=='F' & df$age > 65), ]

**or** <br />
df1 <- df[ which(gender=='F' | age > 65),]
