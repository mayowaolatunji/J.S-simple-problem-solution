# LOGICAL OPERATORS

## Logical OR 

There are cases in code where we want to say "this condition" or "this other condition". If either of the conditions are true, let's do something!

It would be quite ugly to write this with if statements every time:

```
if(car) {
    driveToAirport();
}
else if(motorcycle) {
    driveToAirport();
}
else if(truck) {
    driveToAirport();
}
```

If we needed to change the driveToAirport function, we would have to change it in 3 places. It is beneficial to adhere to the principle of code DRYness, which stands for "Don't Repeat Yourself." Whenever feasible, it is advisable to minimize code redundancy and strive for efficient reuse.




