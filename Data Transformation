## Creating empty Data Frame

colClasses = c("Date", "character", "character")
col.names = c("Date", "File", "User")
df <- read.table(text = "", colClasses = colClasses, col.names = col.names)

## Filtering data frame
newdata <- subset(mydata, age >= 20 | age < 10, select=c(ID, Weight))
newdata <- subset(mydata, sex=="m" & age > 25, select=weight:income)

**first n observations**
df1 <- df[1:n,]

**based on variable values**
df1 <- df[ which(df$gender=='F' & df$age > 65), ]

**# or**
df1 <- df[ which(gender=='F' | age > 65),]
