# PRODIGY_DS_02
```
titanic_data <- read_csv("C:/Users/geeta/Downloads/train.csv")
# Check the structure of the data
str(titanic_data)

# Check summary statistics
summary(titanic_data)

# Check for missing values
colSums(is.na(titanic_data))
titanic_data <- titanic_data[complete.cases(titanic_data), ]

# Convert variables to factors
titanic_data$Sex <- as.factor(titanic_data$Sex)
titanic_data$Embarked <- as.factor(titanic_data$Embarked)
titanic_data <- subset(titanic_data, select = -c(PassengerId, Name))
write.csv(titanic_data, "cleaned_train.csv", row.names = FALSE)


summary(titanic_data)
correlation_matrix <- cor(titanic_data[, c("Age", "Fare", "Survived")])
print(correlation_matrix)

ggplot(titanic_data, aes(x = Age, y = Fare, color = factor(Survived))) +
  geom_point() +
  labs(title = "Scatter Plot of Age vs Fare (Colored by Survival)",
       x = "Age",
       y = "Fare",
       color = "Survived")
```
![d37c12e9-58ac-4800-941b-162765ad5621](https://github.com/geetashree10/PRODIGY_DS_02/assets/158750505/1c5fbdcb-8605-47a0-b760-79f81ca7c06f)

