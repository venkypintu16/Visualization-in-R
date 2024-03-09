#R code to visualize data using 3 different plotting techniques (scatter plot, lattice plot, ggplot).

Y = data("mtcars")

#Using normal plot function.

plot(mtcars$mpg, mtcars$hp,
         xlab = "MPG",
         ylab = "HP",
         main = "Scatter Plot of MGP vs HP (mtcars data)")

# Using lattice plot.

library(lattice)
xyplot(hp ~ mpg, data = mtcars, main = "Scatter Plot of MPG vs HP", xlab = "MPG", ylab = "HP")


# Using ggplot2.

library(ggplot2)
ggplot(mtcars, aes(x = mpg, y = hp)) +
  geom_point() +
  labs(x = "MPG", y = "HP", title = "Scatter Plot of MPG vs HP")

###########################################################################################################################################################################################

Explanation of the above R code is below: 

1. Y = data("mtcars"): This line is attempting to load the mtcars dataset into a variable called Y.
   
2. X = plot(mtcars$mpg, mtcars$hp, xlab = "MPG", ylab = "HP", main = "Scatter Plot of MGP vs HP (mtcars data)"): This line is creating a scatter plot using the plot function, with mpg on the x-axis and hp on the y-axis. It also sets the x-axis label to "MPG", the y-axis label to "HP", and the main title of the plot to "Scatter Plot of MGP vs HP (mtcars data)".

3. xyplot(hp ~ mpg, data = mtcars, main = "Scatter Plot of MPG vs HP", xlab = "MPG", ylab = "HP"): This line creates a lattice plot using the xyplot function from the lattice package. It plots hp against mpg from the mtcars dataset. The main, xlab, and ylab arguments set the main title, x-axis label, and y-axis label, respectively.

4. ggplot(mtcars, aes(x = mpg, y = hp)) + geom_point() + labs(x = "MPG", y = "HP", title = "Scatter Plot of MPG vs HP"): This line creates a ggplot using the ggplot2 package. It specifies the mtcars dataset and defines the aesthetic mappings using the aes function, with mpg mapped to the x-axis and hp mapped to the y-axis. The geom_point function adds points to the plot. The labs function sets the x-axis label to "MPG", the y-axis label to "HP", and the plot title to "Scatter Plot of MPG vs HP".
