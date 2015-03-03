# diamond-box-plots

library(gridExtra)

p1 <- qplot(x = color, y = carat, data=d, geom = 'boxplot')
  coord_cartesian()

p2 = qplot(x = color, y = price, data=d, binwidth = 1, geom = 'boxplot')
  
p3 = qplot(x = color, y = price/carat, data=d, binwidth = 1, geom = 'boxplot')+
  coord_cartesian(ylim = c(0, 10000))


grid.arrange(p1,p2,p3)
      
