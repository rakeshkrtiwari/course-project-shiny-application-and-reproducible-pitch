---
title       : Shiny Application and Reproducible Pitch
subtitle    : 
author      : Rakesh Kumar Tiwari
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

##Course Project

* This is the final presentation for the Course Project
* The course is focused on Developing Data Products
* The main objective of the project is to write a Shiny application

---
#Shiny Application

* In this project a Shiny Application was written
* This is small game application which takes a number between 1 to 100 from user
* Compares it with a random number generated in server side 
* Give the outcome to the users.
* Users can try this any number of time

---

# Following code compare the number and reture outcome

```r
numberGuessed <- function(guess, number) {
    returnValue <- "Nothing entered yet."
    if (guess > 100) {
        print(guess)
        #print(class(guess))
        #print(class(100))
        returnValue <- 'Above 100.\nPlease make a selection between 1 and 100.'
    }
    else if (guess < 1) {
        #print(guess)
        returnValue <- 'Below 1.\nPlease make a selection between 1 and 100.' 
    }
    else if (guess > number) {
        returnValue <- 'Higher than the number.'
    }
    else if (guess < number) {
        returnValue <- 'Lower than the number.'
    }
    else if (guess == number) {
        returnValue <- 'Correct!'
    }
    returnValue
}
```

---

#The application 
* Application can be found in following link
+https://rakeshkrtiwari.shinyapps.io/Shiny_Application/
* Source Code is hosted in GitHub in following Repository
+https://github.com/rakeshkrtiwari/course-project-shiny-application-and-reproducible-pitch.git

