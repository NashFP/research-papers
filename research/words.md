
*"Exploration #1:  Write 10 things about where you are sitting right now" - Keri Smith*

# Words for Word Time #

Let's try to get this list going from potentially simplest to more obscure topics, details, and language features.

##REPL##
 
 1.  A simple way to interact with a programming language
 2.  Read eval print loop 
 3.  Stores state and values of variables, etc.
 4.  As powerful as any program just requires that you type stuff (or load it in)
 5.  In some use cases, you don't want saved programs, you want computation
 6.  Loading libraries are handy 
 7.  Repl driven development... like a live action performance of TDD
 8.  A great way to get a repl into production or test environment and see what's going on behind the scenes
 9.  Practically a must have for dev.  Even when I code C#, I use linqpad to test snippets out.
 10.  START HERE

##Functions##
 
 1.  Mathematically a transform that maps values from one set into values of another set.  So it has inputs and returns an output.
 2.  In FP, functions are data!  Hence they are "First Class" and have all the benefits of that.
 3.  Pure functions always return the same output for a given input... ie Deterministic.  You can reason about it!  Spock is happy!  
 4.  No side effects.  The only result of calling f on a value x is value returned.  There is no action on the side.  No cheating on your caller.  
 5.  Many languages have anonymous functions that have no name.  Or shorthand notation called Lambda functions.
 6.  Lambdas actually are the creation of Alfonzo Church and he essentially had a theory of computing all based upon these shorthand functions.  
 7.  You could even store numbers in them, etc.  Church numerals.
 8.  Functions should be small.
 9.  Functions should do one thing ideally.
 10.  Traditionally, functions only have one argument.  Don't let grandpa's FP get you down though.
 
##Map##

 1.  A function that calls a function on each of the individual members of a collection and returns a new collection.
 2.  Think of a real life map.  It takes points in our environment and projects them onto surface maintaining relationships, etc.
 3.  Map is the first of the "holy trinity" of functions in FP that help devs get work done over sets of data.  (It's not in the holy trinity of functional programming from Richard Bird's book on Haskell)
 4.  link to Heath's list of map implementations
 5.  I like to think of functions as maps in an abstract sense, but map is really just a common workhorse function you'll find in many languages.  Select in SQL, C# Linq select method, map in python, _.map in _.js, List.Map, etc etc.
 6.  Remember that in FP, since functions are data, you could map over a collection of functions...
 7.  Dora the explorer's pal.
 8.  Maps are commonly thought to be implemented by recursing over a collection linearly head over tail but there's lot's of parallel implementations or implementations that traverse trees, etc.  Lazy maps.
 9.  Don't confuse maps with plans which are more for destroying battle stations. 
 10.  Maps are declarative which means there's a whole class of bugs you'll never make again when you use them.

##Reduce##

 1.  Map's partner in the trinity.  Maps and reduce can both be implemented using eachother, etc.
 2.  Reduce uses an aggregator function to combine all the values in a collection in a single value.
 3.  You can do a ton of things with reduce.  
 4.  Again, its declarative style makes your code vanish and get terse which is sometimes a pain in the butt to read if you're not kind but often is amazing.
 5.  Think SUM in sql.  Or group by.  
 6.  Handy for arithmetic, trees, string building, or applying a kitchen full of functions on some data, etc.
 7.  Reduce can also be lazy.  etc.  Smart people are always going to breakdance.  
 8.  Aggregate, Fold Left, Right, Pipes... a bunch of this stuff interconnects.  
 9.  Smooth jazz.
 10.  map and reduce are your friends even if they aren't pythonic.

##Filter##

 1.  A method that takes a collection and a predicate function and returns the members of the collection that are true for that predicate.
 2.  A predicate takes an x and returns true or false.
 3.  Hey Scoob, Filter is the where in your SQL.
 4.  I put filter in with map and reduce because it's so critical and helpful.
 5.  Discrimination is useful.
 6.  Filter can be implemented with reduce.
 7.  Filters are helpful with coffee.
 8.  A filter on an empty set is empty.
 9.  A filter can be applied lazily.
 10.  Filters are declarative and should be used often even outside of FP.

##Composition##

 1.  To assemble ideas together sequentially.
 2.  To call a function g with the result of the function f applied to x.  y = g ( f ( x ))
 3.  In FP, you can compose g and f together with passing in the x just yet and pass that h = f . g around.
 4.  Composition not only allows us to build incredibly complex functionality but it also allows us to build data structures and even the simplest data.
 5.  Lambda Calculus makes extensive use of composition.
 6.  Notes in a symphony and sentences in a paragraph assemble together in a composition.
 7.  Data structures built with composition are immutable and yet can be used to create new data structures.  Change is possible!
 8.  Foundational.
 9.  Matrices can be composed.
 10.  If f takes x and makes y and g takes y and makes z then g of f takes x and makes z.

##Recursion##

 1.  The ability for an idea or functionality or execution or data to be self-referential and continue on.
 2.  Functions can be recursive and call themselves in their body.
 3.  Trees can be recursive and have other trees on their leaves.
 4.  Often recursive algorithms using recursive functions will have a halting condition.
 5.  Essentially, it's helpful to stop or reach an end.  
 6.  Trees get smaller and small and eventually stop when they become leaves.
 7.  A function will process a list until the list is empty.  Each successive call passes a smaller list.
 8.  Recursion is one of the fundamental theories of computation we get from the 30s.
 9.  Recursion let's us keep things immutable in a function's context and we see change across call boundaries in the stack calls.
 10.  Recursion can lead to stack overflows in naive and overly optimistic solutions to a problem.  (There are optimizations however!  yay science!)

##Immutability##

 1.  Compuational state can be written once upon definition.
 2.  Promising for future thread safety and multi-core computing.
 3.  Mostly eternal truth is handy for reasoning.
 4.  No side effects allowed.
 5.  Life and input-output state often is about change.
 6.  Maintain cores of immutabilty.  Manage mutability on the fringes.
 7.  Small functions and composition help programmers maintain immutability.
 8.  In FP-flavored OO, object methods are static and chainable and return new objects.  
 9.  Append-only databases encourage immutability.
 10.  To programmers grown in imperative languages, assembly, and modern OO, immutability is hard at first, but the problems it solves are actually much, much harder.

##Declarative Style Coding##

 1.  Coding style emphasizing what the coder wants and less how it should be accomplished.
 2.  With composition and higher-order functions, it's easy to grow your abstractions such that more primitive mechanisms in computing are unnecessary.
 3.  Black-box programming hides the details.
 4.  Immutability and no global state and side effects gives you the reassurance of treating a function like a black box.
 5.  Some might call this sugar.  At times it is.  
 6.  For loops allowed us to avoid branches and addr locations.  Foreach allowed us to avoid looping variable errors.  Map and reduce allowed us to forgo a loop altogether and just perform operations on sets.
 7.  SQL might be the most widely used declarative language.
 8.  Whole classes of errors go away when developers hide technical mechanisms.
 9.  It's important to remember that several FP qualities are critical to getting declarative right and not springing crazy leaks where yr primitive details poke out.
 10.  Layers.


 * currying vs. partial function application
 * head and tail
 * closures
 * global state
 * lazy
 * type providers
 * pictures of OO and FP together
 * data structures vs classes
 * inheritance and FP 
 * actors and classic original formula OO as just message passing
 * monads
 * IO paradigms
 * functors
 * back-tracking
 * pipes
 * streams
 * applicative functors
 * monoids
 * tail recursion vs. recursion
 * pattern matching
 * chaining
 * reactive
 * atoms
 * append only
 * macros
 * abstract syntax trees

