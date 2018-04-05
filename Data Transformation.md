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
total <- merge(data frameA,data frameB,by=c("ID","Country"))

**Outer join** <br /> 
merge(x = df1, y = df2, by = "CustomerId", all = TRUE)

**Left outer** <br />
merge(x = df1, y = df2, by = "CustomerId", all.x = TRUE)

**Right outer** <br />
merge(x = df1, y = df2, by = "CustomerId", all.y = TRUE)

**Cross join** <br />
merge(x = df1, y = df2, by = NULL)

