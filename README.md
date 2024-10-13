# Bit-Board

Starting off with the utility class, I had the base foundations of what a class like this needed to do, I just needed to implement it in a way that it could perform actions with bits instead of normal data types. I scoured the project details sheet for all the items this class might need, which I combined to make the class itself. I have always programmed in java, so I knew I wanted to do that after I found out that java did bitwise functions. I also learned about the << function when researching some of those functions. I found that I needed my converter method to be used on almost every other method to make sure the output was correct. 

My variables were quite simple here, as the methods only need a value and position, and the arithmetic needed two values. To output all the correct binary strings, I made sure all of the methods used the string return.

Once I started work on the bitboard itself is where I found my first troubles. I realized that my parameters for some of my methods in the utility class were not the right variable type. Each of the player boards neeeded to be intialized as a long, and many of parameters took an int. This was made readily apparent when I learned that Java initializes longs into 16 bits already, which is handy, but needed to bhe fixed. This also created other problems in my bitboard, but my IDE IntelliJ easily picks out issues and sometimes gives a way to solves them immediately (ie parsing variable types if they needed to be converted).

Re evaluated that and I realized I just needed to change one instance of a long in each of the methods to make it not so weird with changing the variables between longs. (thanks ide for telling me)

Finding out how to initialize the board was also a task, because I have to research how to create one and trial and error the exact longs for each board. It was incredible once I figured out that AA55AA was pretty much all I needed. 

I think the idea of moving the pieces was the hardest part to challenge mentally. I had to create a way to manipulate a long without shifting the items in the wrong way. Turns out it wasn't hard out all. All I had to do was have the parameters implemented and just switch the bits at the given index. I just laid the roots down for later, as I know I need to have a legal move checker to make sure these moves work.

The legal move function is a bit weird, because there are many types of illegal and legal moves. I think it would take a while to do many of the illegal ones, but the ones I did figure out are making sure that the bit its trying to move into is not taken and that its in the bounds of the indexed grid. Once I had this method created I implemented it into the movepiece method for ease of use.

Capture was a similar method, but I had to create a way to check when a piece needed to be removed because it was jumped over. Again it seemed like a challenge but it was as simple as checking which players turn it was, and using the position of the other players piece to remove it.

Printing the board was simple I have done this a million times, I just represented it in a way that was easy to read which a simple for loop.

To test my methods and game actions, I started with hard checking the methods just by running lines with the parameters directly input. Once I knew my methods worked as well as I needed them to, I just made a simple menu that changed player turns, asked for inputs with a scanner, and checked the game state. I added a couple print lines for ease of use and to make sure the players know what is happening.

I think overall the project was really difficult trying to figure out how java wanted to work with bits, but I think I overshot the difficulty of the entire thing. Most of the shell was things I have done many times, it was just the learning curve and research of the bitwise functions that I had to be clear on before I could succeed. That being said, kinging was something I could just never figure out. Playing within the bounds of the rules is difficult, and first I had to make sure the pieces couldn't move backwards which was difficult. Also I don't know if its even possible to represent a bit as a special king without the players just being able to move any piece like a king. 

I did notice that I was overprepared for what I was able to complete. I was able to complete all that I did without many of my utility class methods. Now that I look back at them, I probably had the same issues with converting the variables. I will still submit them, but I didn't use most of them.

Very fun project however! Very challenging but also informative.

