## What is Firefox Replay?

Firefox Replay helps you construct a chronology of events in order to understand how your application changed over time.
## How to Get Started with Firefox Replay

To test out some of the most important functionality of *Firefox Replay*, let's experiment together using [TodoMVC, a simple and free-to-use TodoList application](http://todomvc.com/examples/vanillajs/).

1. **Start Recording** - With the DevTools toolbox open, and the "Debugger" tab selected,  hit the circular "Enable WebReplay" Icon
2. **Add a Logpoint** - With Devtools open, click the "Debugger" tab to open the debugger. In the Sources tree in the right-hand sidebar, navigate to [examples/vanillajs/js/model.js](http://todomvc.com/examples/vanillajs/js/model.js). Then, right click line 29 in the right-hand gutter of the Editor window (pictured) to open the context menu, and select "Add log". When the new input box opens up below that line, type in a valid string (e.g. "Hello, world") and press Enter to activate the logpoint. When the logpoint has been entered correctly, the arrow in the gutter (over "29") will turn purple.
3. **Record a Change in Your Application** - Let's start by making a simple change to our application state. Enter the letter "A" into the input box at the top of the todo-list app, and hit enter.
4. By making the above change, you have caused the code on line 29 to run. Since our logpoint on line 29 has been triggered, you should notice two things:
      1. If you switch to the "Console tab", the logpoint string ("Hello, world") has been printed to the console once.
      2. A circular point has appeared on the Replay timeline. This is the "point" in time that your logpoint was triggered.
 
 5. Next, let's make another change. Enter "B" into the input box, and hit enter again. You should see a second element added to the To Do list, under A. You should also see another "Hello, world" printed to the console (when the "Console" tab is active), and another point added to the replay timeline.
 6. Now take your mouse, and click on the second (most recent) point on the timeline. 
 7. You should notice a sudden change. No longer does the "B" todo appear on the list. Instead, the application state shows "B" still in the input box, right at the last point when line 29 was triggered.
    
    You've successfully traveled backward in time!
    
 8. Now take your mouse and while hovering (without clicking), move it back and forth on the timeline. As you move it to the left of a point, you should notice the state of the todo app change to how it was previous to that point. As you move it to the right of a point, you should notice the state of the todo app change to how it was after that point.
 9. Now, using what you've learned, **do some experimenting!** You can:
       1. Add new logpoints at different points in the codebase.
       2. Inspect how the attributes of the app change depending on which "jump to" point is selected on the *Replay* timeline.
