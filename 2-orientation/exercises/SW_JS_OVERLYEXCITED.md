# Overly Excited

## Requirements

For this exercise, you need to create a single JavaScript function named `addExcitement` that will use `console.log()` to print out a sentence to the browser console.

1. If you haven't done so yet, create the `workspace/exercises/overly-excited` directory structure in your home directory. Open your terminal and enter in the following command.

    ```
    mkdir -p ~/workspace/exercises/overly-excited
    ```

1. Now that you have created the directory, you want to change to that directory so that you can add files to it.

    ```
    cd ~/workspace/exercises/overly-excited
    ```

1. Create an `index.html` file with the [touch](http://www.linfo.org/touch.html) command.
1. Create an `overly-excited.js` file with the touch command.
1. Copy the following code and paste it into the `index.html` file. Notice that the `overly-excited.js` file is properly linked so that when you load this HTML file in a web browser, the logic in that file will be executed.

    ```
    <!DOCTYPE html>
    <html>
    <head>
        <title>Overly Excited</title>
    </head>
    <body>

        <script src="overly-excited.js"></script>
    </body>
    </html>
    ```

1. Open the `index.html` file in your web browser.
1. At this point, you will simply see a blank web page because you have no content in the HTML file. Open your developer tools using the *Option+Command+I* keyboard shortcut.
1. At the top of the developer tools panel, you will see the word *Console*. Click on that word. The `console.log()` statement will output any message into this panel in your developer tools. You can try it out immediately by clicking in the Console panel, and typing `console.log("Hello, world!")`, and then pressing your return key.

## Stacking Words

Create an `addExcitement` function that should `console.log()` rows of words. It should take an array containing the words of a sentence and output them in the developer console.

> **Example output:**  
>  
> The   
> The walrus    
> The walrus danced      
> The walrus danced through     
> The walrus danced through the     
> The walrus danced through the trees         
> The walrus danced through the trees in            
> The walrus danced through the trees in the        
> The walrus danced through the trees in the light  
> The walrus danced through the trees in the light of   
> The walrus danced through the trees in the light of the    
> The walrus danced through the trees in the light of the moon  
> ...

Paste the following code into overly-excited.js

```js
// Create an array that contains the words in the sentence
var sentence = [];

// The addExcitement function should accept the array as the sole argument
function addExcitement (theWordArray) {
    /*
      Write a `for` loop that iterates over the array argument and
      outputs the words.
     */
}

// Invoke the function and pass in the array
addExcitement(sentence)
```

## Adding Conditions to the Loop

Then add logic to `addExcitement` that places an exclamation point (!) after every third word. This will require you to do some basic math in JavaScript, and use an `if` statement.

Your job is to read the following English statement and write the equivalent in JavaSript code to make it work.

> If the current value of the [counter variable](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for) can be evenly divided by 3 - using the JavaScript [remainder](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators#Remainder) operator - then add a single exclamation point (!) to the output.

> **Example output:**  
>  
> The               
> The walrus            
> The walrus danced!                
> The walrus danced! through            
> The walrus danced! through the            
> The walrus danced! through the trees!         
> The walrus danced! through the trees! in          
> The walrus danced! through the trees! in the          
> The walrus danced! through the trees! in the light!           
> The walrus danced! through the trees! in the light! of            
> The walrus danced! through the trees! in the light! of the        
> The walrus danced! through the trees! in the light! of the moon!      
> ...


## Challenge

Add logic in the `addExcitement` function to the increase the number of exclamation points after every third word. The number of exclamation points (!) will be determined by how many times the counter variable can be divided by 3. 


> **Example output:**  
>  
> The                   
> The walrus            
> The walrus danced!            
> The walrus danced! through            
> The walrus danced! through the            
> The walrus danced! through the trees!!            
> The walrus danced! through the trees!! in         
> The walrus danced! through the trees!! in the             
> The walrus danced! through the trees!! in the light!!!            
> The walrus danced! through the trees!! in the light!!! of             
> The walrus danced! through the trees!! in the light!!! of the             
> The walrus danced! through the trees!! in the light!!! of the moon!!!!            
> ...