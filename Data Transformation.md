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

**Merge Data Frames**
**merge two data frames by multiple variables** <br />
**Inner Join** <br />
df1 <- merge(dfA, dfB,by = c("Col1","Col2"))
df1 <- inner_join(x, y, by = NULL, copy = FALSE, ...)

**Outer join** <br /> 
merge(x = df1, y = df2, by = "CustomerId", all = TRUE)

**Left outer** <br />
merge(x = df1, y = df2, by = "CustomerId", all.x = TRUE)
left_join(x, y, by = NULL, copy = FALSE, ...)

**Right outer** <br />
merge(x = df1, y = df2, by = "CustomerId", all.y = TRUE)
right_join(x, y, by = NULL, copy = FALSE, ...)

**Cross join** <br />
merge(x = df1, y = df2, by = NULL)

# sort data frame
**sort by a column**
df1 <- df[order(col1),]

**sort by multiple columns** 
df1 <- df[order(col1, col2),]

**sort by col1 (ascending) and col2 (descending)**
df1 <- df[order(col1, -col2),]

**Aggregating Data** <br />
aggdata <- aggregate(df, by=list(Col1, Col2), FUN=mean, na.rm=TRUE)
**or** <br \>
ddply(dt,~group,summarise,mean=mean(col1),sd=sd(col1))

# Reshaping
library(reshape)
md <- melt(mydata, id=(c("Col1", "Col2")))

# Data Type Conversion
**Check Data Type**
is.numeric()
is.character()
is.vector()
is.matrix()
is.data.frame()

**Change Data Type**
as.numeric()
as.character()
as.vector()
as.matrix()
as.data.frame()



