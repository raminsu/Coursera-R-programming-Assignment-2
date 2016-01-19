# Coursera-R-programming-Assignment-2
Programming assignment 2 

rm(list = ls())

makeCacheMatrix <- function(x = matrix()) {
  y <<- solve(x) 
  y
}


cacheSolve <- function(x,... ) {
  if(exists('y')) {
    message("getting cached data since inverse object exists")
    return(y)
  } else { 
    message("calculating inverse since inverse object doesn't exist")
    makeCacheMatrix(x)
}
}

one <- matrix(1:4,2,2)
cacheSolve(one)
