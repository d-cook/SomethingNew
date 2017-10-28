*(Abridged) Conversation between Pavel & Dan in response to the Fonc-decommission email.*

----

Pavel Bažant <pbazant@gmail.com>
<br/>30 July 2017

Your list of sources is awesome! It looks like your list goes beyond the particular flavour of innovation that resonates in the FoNC community. In particular, you mention the Intentional Domain Workbench and the Meta Programming System, the latter of which I am a huge fan of!

In fact, I am developing a user-centered software innovation, as you call it, too. My project could be described as a homoiconic spreadsheet based on interlinked tree structures instead of just tables. I took many ideas from MPS as well as from traditional spreadsheets like Excel.

I, too, am trying to find as many diverse resources as possible. Perhaps we could cooperate. I also have some friends here in the Czech Republic who are highly interested in user-centered programming.

Could you briefly describe your project?

----

Dan Cook <dcook0819@gmail.com>
<br/>3 October 2017

Sorry for the delay. It's hard to describe what I'm making, mainly because: (1) I am less interested in creating a specific software tool or language, and more interested in the kind of process (for making & manipulating software & data) that comes out of it; (2) whatever system or tool I create is meant to be able to reshape itself into something else entirely, so whatever I start with is just a stepping stone; and (3) this is somewhat of an experiment to see what kind of system or abilities can come out of this...process.

A couple analogies may help:

It's like I'm trying to create an environment in which new life forms can be created or evolved from existing ones, or new organic matter can be created from existing forms. Now I'm not interested in creating a particular lifeform or organic thing, I just want to make it possible for anyone to create & evolve whatever they want. The tricky part is creating the *first* lifeforms / organic matter, because they have nothing to evolve from, and must be created manually. Also, the creation of new things from old things has to be enabled by some mechanism of the existing life/matter. So the trick is not to come up with the perform forms, but some minimal set of things from which new and better things can be evolved, and possibly replace the old things altogether.

Or perhaps it's like having a special kind of material from which any tool or machine can be created. Imagine a clay whose physical properties can be modified through direct manipulation: by applying the right kinds of pressure, forces, temperature, etc., you can make it hard or soft, more or less electrically conductive, elastic, malleable, etc. The only tools you need to create anything and everything are your hands, and the clay itself. You begin by creating rudimentary tools with your hands, and then use those crude tools to create higher quality tools, and so on. Once a thing is made, you can still manipulate it if you have the right tools (apply the right pressure in just the right ways, etc.). Now certainly you cannot make a high quality telescope with just your hands; but since you can "get" whatever tools & machines you need by hand as part of the process, you can still "make" such a thing "by hand", starting from almost nothing.

Now sure, it would make sense to create some high quality tools and keep them around for reuse; but you are not committed to them specifically, nor are you limited by what kind of tools you have. If this universal material were highly available and cheap, only an idiot would by expensive tools for working with the stuff, if it was easy enough to refine them yourself (especially if you reuse what you make). By the idea is that you are not limited to what has already been made FOR you; anything is possible.

What I like about the material analogy is that this is already mostly true of software. That is, you can do anything imaginable with software if you have the right tools. But what kind of tools do you use to manipulate and create software? ... Other software! Why then are so limited as to what can be done with software? It's because this self-modifying-tool has not been made yet.

That's where the "life" analogy hold up better than the "materials" one: unlike the clay, you cannot TOUCH software with your hands; it's intangible (sort of). But, once you have the initial software tools to manipulate it, you should in theory be able to do whatever you want with it.

Some may argue that this is already the situation, but I say it's far from it (or at least in the middle somewhere). We are restricted by programming languages which say exactly what we can express and how; and many other restrictive & prescriptive ways & tools & formats ... I won't get into it right now. But what I am trying to make is a tool that allows you to create whatever, and do it however; and that is only possible is the tool can be used to modify and replace itself.

There is SO much more I can say about why the difference between source code and executable code (and between runtime & compile time) is an absolutely arbitrary distinction that severely limits software creation and complicates programming languages. There is more I can say about why I think COLA & MPS and other tools fall short; ... but I'll save all that for another email.

