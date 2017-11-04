**List of relevent concepts for designing relevant solutions**

*(TODO: Add concepts gathered from materials listed in Resources.md)*

#### Stepping Stones
* "[Worse is Better"](https://www.dreamsongs.com/WorseIsBetter.html)
* Bootstrap a minimal implementation from which something better can be made, rather than trying to create the perfect thing up-front
  * Initial decision decisions don't matter much if they can be made easily (fluidly) changeable
* Don't try to find the one "best" way / goal / etc., but instead nurture many alternative approaches
* Experimenting with initial stepping stones (Alan Kay: "almost new") is a necessary prerequisite to discovering the "new" thing (Alan Kay: "New" vs "News") 

#### Moldable Software
* Software (tools) that can evolve or be reshaped into something new or different at will (by the end-user)
* The software tool is its own live-editor, and can be insected and modified in place (without "rebuilding")
* "Strong References": Entities (in code) are referenced directly rather than by name. Changes to the entity (e.g. rename) are immediately reflected (transparaent) everywhere that the entity is used
* Ability to edit code (at runtime) without breaking context (e.g. JavaScript closures are broken when functions are edited)
* "[Ultron](https://en.wikipedia.org/wiki/Ultron)": System that can re-compile itself to another platform. As this pattern is repeated, each compiler "comes with" because it is written in the language of the system

#### Self-Defining
* Abstract: Software entities define ("bootstrap") their own creation, language, UI, editor, etc. in a self-evident way
  * Rather than depending on sepate things (IDE, compiler, editors, etc.)
* Surprising that this is not already common, since the tool for making & editing software is ... ***software***
* Bootstrapping: compiler/system that is written in "itself", and can redefine itself ("Moldable Software")
* Software Archeology: self-contained system that makes its own bootstrapping & running self-evident: http://www.vpri.org/pdf/tr2015004_cuneiform.pdf

#### Everything as Objects
* Alan Kay: objects as a recursion of the notion of "computer"
* Everything (code, data, UI, runtime) is made of nestable "objects" that can be inspected and modified in place
* All objects are part of the same "object-tree", with the "root node" being the entire system
* Work directly with intented model (structure) of things, rather than a *representation* of that structure
  * Code is manipulated directly in [AST](https://en.wikipedia.org/wiki/Abstract_syntax_tree) form, rather than [Parsed](https://en.wikipedia.org/wiki/Parsing#Computer_languages) from text
  * Code can be generated & manipulated directly at runtime (by the user, or programmatically)
* A universal tool can be used to view and edit everything, since it all shares a common representation
* An AST structure can model both code & data, but also (for example) files & folders, or settings
* Execution state of a program exists in some inspectable form. Can be paused, modifed, serialized, and resumed
  * Actors that can be sent (or send themselves) across systems, and keep running afterward

#### Message Passing
* Operations between objects (code) are all "messages"
* Alan Kay: objects as a recursion of the notion of "computer"
* Blurred distinction between objects and networked computers (Alan Kay's notion of objects)
* "Strong References" are avoided, so that objects are decoupled (better for composition & serialization)
  * Decouple code by splitting into functional code, and separate execution context that is "passed in"
  * Decouple "closures" from context by using *named* references into a separate "context" object. Thus the context object could be replaced or edited separately, or perhaps (optionally?) passed in separately

#### Blurring the Line
* Between code ([API](https://en.wikipedia.org/wiki/Application_programming_interface)) & [UI](https://en.wikipedia.org/wiki/User_interface) (if they share the same representation -- see "Everything as Objects")
* Between programmatic operations & user (inter)actions
* Between compiler & program / compile-time & runtime / script & compiled program (see "Abolish Compiled Language")
* Between ([LISP](https://en.wikipedia.org/wiki/Lisp_(programming_language))-like) [macros](https://en.wikipedia.org/wiki/Macro_(computer_science)#Syntactic_macros) & other programmatic transformations (macro 

#### Abolish Compiled Language
* Think of uncompiled source code (written in a compiled-language) as a program that makes an executable program, and the compiler as the interpreter of that program. When viewed in this way, declarations within code (classes, functions, variables) act as *imperative commands* to create components of a program. Replacing these "commands" with an API & user-defined functions would allow programs to be generated with *any* components & mechanisms, rather than from a *fixed set* of "language features". No more language restrictions!
* Example: `class Foo { Bar b }` becomes `myClass = MakeClass("Foo"); myClass.AddMember("b", myBarClass)`
* Example: `myTrait = new MyVeryOwnTraitsImplementation("ResizableThing"); myTrait.ApplyTo(myClass)`?
* This is what makes languages like JavaScript so powerful: many things that are "declarations" in other languages are actually imperative calls to user-defined functions. This is why people have been able to make so many different kinds of object-models (etc.) in it.
* This makes things like compiler hooks and reflection mostly obsolete (see "Fewer 'kinds' of things" under "Less Restrictive")

#### Avoid Restrictions
* Related to "Respect the Human Model"
* Not imposing a prescriptive way of doing things (e.g. programming language, code frameworks, set-in-stone UI, etc.)
* Instead of hiding things (like closure contexts) or enforcing restrictions (static types, access-level modifiers), expose ALL things for maximum potential, and rely on good structure & practice to make things clear
* Late-binding & Dynamic-typing (instead of static): Structure is freeform rather than held a rigid calculus
* Avoid pre-mature optimizations that make decisions / set things in stone too early
* Fewer "kinds" of things, and more general (and simpler) common things / representations / tools
  * Simple underlying structure for representing many things ("Everything as Objects")
* Context-based decisions, behaviors, language, UI, etc. rather than prescribing "one for all" ("Self-Ownership")
* Make OO about objects again, rather than about classes (like [Self](https://en.wikipedia.org/wiki/Self_(programming_language)))
* Example: using generic data types (or JSON) instead of creating a new class for every possible "kind" of data.
  * Microsoft .NET frameworks like [WCF](https://en.wikipedia.org/wiki/Windows_Communication_Foundation) and [MVC](https://en.wikipedia.org/wiki/ASP.NET_MVC) are great examples of *failing* to do this; they make it *really hard* to do things generically or just "pass the data".

#### Respect the Human Model
* Related to "Avoid Restrictions"
* Good design (and "doing the right thing") cannot be *enforced* with retrictive mechanisms. It can only be *encouraged* by respecting the human element. See "Linda Rising" and "Jane Jacobs" in the [Resources](https://github.com/d-cook/SomethingNew/blob/master/Resources.md)
* Instead of making programming more fun for programmers, make "computering" better for users (note: have we even discovered what "computer" can mean? Can we open the door to let users do that discovering?)
* Software components / modules are only meaningful if the abstractions are proper "whole" parts of a human mental model, decoupled from everything else
  * When this is acheived, then composability is more than just a nice property of source code, but something that can be exposed to the end-user through a UI at runtime (drag-and-drop software composition through a UI)
  * Read about "Restricted OO" on http://fulloo.info (TODO: provide a more direct link)
* Related: "Software Archeology" (under "Self-Defining")
* Create more of a runtime model (e.g. a whole system) rather than just a language with dependency on a separate compiler/interpreter

----

*Everything above has been refined & organized. Everything below has yet to be.*

----

#### Projectional editing
#### Simplicity over complexity
#### Simplicity of underlying structure, or of mechanism for creating it? Maybe there should be no (or little) distinction between the two
#### Specify structure, or specify process that generates structure?
#### Modeling & editing structure as-is, or modeling and editing a generative process and replacing the old thing by regenerating it.
#### Programming via interaction (e.g. capturing operations as steps of UI operations, rather than trying to visualize a "flow" of operations). Idea taken from Bret Victor's "Drawing Dynamic Visualizations".
  * That is, not a flat look-at-it-all-at-once model of exeuction, but a dynamic interactive model for exploring it. Also see Bret Victor's "Media for Thinking the Unthinkable"
#### Automatic JIT compilation, or compiling only key components (which?)?
#### A basic UI substrate from which anything can be put together (like how any structure can be built from the same object-model)
  * Concept of graphics primitives, or of UI primitives (e.g. boxes), each with their own relative transformations
#### To prototype (or class) objects, or not to?
#### AST means nothing is every "compiled" down to machine level, but instead there is a kernel (written or mirrored in itself)
#### JIT compilation upon code edit, or just projectional view/edit? (is this the same thing?)
#### Still generate compiled programs, but a bootstrapped self-contained tool as a better alternative to "source code"
#### Potential of LISP is generally overlooked, and it is used as JUST a programming language
#### Not a MetaObject Protocol, but a MMOP that is its own MMMOP
  * Lisp Macro expansion does this because the macro language is the same as the target-languages; and thus you can have macro-macros, etc. Apply this idea to UI & code: if they are "the same thing", then ... voila!
#### No need for an OS
#### Replace concept of "compile time" with JIT compilation (i.e. compilation on demand at runtime). How is this any different than any other normal code transforming data (especially if code and data are the same)?
#### If all objects have a UI metaphor, then maybe you don't need a UI for everything? It's like a UI equivalent of a command-prompt? (API x UI = AUI?)
#### A "Grammar" of visual (and behavioral) pieces, and not just textual "language". (Expand this idea to "macros"?)
#### Embedded DSLs and interpreters within existing ones, but all running at the "root" level
#### Instead of using macros to convert from a good representative to an obscure one, choose a good underlying representation to begin with, and a good UI tool for showing & editing it (see "Magic Ink"). The underlying representation can be flexible by allowing context-specific evaluators.
#### There is a way to do this "stuff" and / or create other powerful software tools and engines, WITHOUT a huge pile of frameworks and lots of very specific complicated parts. Once we make such a system, we may be able to find a minimal set of patterns and process that would allow anyone to" bootsrap" almost anything on almost any system, from almost nothing.
#### Object-Oriented CPU. Fundamental object-operations (get, set, delete, etc) are supported by hardware. Imagine something like JavaScript running on bare metal, and all the layers of software that would cut out. This could potentially be much more efficient than traditional statically-typed compiled languages.
#### Tool support for a recorder view of the program which supports programming and debugging by demonstration: record, unplay, play, step, unstep, undo and cut (forward) of actions.  Be able to program with the previous operations.  Store a log or trace of operations in the live-editor for use with the PbD system.  Support research into sequence clustering of code, imitation learning and one-shot imitation learning, to model the programmers mind.
