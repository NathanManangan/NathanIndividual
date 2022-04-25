{% include navigation.html %}

# Create Task

{% include createtask.html %}

## Nathan Written Response
My plans for the written responses are encapsulated by my Initial create task project overview, and explaining how the program implements into our project's games page, the procedures the user input goes through to return the output, and explains how the numbers they give play a role in the output.

### 3a
- In our program, we plan on taking an **INPUT** from the **USER**. It will ask for 5 numbers, and then once the numbers are given, we will display **(MIN) (MAX) (AVG)**. For the video, we will do 1 run for each output of the program after a user input. This will be showing the inputs going into a list, then showing iteration for going through the lists, selection to display if a number is the lowest or highest then sequencing to check each number. The input is the user giving numbers, and the output will essentially show which number was the highest number, which one was the lowest number, and what the average for all of those numbers were.

### 3b
- `
var list = []; // Defines list
`
The name of the list is list

The data in the list has the numbers that the user inputs and is used to find values

Without the list the code wouldn't display any of the numbers the user input, as well as not be as user friendly.

### 3c
- `
function addnumber(){
    console.log("")

    var numbers = parseInt(prompt("What number would you like to put in the list?")) // Prompts the user for an input

    console.log("")

    list.push(numbers) // Pushes the user input into the list

    if (value1 === 1){ // makes the first value equal to the min and max so they aren't undefined
      min = list[0]
      max = list[0]
      value1 = 0
    }
    
    for(var i = 0; i < list.length; i++) { // Recurs through each number in the list
        if(list[i] < min) min = list[i]; // Determines if number is lower than current minimum
        if(list[i] > max) max = list[i]; // Determines if number is higher than current maximum
        average += list[i]; // adds the number to the average count
    }

    average /= list.length; // Calculates average
    button() // Redisplays the list
}
`
The main function that does the the algorithms is named addnumber(). Sequencing is shown through every input, which is gone through the list to check if it's lower or greater than the previous numbers. Selection is then performed if it is less or greater than to make it the new min/max. Then finally, the iteration is performed with every single "click" event. With every click of submitting a number the process is repeated again showing iteration.

`
function button(){ // displays a menu and a prompt to choose

    console.log("1. Add a number");
    
    console.log("2. See the mininum value");
    
    console.log("3. See the maximum value");
    
    console.log("4. See the average");
    
    console.log("5. Stop");
    
    var funclist = parseInt(prompt("What option would you like to choose?"));

    if (funclist === 1){ // calls function for adding a number
        addnumber()
    }
    
    else if(funclist === 2){ // calls minimum funciton
        minimum()
    }
    
    else if(funclist === 3){ // calls maximum function
        maximum()
    }
    
    else if(funclist === 4){ // calls average function
        avg()
    }
    
}
`
This is the function, which is a menu, where the functions can be called. It is called at the very start of the program, and also called whenever 1-4 is responded. Once this happens the javascript function is run. Essentially, our algorithm takes each input from a user and adds it to a list, and also added to a variable called average. List is the numbers in the list and average is the sum of the numbers in the list. It also then makes the min and max temporarily the first input number. After more numbers are added, the each get compared to the first number, and if they the highest or lowest value out of the previous numbers, they are set to min or max. After all that happens, finally average is calculated by taking sum/count.

### 3d
- 
`

if (funclist === 1){ // calls function for adding a number

        addnumber()
        
    }
    
    else if(funclist === 2){ // calls minimum function
    
        minimum()
        
    }
    
    else if(funclist === 3){ // calls maximum function
    
        maximum()
        
    }
    
    else if(funclist === 4){ // calls average function
    
        avg()
        
    }
    
`
In the these calls, the functions are calling for the outputs from addnumber(), or calling for the function itself, and displaying it in the terminal. This is testing for the "min max avg" values that were calculated in addnumber(). This will then display them once inputted number 1-4.
