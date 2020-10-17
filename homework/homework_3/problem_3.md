## (20pt) Print A Single Linked List In Reverse Order

Going backward is fun sometimes.

Let's write a function to print a single linked list backward to the screen.

"if one can only go one-way from head to tail in a single linked list, how do we travel through it backward?", you ask.

Well, since a Stack is FILO, it is a perfect candidate for this job. Imagine walking through the linked list and pushing each node's value onto a stack. Once it's through, simply pop everything from the stack and print to screen and you are done! 

Stack is great for visiting things in reverse order of the visit.

Please **only** use the Stack from problem 1 for this task. You can choose between ArrayStack and LinkedListStack. Please do not use any other data structure such as array or list or it'll zero the points.

"Wait!", you say. "If it's printing to the screen, how do we test this?". I'm very glad you are asking that. For this test we will use the idea of "dependency injection". This will be explained in Monday lecture but for those curious please read the test code to understand how it's done.

And finally we'll meet our good old friend "main()" in this homework :)