One thing I will say though, is that Bret Victor comes closer than anyone I have ever seen to at least bridging some of these gaps *conceptually*, and his many demos and viewpoints are (and will continue to be) a great source of inspiration for what I'm after. And there are others, but I will stop there.

I sincerely hope that this correspondence goes somewhere meaningful; thanks for inquiring! And if what I say seems odd or naive or confusing, or not in line with your direction, perhaps we can endeavor to understand our different viewpoints & goals & approaches better, and find some sort of synergy to produce better outcomes than we would have on our own.

----

Dan Cook <dcook0819@gmail.com>
<br/>5 October 2017

Thanks for the reply! Just a quick answer for now(will go into more detail later): I agree that what is needed is a substrate/a set of substrates that is so flexible that it is able to replace itself continuously (this is already the case today, but only in a very limited sense). e-mail is fine for me as a communication medium. We could also discuss over Skype or Google Talk/Hangouts. What you write is extremely interesting. I, too, consider my project a kind of stepping stone, but without such stepping stones it is very hard to make progress.

BTW, could you elaborate on the weaknesses of MPS? Not technical ones, of course, but conceptual ones.

----

Dan Cook <dcook0819@gmail.com>
<br/>6 October 2017

I feel this response will be very disorganized, so I'll just spit out my thoughts in no particular order:

I could list what I like or dislike about various projects like MPS or Lively Kernel (and I will), though the nature of that kind of commentary might seem pretentious/contentious, especially if it reveals differences in our goals, values, or expectations. Though I do think that is inevitable to some degree, I am quite pleased & excited at how similar our goals & visions are so far, and I see great potential in collaborating on this topic. At worst, we can trade valuable ideas & outlooks and do different things with them; and at best, we may find that we are trying to do the same thing and collaborate to develop something superior to an individual effort.

On that note, my expectation is that we share as many ideas, outlooks, etc. to grow as big of a picture as possible, and then either develop something grand from it, and/or try different things but share a much richer ecosystem of thought. I mentioned that in the FONC mailing-list, and I don't think anyone has agreed on a good place. I plan to create some documents on my github project for that, and I'll follow up about that later. It might be better to create a new project (or something) just for that, but something has to start somewhere. I think I'll create a document listing a collection of goals or ideas, and another listing other resources (projects, videos, etc.); and then perhaps separate ones for specific topics if they become worth expanding in detail. I think something like that that group of people can contribute to & take from would be great! 

...

So here's my response to MPS:

Firstly, the idea of embedding a mix of "views" into code is EXCELLENT. I think a superior way to model & interact with software is to create better (of "the ideal") views for the thing being modeled -- and I think that textual code is not ideal for most things.

More than that, a lot of it is about simplicity/complexity. The goal is to create the most simple & direct representation of the thing. Simple for viewing & understanding it, for creating & editing, etc. However, if that requires dealing with more complexity (more tools, more code, parts) to do those things (understand, create, etc.), then I think that the advantage is lost.

Granted, I don't have any true experience with MPS; just the various videos I have watched, and the papers that have been written about it. But I look at the examples/walkthrough, and dig through some of the sample projects, and ... my goodness is there ever so much more code and parts to deal with than there might be had I just coded up the equivalent thing! Also, what I see is a lot of TEXTUAL CODE. Yes, it enables DSLs and visuals that are not available otherwise; but the amount of CODE to get that ... I watch the videos showing how X and Y and Z altogether make W so much more straightforward to express, but I have to know understand all this other CODE to understand my other code. The transformational views are a great idea, but it looks like a lot of it is still very very CODE oriented. I think if done right, the visual transformations could be had at more levels, so it's not about having nice views in some keys places and code code code (and much more of it) everywhere else. Text, text, text ... how is this better? I mean, sure, that enables parts to be better represented, but you still have all the other code to deal with; that's more complexity: more to look at, more to understand, ... etc.

Also, MPS (like many many other frameworks and tools) lays out a prescriptive way that things must be done. Here are your structures; here are your languages; here are your ... I don't know off the top of my head, but it looks like there are many different kinds of things & concepts that must be involved. The fact that you look at the navigation panel (tree view) of a project and it has to fit this complex predetermined structure ... it's prescribing this form onto everything. I feel that this is a hard argument to make, and sounds opinionated and weak; but I see it elsewhere, and perhaps some examples will help:

