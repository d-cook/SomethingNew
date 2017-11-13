**List of relevent concepts for designing relevant solutions**

#### Stepping Stones
* *(Converted this to an issue: "[Stepping Stones](https://github.com/d-cook/SomethingNew/issues/7)")*

#### Moldable Software
* Software (tools) that can evolve or be reshaped into something new or different at will (by the end-user)
* "Sculptable" software: relies on **immediate feedback** between creator and creation. Sculpt the clay while *seeing* and *feeling* it, draw the picture with your eyes **open**, compose the music by **playing an instrument** to see what works (never mind Beethoven; anyway, I thought he could "hear" via touch or something :) )
* Calculus revolutionised mathematics. Partly because it is about expressing systems in terms of **small differences / deltas**. Aim for "continuously" changing software, rather than sudden leaps and bounds of adding code, compiling code, restarting etc. (from Alan Kay)
* The software tool is its own live-editor, and can be inspected and modified in place (without "rebuilding")
* "Strong References": Entities (in code) are referenced directly rather than by name. Changes to the entity (e.g. rename) are immediately reflected (transparent) everywhere that the entity is used
* Ability to edit code (at runtime) without breaking context (e.g. JavaScript closures are broken when functions are edited)
* "[Ultron](https://en.wikipedia.org/wiki/Ultron)": System that can re-compile itself to another platform. As this pattern is repeated, each compiler "comes with" because it is written in the language of the system

#### Self-Defining
* Abstract: Software entities define ("bootstrap") their own creation, language, UI, editor, etc. in a self-evident way
  * Rather than depending on sepate things (IDE, compiler, editors, etc.)
* Surprising that this is not already common, since the tool for making & editing software is ... ***software***
* Bootstrapping: compiler/system that is written in "itself", and can redefine itself ("Moldable Software")
* Software Archeology: self-contained system that makes its own bootstrapping & running self-evident: http://www.vpri.org/pdf/tr2015004_cuneiform.pdf

#### Everything as Objects
* *(Converted this to an issue: "[Structural Substrate](https://github.com/d-cook/SomethingNew/issues/9)")*

#### Message Passing
* Operations between objects (code) are all "messages"
* Alan Kay: objects as a recursion of the notion of "computer"
* Blurred distinction between objects and networked computers (Alan Kay's notion of objects)
* "Strong References" are avoided, so that objects are decoupled (better for composition & serialization)
  * Decouple code by splitting into functional code, and separate execution context that is "passed in"
  * Decouple "closures" from context by using *named* references into a separate "context" object. Thus the context object could be replaced or edited separately, or perhaps (optionally?) passed in separately
* Networked computers (hence, objects) are **automatically secure** because what comes in through the network is just data stored in a buffer. An object can ignore messages and respond however it likes. Code-based security holes occur *inside* the "computer", often due to components within it stepping all over each other (because their internals are not protected).
* An implementation of objects "inside" a computer might not be able to prevent arbitrary scribbling over memory by a determined user. This would require hardware protection of "objects" in the same manner as VM pages. But the common case is errant code having access to internals of the wrong data structures, rather than deliberate meddling of a hacker in a debugger.
* It's a long shot away, and will require changes in thinking only possible through transitional work. But in the intended "mature stage" of OOP, messaging would be to *inform somebody that something happened*, rather than to "command" them to do something. i.e. fully reactive. Vague and not to be applied as a blanket rule, but still worth keeping in mind. Particles and fields, ant colonies, multicellular life, the Internet, etc.
* Distributed systems. Current software is always a big, complicated engine. One spanner in the works, and the gears all stop. The Internet, living organisms, etc. are not brought to their knees by local faults; they **heal**.
* Say what you want about the internal combustion engine or aircraft or computers so far. The first two aren't perceived as endlessly getting bigger. But software is *constantly* growing in influence, and gears **do not scale** by such orders of magnitude. But we are made of trillions of "cells"; how's that for scaling?
* What is "messaging"? Standard: a message is a verbatim (i.e. case-sensitive and spelled correctly) name. You "lookup" the name on the object, you get back a "method implementation". Which is the *memory address* of a *subroutine*. Well OK, but *is your spidey-sense tingling?*
* **Names** do not scale. How about: learning to speak a common language? Discovering, querying the environment? [Call By Meaning](http://www.vpri.org/pdf/tr2014003_callbymeaning.pdf)

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
* And then, make OO about "messaging", rather than the "objects" (see Alan Kay's lament on the name "*Object*-oriented")
* Important difference between "object-based" and "class-based": objects can *specialise* to not act like their kin. If you need to create a new class just to specialise an object ... well, conceptually this is noise; can be tolerated as a hidden implementation detail (since, well, [OROM](http://www.vpri.org/pdf/tr2006003a_objmod.pdf) commits this sin. But it makes up for it by being *self-mutable*, and a starting point.)
* Example: using generic data types (or JSON) instead of creating a new class for every possible "kind" of data.
  * Microsoft .NET frameworks like [WCF](https://en.wikipedia.org/wiki/Windows_Communication_Foundation) and [MVC](https://en.wikipedia.org/wiki/ASP.NET_MVC) are great examples of *failing* to do this; they make it *really hard* to do things generically or just "pass the data".

#### Respect the Human Model
* Related to "Avoid Restrictions"
* Good design (and "doing the right thing") cannot be *enforced* with restrictive mechanisms. It can only be *encouraged* by respecting the human element. See "Linda Rising" and "Jane Jacobs" in the [Resources](https://github.com/d-cook/SomethingNew/blob/master/Resources.md)
* Instead of making programming more fun for programmers, make "computering" better for users (note: have we even discovered what "computer" can mean? Can we open the door to let users do that discovering?)
* A system is not explorable if you can **irreversibly brick it by mistake**. Branching **history**, unlimited **undo**, etc. are a *requirement* for people to feel safe trying things out. See the [Worlds](http://www.vpri.org/pdf/tr2011001_final_worlds.pdf) paper.
* Software components / modules are only meaningful if the abstractions are proper "whole" parts of a human mental model, decoupled from everything else
  * When this is achieved, then composability is more than just a nice property of source code, but something that can be exposed to the end-user through a UI at runtime (drag-and-drop software composition through a UI)
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
#### Object-Oriented CPU. Fundamental object-operations (get, set, delete, etc) are supported by hardware. Imagine something like JavaScript running on bare metal, and all the layers of software that would cut out. This could potentially be much more efficient than traditional statically-typed compiled languages. Related: [Quantum Object Dynamics](http://www.vpri.org/pdf/m2009002_qod.pdf) (how N-way associative lookup is at the base of much high-level semantics. If it were in the hardware, well...)
#### Tool support for a recorder view of the program which supports programming and debugging by demonstration: record, unplay, play, step, unstep, undo and cut (forward) of actions.  Be able to program with the previous operations.  Store a log or trace of operations in the live-editor for use with the PbD system.  Support research into sequence clustering of code, imitation learning and one-shot imitation learning, to model the programmers mind.
