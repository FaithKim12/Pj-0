# Pj-0
#rbasics
#plot function
head(iris)
plot(iris)
plot(iris$Petal.Length, iris$Petal.Width)
plot(iris$Species)
plot(iris$Petal.Length, iris$Petal.Width, #plots with scatter plots
     col = "#cc0000", #hex code for datalab.cc red
     pch = 19, #point character.Use solid circles for points
     main = "Iris: Petal Length vs. Petal Width",
     xlab = "Petal Length", 
     ylab = "Petal Width")

#plot formulas with plot()
plot(cos, 0, 2*pi)
plot(exp, 1,5)
plot(dnorm, -3, 3)

#plot formulas with scatter plots
plot(dnorm, -3, 3,
     col = "#cc0000", 
     lwd = 5, 
     main = "Standard normal distribution",
     xlab = "z-scores",
     ylab = "Density")

#barcharts
library(datasets)
?mtcars
head(mtcars)
barplot(mtcars$cyl) #doesn't work.instead we use table with frequencies for each category.
#Need a table with frequencies for each category
cylinders <- table(mtcars$cyl)  #create table (mtcars$cyl) which feeds to the data cylinders
barplot(cylinders)   #barchart
plot(cylinders)

#histograms
library(datasets)
?iris
head(iris)   #load data
hist(iris$Sepal.Length)
hist(iris$Sepal.Width)
hist(iris$Petal.Length)
hist(iris$Petal.Width) 

#histograms by groups
#put graphs in 3 rows and 1 column
#histogram for each species using options
hist(iris$Petal.Width [iris$Species == "setosa"], #variableiris$Petal.Width and row selection irissepecies
     xlim = c(0, 3),  #x limit scale
     breaks = 9,  #bars for the histogram
     main = "Petal Width for Setosa", #heading
     xlab = "",  #no x label
     col = "red")
hist(iris$Petal.Width [iris$Species == "versicolor"], 
     xlim = c(0, 3), 
     breaks = 9, 
     main = "Petal Width for Versicolor", 
     xlab = "", 
     col = "purple")
hist(iris$Petal.Width [iris$Species == "virginica"],
     xlim = c(0,3), 
     breaks = 9, 
     main = "Petal Width for Virginica", 
     xlab = "", 
     col = "blue")

#Scatterplots
library(datasets)
?mtcars
head(mtcars)
