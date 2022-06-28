what is the difference between Props and State?

Props:-

Props are read-only.
Props are immutable.
Props allow you to pass data from one component to other components as an argument.
Props can be accessed by the child component.
Props are used to communicate between components.
Stateless component can have Props.

state:-

State changes can be asynchronous.
State is mutable.
State holds information about the components.
State cannot be accessed by child components.
States can be used for rendering dynamic changes with the component.
Stateless components cannot have State.

Explain the useState API?
useState is a Hook (function) that allows you to have state variables in functional components. You pass the initial state to this function and it returns a variable with the current state value (not necessarily the initial state) and another function to update this value.

Map Function :-
The map() method in JavaScript creates an array by calling a specific function on each element present in the parent array.
Filter Function :-
The filter() method creates a new array filled with elements that pass a test provided by a function. 
Reduce Function :-
The reduce() method executes a user-supplied "reducer" callback function on each element of the array, in order, passing in the return value from the calculation on the preceding element.


Map Function :-
Array.prototype.mymap = function(callback) {
    const resultArray = [];
    for (let index = 0; index < this.length; index++) {
        resultArray.push(callback(this[index], index, this));
    }
    return resultArray;
}

Filter Function :-
Array.prototype.myFilter = function(callback) {
    const filterArr = [];
    for(let index = 0; index<this.length; index++) {
        if(!!callback(this[index], index, this)) {
            filterArr.push(this[index]);
        }
    }
    return filterArr;
}

Reduce Function :-
Array.prototype.myReduce = function(callback, accumulator) {
    if(this.length < 1) {
        throw new Error("Array is Empty")
    }

    if(!accumulator) {
        if(typeof this[0] === "string") {
            accumulator = '';
        } else if(typeof this[0] === "number") {
            accumulator = 0;
        }
    }

    for(let index=0; index < this.length; index++) {
        accumulator = callback(accumulator, this[index]);
    }
    return accumulator;
}