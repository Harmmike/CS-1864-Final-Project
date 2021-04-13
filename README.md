# CS 1864 Final Project
 Final project for CS 1864


Here's the final probject for my CS 1864 class in 2020.

The application itself works fine and meets all the required criteria. I received full credit (100%) for this project.

Some things I'd like to change or improve about this looking back are as follows:

1. UI
   - I'm not happy with the look/feel of the application. There are several areas where you can see the edges of grids exposed.
   - The navigation of the app is handled through code-behind, which functionally is fine. I've since learned about the Command Pattern, and would likely prefer to use this.
   - I think having a static size for the application is ok, but looking back an adjustible and responsive design would have been even better.

2. Code
   - The code in the AppSession.cs is pretty simple and not so elegant, although functional. I think I could improve this by using 2-way binding from the View, adding UserControls to the main window and having additional ViewModels to control them.
   - The codebase feels a little bit "spaghetti" and doesn't appear to follow a clear structure. It looks like I did what I needed to do the way I thought best, rather than researching actual solutions to the types of problems I faced.
   - The math and problem-generating aspect of the code is quite simple. Although the instruction for the project asked for less than was given, I could have done a better job.
   
3. Data
   - The data is saved via a Data Access Layer (DAL) and this was overkill. I should have just included this in the Engine dll and it would have reduced the size/complexity of the project.
   - The logging system is prone to infinite loops. I could change to kill itself and send a message upwards or change it from xml to another type or even add a backup. No matter the solution, I'm aware that this is ugly, and was one of my first attemps at catching errors.
   - I lack strong error checking in the save/load methods. I really am only checking whether or not files exist, and if anything else goes wrong I'm just logging it rather than trying to correct it. I could do better, though I should note none of this was a requirement of the assignment.
   - The save and load classes probably should not be singletons. I haven't investigated the performance of one versus the other, but I have a gut-feeling I should have left them as static classes, or even just instantiated-used-destroyed them.
