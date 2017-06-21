# cats
Doing a R package with devtools
I used this example from hilaryparker.com

## Step 0: Packages you will need
The packages you will need to create a package are devtools and roxygen2. 

## Step 1: Create your package directory
 You are going to create a directory with the bare minimum 
folders of R packages.

create("cats")

## Step 2: Add functions
cat_function <- function(love=TRUE){
  if(love==TRUE){
    print("I love cats!")
  }
  else {
    print("I am not a cool person.")
  }
}

## Step 3: Add documentation
Ctrl + Alt + Shift + R
#' A Cat Function
#'
#'This function allows you to express your love of cats.
#' @param love Do you love cats? Defaults to TRUE.
#' @keywords cats
#' @return
#' @export
#'
#' @examples
#' cat_function()
#' 
cat_function <- function(love=TRUE){
  if(love==TRUE){
    print("I love cats!")
  }
  else {
    print("I am not a cool person.")
  }
}

## Step 4: Process your documentation

setwd("./cats")
document()



## Step 5
Step 5: Install!
Now it is as simple as installing the package! 
You need to run this from the parent working directory that contains the cats folder.
setwd("./cats")
document()


setwd("..")
install("cats")

