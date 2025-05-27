# Generating random expressions for testing and evaluating with XojoScript
 
Something that will eventually be needed when further work happens on this:

https://github.com/charlierobin/expression-evaluation-in-xojo-the-one-that-will-be-thrown-away

ie: something that will help automate the generation of test expressions for my expression parser/evaluator, and also calculate the correct answers so that they can be compared with my own evaluations.

So far everything that I’ve randomly selected and pasted into the Google calculator/evaluator has come out correct, so hopefully it’s all on the right track.

Eventually expressions are going to have custom functions in them, eg: sum( val1, val2, ... etc ), so this will have to be extended to all testing of those as well.

Finally, the expression evaluation project allows mixing of numbers and strings (and eventually lists/arrays as well), and the XojoScript thing (which at the moment is pretty much a straight lift from the demo project that comes with Xojo) can't handle that, so that will need some work as well.

But it’s good enough for now...
