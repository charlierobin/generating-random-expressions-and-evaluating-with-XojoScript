# Generating random expressions for testing and evaluating with XojoScript
 
Something that will eventually be needed when further work happens on this:

https://github.com/charlierobin/expression-evaluation-in-xojo-the-one-that-will-be-thrown-away

ie: something that will help automate the generation of test expressions for my expression parser/evaluator, and also calculate the correct answers so that they can be compared with my own evaluations.

So far everything that I’ve randomly selected and pasted into the Google calculator/evaluator has come out correct, so hopefully it’s all on the right track.

Eventually expressions are going to have custom functions in them, eg: sum( val1, val2, ... etc ), so this will have to be extended to all testing of those as well.

Finally, the expression evaluation project allows mixing of numbers and strings (and eventually lists/arrays as well), and the XojoScript thing (which at the moment is pretty much a straight lift from the demo project that comes with Xojo) can't handle that, so that will need some work as well.

But it’s good enough for now...

At the moment, it just creates a string of random operands (at the moment numbers, but in the future could be strings, functions, variables, lists/arrays) with random operators inbetween them.

At any particular operand, there is a small chance of a bracketed expression, togther with a small chance of negation, just to make things interesting.

For numbers, there is a chance of a simple integer, or a floating point number, or a floating point number with an exponent.

For example:

```
15+301.8107--9--57.14341*50-279.479-273.1478 = 2630.354

62/61.23692*(60*67*16/83+22+108.589e+1*(-85+(-29/348.5038-83.7658)*-0/-98+77*75))/98/1/353.7215 = 180.4866

13*392.9748e+8+239.6429-456.3374e-6 = 5.108672e+11

29-261.4569e+8+73^100*-295.5008-212.4404+49.556+-42 = -6.351037e+188

79/97+239.2818e+5/(19*-246.5779+-276.3355+-435.7652*-416.4591)*23.986+(98/444.1408-87) = 3165.513

11--401.7872 = 412.7872

24*-214.0322+-69 = -5205.773

-344.2521e-5*16*20-333.5009/394.2038^274.8004e+6/27*495.5383e-6 = -1.101607

34/54.99536*220.5633e+9*26*123.577e+5/-386.9345e+10-(98^416.4944e-4)*35 = -1.132299e+7

379.9684*30 = 11399.05
```

There is no effort to catch division by zero or anything else that might generate a NaN or an infinity, as I figure that my own expression evaluator will have to handle those errors properly as well, and therefore the random expression generator should leave them in.

That aside, it does generate “correct” expressions, ie: balanced brackets and so forth.

But I’m now thinking that it should perhaps also generate some deliberately wrong expressions, perhaps ones which have had some characters randomly deleted from them, just so that the error handling of those can also be fully tested.
