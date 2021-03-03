# EGAP Learning Days Book Repository

```
Caramba y zamba la cosa
que vivan los experimentos! 
-from 'Me Gustan Los Estudiantes' by Violeta Parra
```

![Build and Deploy](https://github.com/egap/theory_and_practice_of_field_experiments/workflows/Build%20and%20Deploy/badge.svg)

This is the repository for the online EGAP Learning Days book which includes a materials to help researchers learn how to design and analyze data from randomized field experiments.

## Contributing

We would love for anyone to improve this work. Please feel free to post ideas in the [Github Issues](https://github.com/egap/theory_and_practice_of_field_experiments/issues). Also feel free to [Fork](https://guides.github.com/activities/forking/) and modify and make a pull request. If you have a message to send, the best way is to use the [Issues](https://github.com/egap/theory_and_practice_of_field_experiments/issues). You can also send an email to <admin@egap.org>.

If you want to work on the slides, you should go to [the Learning Days Resources repository](https://github.com/egap/learningdays-resources/).

## Tools

Here we describe how we develop this book and provide some guidance for people who want to collaborate with us in writing etc.

### Markdown

We write the text for the modules in Markdown format. The slides are in R+Markdown format.

If you want help making tables, you can try the following online tool <https://thisdavej.com/copy-table-in-excel-and-paste-as-a-markdown-table/>.

### R packages

We are also using the [renv](https://rstudio.github.io/renv/index.html) package to keep our libraries portable. So, before you start collaborating you will need to do the following:

```
install.packages("renv")
```

After you clone this repository you will want to do the following from within the `Book` working directory (for example opening the `learningday-book.Rproj` file in RStudio) to install all of the packages we use in this book do:

```
renv::restore()
```

Then you will need to restart R so that it begins work in the new R environment that we have created.

That command will read the `renv.lock` file 

From then on, if you start R from within the book directory, you should be only using R packages installed locally and they need not clutter your whole system just to work on this book project. For example you should see something like this at the top of your R session console.

```
* Project '~/Documents/PROJECTS/theory_and_practice_of_field_experiments/Book' loaded. [renv 0.11.0]
```

We use the `bookdown` package. So you will need to `install.packages("bookdown")` before loading the `theory_and_practice_of_field_experiments.Rproj` file in RStudio.

###  To Deploy the Book Online

The book will automatically be built and deployed online for each push to the repository using github actions.

#### To build by hand

Before using github actions we used the `_build.sh`  bash shell script for building locally OR we used the "Build Book" function in RStudio. Either way allows you to look at `_book/index.html` or the pdf or epub versions of the book on your own computer.
  
## License

We are happy for others to use this work as long as EGAP is attributed. See the following license for the precise terms.


<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