If you've ever used TFS (really TFVC) in Visual Studio (Microsoft's integrated source control), that's a great example of an overly prescriptive structure. It tries to force you to structure your repository in terms of Teams, Team Projects, Branches, Folders ... and it has preset ideas about how those things can be structured and in what order, and what you can do with what. It forces a particular view of how Microsoft thinks you should organize your projects, and it conflates that with how the source control tool is allowed to work. Those are two separate things. I good source control (or version control) tool doesn't have ANY notion of what you are making or how you structure it, and you can do what you want and branch/merge whatever & wherever.

Or take HTML for example. There are all the different types of elements, sure; but most of them are really just the same thing: either a box (div) or an inline section (span), and you can set the same properties on most of them to control borders, padding, spacing, etc. Imagine if every kind of element had different properties & rules for all these things ... it would be a nightmare! But because of the common box-model, you can basically just do whatever you need with whatever. This is less true with most UI-components outside of HTML (e.g. WinForms).

One thing I do think is a promising way to approach software is to stop specifying lots of different kinds of things, and instead have fewer & more general things, and let the user or programmer control them as needed. That is what makes HTML more powerful than many other UI frameworks; and it is what makes JavaScript so powerful and expressive (and it's also why the addition of "classes" to ES6 is backwards progress).

That leads me to another point: Of all the things tools in MPS that allow you to express things however you want, the manner in which you express them is NOT flexible; it's a rigid set-in-stone framework for building a certain way. I'd like to see a tool that can serve as it's own editor, or a tool wherein all the components that make up that tool are no different than the components that the tool allows the user to create. This is why the substrate-language for my project is designed in a way that you could manipulate the very interpreter/compiler at runtime. The components of the "engine" are no different than any other components or objects that can be created & manipulated by the user or by code running in the system.

One final note: If I wanted to take ALL DAY to compose this (and I could!), then I'd tie in lots of resources (videos / papers) to make my point. If you want to ask (or rebuttal) about anything I have said, I could probably list some materials to support some of my views & claims. Most of them will come from the likes of Alan Kay, Bret Victor, Christopher Alexander, and Jim Coplien, but there are others.

I won't go into detail here, but for reference, some source relevant to this are Bret Victor's "Magic Ink" and "Learnable Programming" and "Drawing Dynamic Visualizations", Douglass Crockford on ES6, and something Alan Kay said about not inventing a new thing for every different kind of thing (I'd have to find the right video).

...

One more thing:

I assume we'd both agree that one thing that MPS gets spot-on is representing everything in AST form. (I said earlier that everything was textual, but what I meant was that the view of many things remains as textual code, which is not the greatest model). The AST model by which both the programmer and the compiler/interpreter understand the code, so why not just view & edit that directly? All the concerns of parsing and what can be parsed etc. are artificial.

I actually think that a node-based model should replace MOST instances where textual data is used to capture data or information. Like the structure that is modeled by JSON or XML (not the textual layout, but the structure) which lets you create any ad-hoc structure of data with arbitrarily labeled & nested nodes. And not just for programming & code, but general purpose use. Imagine if it was normal to create a grocery list as a list model. Etc. Imagine how easy it would be both for a user to manipulate and search and copy/paste at the node level, as well as for a program or tool to do the same. Furthermore, this would create a situation in which many things are SUDDENLY using the same model. For example, what is now stored as textual data, but also file & folder structures, and perhaps settings in the OS. There would suddenly have to be a lot fewer specialized tools and views (in theory), and so many more things just magically become editable and viewable in a familiar format.

I once put forth this idea to a colleague, starting with "why are we still coding textually nowadays?" and expanding it into the above idea, and the response I got was that plain text is universal and you don't have to rely on a certain tool or support for it. My response was that this is already the case for plain text: everybody has agreed on a standard code(s) for what means what, and how to display and store it. I don't see why a simple node model could not have had the same universal support. Yes, there would be serialization to worry about (and the thing with text is that it already is in a serialized form) ... but imagine if plain-text was not the substrate of communication (e.g. with HTTP or REST), but instead a good protocol had been invented for transmitting nodes of data. The limitations are really quite artificial. I could even take this further and complain about how much I hate client-server exchanges in statically-typed languages like C# when they try hard to force you to create a new class and/or interface for  ... every ... single ... possible ... representation of data that you might send or receive. Wouldn't it be so much easier if the data format was universal and you could just "get" it? ... Anyway, I'm getting off topic.

Anyway, the response I got from that expansion was that I am living in a made up world of impracticallity. I won't disagree about the practicality of magically changing the world around me; but I do think that I can POC that such things are possible. As might be apparent by now, I'm interested in more than just a better programming model, but a rethinking of how all things on a computer are represented and dealt with. But I disagree with the perspectives of "that's just not how things work" and "things now are so much better than they were".

Also, It was put forth to me that a "good IDE" does a ton of magic for you to understand your code and help with refactoring, etc. But my goodness is there ever a colossal amount of work (and code behind) for it to be able to do that, and it does not scale to other applications or new operations. Well, how about this: imagine if every WYSIWYG UI-editor (where you drag & drag GUI components and get generated code for it) were instead replaced by a special textual format where you literally create rectangles and buttons from text (like ASCII art). What a ridiculous substitution that would be! Can you imagine how much work it would be to change the size of a panel, and how much text you'd have to edit to do that? Well, what if I told you that that's what a good IDE is for? One that is SO good that you can drag the textual borders and it modifies the grid of textual characters right before your eyes. Surely if people were used to having to do it all textually to begin with, the response would be what an amazing tool that is. Surely text cannot capture all the nuances of size and other things though? Well, how about some grammar for annotating data next to things ... Anyway, this is clearly ridiculous, but I can argue that it is the current state of how we view & edit code.

Again, Bret Victor's "Learnable Programming" and "Magic Ink" provide great support for these arguments.

So by this point it might be clear why I say a medium other than email may be helpful, though at least typing it out captures the information for reference later.

I think that creating a place to capture such views and points from myself and others (but probably not in such drawn-out prose) would be beneficial.

----

Pavel Bažant <pbazant@gmail.com>
<br/>7 October 2017

Most of what you write seems pretty obvious to me:-), but only thanks to the fact that I contemplated these very questions in the last say 5-7 years a lot, and "unlearned" a lot of prior "knowledge" along the way. I will intersperse my comments into your observations.

...

[Dan] ...one thing that MPS gets spot-on is representing everything in AST form...
[Pavel] I think they want to make the system feel at least a bit familiar to new people, so the try very hard to make the editor feel like a text editor. The unfortunate result is that the structural editing is not utilised to its full potential.

[Dan] The AST is the model ... why not just view & edit that directly? ... [parsing is] artificial.
[Pavel] Exactly. The need for constant parsing and unparsing of stuff is an artefact of certain technical decisions. There is nothing inevitable about parsing -- systems that are able to bootstrap new versions of themselves without using text at any stage of the bootstrap are perfectly possible and IMHO extremely desirable.

[Dan] I actually think that a node-based model should replace MOST instances where textual data is used ...
[Pavel] Yes. An agreed upon node-based data substrate would make a lot of the complexity induced by the primitivity of flat text-based data disappear. It will be very hard to find a way to make this transition in the real world. Not impossible, but very hard.

[Dan] I once put forth this idea to a colleague ... rethinking of how all things on a computer are represented and dealt with ...
[Pavel] Most people do not feel the motivation to question the fundaments and do not spent too much time trying to understand root causes of problems. Moreover, we both have likely spent years thinking about this stuff, so we shouldn't expect anyone with mainstream knowledge about programming to grasp the ideas in a single session -- it may take many months to unlearn some of the old stuff and most people even won't be motivated to unlearn.

[Dan] Also, It was put forth to me that a "good IDE" does a ton of magic ...
[Pavel] Yes. Of course the monstrous text-based IDEs are just a hack to cover the inadequacy of pure text editing as a general data manipulation / modeling metaphor. What is interesting is that the more advanced such IDEs are, the more they tend to resemble structure editors.
I even posted a rant in FoNC called something "1d text considered harmful" or "flat text considered harmful" (I cannot find it right now), but some of the readers of FoNC were not amused.
 
[Dan] Again, Bret Victor's "Learnable Programming" and "Magic Ink" provide great support for these arguments.
[Pavel] I watched almost every video by Bret Victor as well as Alan Kay. Great inspiration.

[Dan] So by this point it might be clear why I say a medium other than email may be helpful, though at least typing it out captures the information for reference later.
I think that creating a place to capture such views and points from myself and others (but probably not in such drawn-out prose) would be beneficial.
[Pavel] There are more people like us. We should all communicate.

[Dan] Firstly, the idea of embedding a mix of "views" into code is EXCELLENT. I think a superior way to model & interact with software is to create better (of "the ideal") views for the thing being modeled -- and I think that textual code is not ideal for most things.
[Pavel] Agreed.

[Dan] ...The goal is to create the most simple & direct representation ... if that requires dealing with more complexity ... then I think that the advantage is lost.
[Pavel] Yes, but we can use MPS as a stepping stone. MPS is hideously complex, but it is a very important demo that full-featured *extensible* projectional editing is doable.

[Dan] Granted, I don't have any true experience with MPS;
[Pavel] Then, I urge you, go ahead and create some MPS projects. Some aspects will be ridiculously easy to implement, some will be tedious and frustrating. Even with all this frustration, MPS is a net win for me. Actually trying to build stuff with MPS will help you understand what are the problems of MPS even better. I will be happy to assist.
That said, my newest project does not use MPS. I took inspiration from MPS and am implementing a projectional "environment" in TypeScript. Ultimately, I'd like to ditch TypeScript and bootstrap the environment from within, thereby getting rid of parsing.
 
[Dan] ... my goodness is there ever so much more code and parts to deal with ... a lot of TEXTUAL CODE ...
[Pavel] Yes but MPS does have the potential to become less code-oriented, I hope. As said, MPS is a zeroth generation demo. Those ideas should be streamlined to the extent that every motivated and reasonably talented programmer should be able to bootstrap his/her own MPS-like environment!
There is one important thing that MPS-style structural editing offers, even if the projection used is a "textual" one. It allows to separate identity and name. The identity is some GUID that never changes. The name is stored in the node and the editor just uses the name in the projection. This makes renaming trivial -- the identity stays the same, so no refactoring is needed. It is sort of a database normalization -- instead of repeating yourself and scattering the name all over the place, you store the name just once. It is the same with people -- the Social Security number of a person identifies them, whereas the human-readable name (Given name + surname) doesn't -- people's names change (marriage, other reasons) and many people may have the same name.
Again, the problem with name collisions in programming is avoidable.

[Dan] MPS (like many many other frameworks and tools) lays out a prescriptive way that things must be done. ... I see it elsewhere, and perhaps some examples will help:
[Pavel] Yes this bothers me too. Fortunately, this is a property of MPS and not inherent in the idea of projectional editing.

[Dan] ... the manner in which you express [things in MPS] is NOT flexible; it's a rigid set-in-stone framework for building a certain way.
[Pavel] This is not entirely true. You can define your own mechanisms for the various aspects and use them instead of the prepared ones. This may not be apparent from some of the videos, but actually the "set-in-stone" part is rather small. A lot of MPS is written in MPS, you can extend and modify it etc. That said, I, too, would like the "set-in-stone" part to be even smaller.
 
[Dan] I'd like to see a tool that can serve as it's own editor ...
[Pavel] MPS is actually pretty close to this -- the editor language presentation is described in itself, the structure language structure is described in itself! It should be not too hard to bootstrap MPS completely into itself, but for some weird reason Jetbrains chose not to do it :-(

[Dan] ... [my] substrate-language ... you could manipulate the very interpreter/compiler at runtime. The components of the "engine" are no different than any others ...
[Pavel] This sounds awesome!

[Dan] If I wanted to take ALL DAY ... I'd tie in lots of resources ... from the likes of Alan Kay, Bret Victor, Christopher Alexander, and Jim Coplien, but there are others.
[Pavel] I will look at Christopher Alexander, and Jim Coplien more closely, thanks for the references (I already follow Alan's and Bret's activities).
I think it is easier to "persuade" other people by showing them working demos than by arguing. Without a demo, we place a huge burden on the other people's imagination. What is easy to imagine for me or you may not be easy for others (and vice versa).


[Pavel] Your ideas are very close to my ideas as well as those of my friends ... I think it would be helpful if they joined this discussion ...

----

Dan Cook <dcook0819@gmail.com>
<br/>10 October 2017

Some replies to your replies:

[Pavel] I think they want to make the system feel at least a bit familiar ...
[Dan] That makes sense. One could argue that they are breaking less ground by doing that. I mean, if you're going to show this radical new way of designing & editing programs, then why not go all the way? But the answer is obvious and valid: it has to be marketable and not too extremely different to be successfully adopted into existing development practices. I think they did the right thing in that regard. I also think that our goals are more toward pushing new boundaries all the way. Alan Kay's "The Future does not have to be incremental" comes to mind (and how he compares "New" versus "News").

[Pavel] Most people do not feel the motivation to question the fundaments ...
[Dan] Agreed. I think that what I said about (JetBrain's goals with MPS versus our goals with something new) applies the same here as well.

[Pavel] The monstrous text-based IDEs are just a hack to cover the inadequacy of pure text editing ...
[Dan] I have noticed the same thing. :) And that's exactly it: the structure is the thing being worked with/on, so the text is just an unnecessary intermediary.
I could also extend this to argue about the advantages of dynamically-typed languages over statically-typed ones (though it's not exactly the same point). Not to say that one is better than the other, but the idea with a dynamically-typed one is that it keeps the structure around and you can see it at runtime; whereas a statically typed language imposes rigid rules to make certain guarantees. Here's an Excellent article (that every programmer should read) on that topic: http://blog.steveklabnik.com/posts/2010-07-17-what-to-know-before-debating-type-systems

[Pavel] I even posted a rant in FoNC called something "1d text considered harmful" or "flat text considered harmful" ...
[Dan] It seemed to me that the COLA project had most of what I was looking for, if only was are ok being restricted to textual representations for everything. On that note though, I HIGHLY recommend that you (or anyone doing what we're doing) read his paper on Open Reusable Object Models. I think it's highly relevant, and contains GREAT explanation & models that his videos don't quite capture. It actually made me deeply disappointed when I learned about Meta-Object-Protocols, because (though awesome in themselves), they only peel back one "layer" of the OO model, whereas Ian's is circular/bootstrapping in a similar manner to what I'm trying to achieve ... except I want to extend that to UI and not just "code".

[Pavel] (we can use MPS as a stepping stone). (MPS is hideously complex), (but it is a very important demo that full-featured *extensible* projectional editing is doable).
[Dan] I agree with all 3 points individually :)

[Pavel] I urge you, go ahead and create some MPS projects. ...
[Dan] I hardly have the time to justify any of what I am doing, to begin with; but it's something I think I'm meant to pursue, and I make whatever little time I can. ... In that light, I don't know if I'll make time to explore MPS like you say; though I DO agree that there is a great potential to learn from what it does or does not do. Maybe someday; but for now I'm glad there's more than one of us to pull experience & perspectives from.

[Pavel] I took inspiration from MPS and am implementing a projectional "environment" ...
[Dan] That sounds awesome! I'd be very interested to see what you've come up with, what you've taken from MPS, and how you plan to bootstrap. That's probably too much detail for this thread (unless you keep it general), but I definitely hope to see more about that as we move forward.

[Pavel] ... MPS does have the potential to become less code-oriented ...
[Dan] That's good to know. It would be nice to see someone explore MPS to its limits. If I had a LOT of time on my hands, that might be me; but that's not the case currently, and probably not any time soon. But it would be great if someone were to demonstrate this someday :)

[Pavel] [MPS] allows one to separate identity and name. ... The problem with name collisions in programming is avoidable.
[Dan] I think I understand this clearly, and it's definitely one of the strengths of MPS, and it's also one of the central features of the Intentional Domain Workbench. This is DEFINITELY an important idea that's been on my mind for a while, though I'm not sure exactly how I'll address it. There is MUCH for me to say on this (or on the topic this is leading me to here), but in brief this affects what kind of substrate language/model I want to use to represent code & entities within the system. One major question I have come across is whether "code" should use concrete references to things, or refer to things by name and rely on contect or scope. This is complicated. One thing I also think about is what the best "coding" model is versus what the best representational model is. Ideally those should be the same thing; but if you look at how you want to code-up a definition of something, and whether you want to be able to serialize or "drop-in" code from another external context ... it's complicated. I've so far opted for a "by name" model in what I'm currently implementing; but I may have already broke my philosophy by storing explicit references to lexical-scope within "function" objects.

[Dan] Two related thoughts are that (1) I will have to implement SOMETHING that makes sense and not make it too complex or think too hard about it, and once it works I can manipulate the system directly and reshape it into something else in case I decide that another way is better; and (2) from there I should do just that, and reshape the system in many ways to do multiple experiments as to what can or should be done with such a system and how it can or should work.

[Dan] That's another thing we should think about in general: not picking "one path", but exploring at least a few, whether they be parallel "forks" of decisions or completely different approaches.

[Dan] Another related thought is that perhaps it's valuable for it to be normal for each system to work however is best for that system. For example, instead of writing software in a certain language or for a certain IDE or tool, what if those things (the language, how it builds, the UI through which it is edited, and the "thing" being edited) were all part of a single self-contained (and self-executing) package? The thing that would stay the same across each such thing would be the fact that they are self-defined, self-executing, self-editing, etc., but otherwise the "how" of any of those parts could be changed to be completely different. For a typical "enterprise" software project, I could see something where the code and representation is all highly dynamic and late-bound, but then compiles itself down into a more optimized "output" program.
 
[Pavel] MPS is actually pretty close to [what I just said above] ... not too hard to bootstrap MPS completely ... Jetbrains chose not to do it :-(
[Dan] Well that's cool! ... the reason is probably for marketability like I said. As cool as it would be, unless they took it "all the way" (like I said about getting more visual, etc.), I doubt enough people would see any value or use in that, based on the way that I think most people are using it. But yes, perhaps that would (or would have) change(d) things.

[Pavel] ... easier to "persuade" [with] working demos than by arguing ...
[Dan] I absolutely agree. ... I realize that the irony is that this is one of the main goals of what I'm after anyway: A way to express whatever one wants in the way that makes the most sense, and likewise to be able to freely change the tools that make this possible (and thus, have whatever tools or representations one wants ... WITHOUT the rigor of traditional coding). As Bret Victor says in "Learnable Programming", the main role of a programming language is that of a User Interface, and in fact it's a terrible interface.

[Pavel] seems ... we actually do want to build "the same thing" ... very close to my ideas [and] my friends ... 
[Dan] That's still quite exciting. At this point, I've probably stated enough for you to decide if that's still true. It's almost hard to believe since it's been almost impossible to find anyone else with the same goals & perspectives (Again, that's why we need to do this, because it's NOT yet how software is understood). One area in which I think we are bound to differ is in the "how", and I don't think that's a problem. As I said, I think we should explore multiple approaches, and variations on them; and I do think it is very likely that any one system (or portion of) could be bootstrapped into the other once they are working.

[Dan] My project on github starts from the "language substrate" (or interpreter, whatever you call it); but I've actually seen some relevance for such a dynamic system at work, and I've started coding a system from the UI end first. The idea with that is a UI for visualizing & interacting with existing JavaScript entities, as well as creating new ones through direct manipulation. For example, dragging entities (representing objects, arrays, values, and functions) onto functions, which then create the resulting entity (which can then be interacted with in like manner).

[Dan] ALSO, I think such a system could answer Bret Victor's question for how to take his "Drawing Dynamic Visualizations" system, and "do the same thing for programming". I noticed that in that, all the transformations (or "steps") are created by actually letting the user do it through some visual interaction, and then recording the step on the side (and then the user can refine the values to be more calculated afterward). I see perhaps letting the user interact with code entities as I described, and then recording those steps (and then being able to refine them). So you could do a bunch of stuff, then say "all that stuff I just did is a function", and then replace concrete entities with arguments or other abstractions.

[Dan] Anyway, that's enough for now. Next, I think I need to scrape our conversation and list out our ideas in some form of documentation, as I said before that I would (I'll add it to my github project).

Feel free to share our conversation so far with others as you see fit.
