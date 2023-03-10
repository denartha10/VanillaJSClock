# VanillaJSClock
A basic clock app built using Vanilla JS, HTML and CSS

### Things I learned when making the clock app

> 📝
>
> While writing this I realised I was able to make optimisations and clean up the code. I should probably do this in the future.

First and overiew of why I made this. I made this 'app' (isn't exactly an app) with just a single html page which included css and html. I mean there isn't much need to use a framework for something so basic. 

I learned more about javascript loading than you would think and more importantly I got to use arrow functions which I really am starting to like from an aestethic point of view anyway.

##### HTML

- I suppose the first thing is how to load google fonts is actually really easy all it requires is adding the correct links into the head of the HTML file and then afterwards it is as simple as referencing it in the CSS

- This time I made an effort to name good classes for my html. descriptive classes instead of easy to write classes which I am guilty of writing in the past

- The main content of the page the name of the clock. The buttons and the button container and also the clock itself are all stored inside a parent container (which is the div that is centered and has no class or ID. It has no css)

##### CSS

- HTML Tag
    - As always I set the html tag with margin and padding of 0 because I absolutely hate that little gap that you get when you don't explicitly mention that

    - Secondly I chose for this application to add height and width of 100% since it was going to take up no other room. It made positioning the body and div elements.

- div.clockContainer Tag and h1 Tag
    - The color purple here is part of the color scheme I got offline 

    - The clock needed to be centered and consisted of 5 h1 tags but on second thought I can just use one.. 
      
      Okay I changed this. The new and old version is there below

    ``` html
    <h1> 00:00:00 </h1>

    <!--Instead of -->
    <h1 id="Hours">00</h1>
    <h1>:</h1>
    <h1 id="Minutes">00</h1>
    <h1>:</h1>
    <h1 id="Seconds">00</h1>
    ```

- div.buttonContainer 
    - A simple container contained within the parent container. It holds the three buttons and is a flex box with a row flex direction and the content is spaced around because I wanted the left button and right button to be lined with the outside of the clock

- div.button and div.button:hover tag

	This probably has the most going on with it in erms of designs but I think it is most important to focus on the hover animation which is probably my first time using the transition property correctly after seeing it used so many times
	 
	So the background works as following. The button looks like this where although the button is the only visible part the purple part of the button is overflowed off the screen.
	
	<img width="685" alt="Screenshot 2023-01-13 at 23 39 11" src="https://user-images.githubusercontent.com/98868685/212437970-4b8ace54-5acc-498b-a3ab-cdf525341f58.png">


> 🔥
>
> I addded a div.button:not(:hover) so it would animate on the way out too



##### Javascript

Now for my favourite part. The javascript

- I think the first thing to mention is th eclock function. i mean i was originally going to run each portion of time seperately (eg, seconds, minutes, hours). But github copilot actually gave me some really cool suggestions on how to structure the clock function which more or less just incremented seconds on each call and using conditionals set the rest 

- The second thing I took note of was the adding of event listeners to the dom elements. Because I originally had set the script tag above the body tag and because the file is rendered from top to the bottom the script  tag was more or less like 
  
  *"AHHH😱 where are the buttons your telling me to listen to I can't see them😭"*
  
- But when i put said script tag below the body tag it was more like:
  
  *"Ohhhh those buttons, yeh sure! 😎"*
