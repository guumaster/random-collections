# Functional programming introduction

## Traversing

1. loop an array
1. use foreach

## Projecting arrays

1. create a projection with forEach ([a] => [a])
1. implement map (accepts a projection)
1. repeat previous with map and projection
    (notice: map allows us to specify what projection we want to apply to an array, but hides how the operation is carried out.)

## Filtering arrays

1. collect some items with forEach
   (notice: there is a pattern, traverse, test, collect)
1. implement filter
1. chain filter and map to transform and collect 
    (notice: expresive power)

## Querying trees

1. flatten a two level tree with forEach
1. implement concatAll()
1. use map() and concatAll() to project and flatten a tree
1. traverse a three level tree with map/filter/concatAll (with no index access)
    (notice: map() and concatAll() regularly go together)
1. implement concatMap()
1. repeat previous with concatMap()
    (notice: usually you'll see concatMap + concatMap + filter + map)

## Reducing arrays

1. use forEach() to find the largest value on an array
1. implement reduce()
1. return largest value with reduce()
1. reduce with an initial value
1. use reduce() instead of filter() to get the smallest value

## Zipping arrays

1. combine two arrays by index
1. implement zip()
1. repeat previous with zip()



