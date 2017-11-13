*On 5 November 2017, A skype call took place between Dan, Joel, Pavel, and Pavol, where we discussed our similar viewpoints & goals regarding a reinvention of software via a universal software tool. We also discussed how we should manage further collaboration of a related project(s), and the broader future of this collaboration as a whole.*

*Below are some snippets of an email exchange we had afterward:*

----

Dan Cook
<br/>6 November 2017

Something interesting I observed:

We talked about distilling a high-level goal(s) / purpose, and keeping that separate from the "how" so that we don't lose sight of our real purpose / what we want to achieve.

However, when Pavol described his project, I was slapped in the face with the realization that there is a certain means or mechanism that seems to be inescapably present in almost every single project or effort related to [(we need to come up with a phrase to refer to what we & others are trying to achieve)]. And that thing is an explicit structural representation consisting of a freeform graph (or tree) of data (I called this "Everything as Objects" Concepts.md). I think there's a clear reason for that, but I won't get into that now.

(One thing I like about what Pavol described is how such a structure can be mapped to other representations, which I think is also a key idea, whether it be done directly on the fly or via a compiler or some other way).

To the point: That's enough to convince me that we do have a specific "thing" that:
(1) Is practically a prerequisite for any of this kind of software revolution to happen.
(2) Is a major short-cut for us getting anywhere, as something that we can focus on very tightly (apart from all our other / wider ideas & goals) to get somewhere fast.
(3) Once implemented, would be a powerful way for us to explore a broader range of (other / the rest of our) ideas.

I think that we could take everything about this collaboration, and apply the same process just around enabling the general use of a general structural representation / tree (maybe we can come up with a name for that "thing"). Not to abandon the larger set of ideas etc., but I think we might do well to zero-in on this one thing in particular, perhaps in parallel with the larger / wider spectrum of what we might do with it.

----

Dan Cook
<br/>6 November 2017

I just realized that I may have made a major assumption that what is inevitable is not just the "structural substrate", but also that programs themselves are composed of it, which necessarily requires an interpreter (or compiler), and thus also requires some heavy-duty circular bootstrapping ... and that perhaps all those things might not necessarily be built into how everyone else sees this going, or even if we do all agree on that, that we may have very different approaches for it all.

Anyway, here's my attempt to explain what & why:

I think that the kind of "structural substrate" (or whatever various things we've identified it as) is like "the arch" of computing & software, since it all boils down to structural representations of information, and this "substrate" is about making it explicit and direct. ("The arch" versus "bricks". Alan Kay compares the Great Pyramids of Egypt, which took mammoth efforts of brute force and an impossible amount of materials, to Cathedrals which are "mostly empty space"). And to expand it further, since software is the tool for making software, we should be using "arches" to make "arches". So perhaps the real arch is not just a structural representation ("substrate"), but one which not only makes it easy to create & modify other things in a structural way, but which also is capable of defining & modifying itself.

Therefore, I don't think that it's good enough just for software to use a structural substrate, but it must also be composed of that substrate itself; Without this, software creation & manipulate does not change from conventional means. I think the structure of the program should also be accessible at runtime if we want to allow a program to (structurally) modify itself or generate new code on the fly. (For me, the real punch line is putting this power in the user's hands; but I won't elaborate on that here).  

This calls for an interpreter which should also be composed of the same structure ("bootstrapped") if we want to be able to modify that fluidly; and if we want to be able to do so on the-fly (at runtime), then this structure should be visible to itself at runtime. The direction I see this going is a program that acts as a tool for building & modifying a "structural substrate", and who's code is composed of the same substrate which can be exposed to the same editing, and of which the interpreter that makes it all work is also contained within the substrate and exposed for inspection and editing. (This might start without a UI, but ultimately there'd be a UI for it, which is made up of components that are editable by itself in the same manner).

I think that such a tool could be used to design any program in any language (ideally whatever is the most suitable per case) (and the same for UI manipulation of it), even to the extent of using it to create a different tool from within. And as for using it as a tool to create other software, you can either manipulate it into the proper state and say "there it is", or compile the structural form into another language or runtime (possibly also bringing the interpreter along with it).

Anyway, such an interpreter is not complicated because it just needs to be able to do all the operations involved with modifying the structural substrate: get, set, lookup, delete, and then maybe fundamental utils for programming logic. I think that given the right focus, we could get something like that working in a (relatively) short amount of time.

So I realize that that might just be my particular vision for one (perhaps of many) ways of achieving the kind of change we seek; but I do think that it (or something like it) could do the job, and could be the kind of thing that could be changed from within to explore other ways of working (e.g. using Just-In-Time compilation instead of an interpreter). I also think that for this reason, it makes sense to start with something easy to implement it in (e.g. a dynamic language like JavaScript already provides such a substrate), and then the whole thing could be cross-compiled to another language or (lower-level) environment; and even that could be done using the tool itself. So I think whatever the fastest way to achieve this (...full-circular-bootstrapping?...) is the way that we should pursue.

I really do think this (or a similar) approach could bring about any other tool that's even half-similar, and make the task of doing so much better.

But, what do you all think? Does anyone have a different idea, or disagree?

----

Joel Jakubovic
<br/>7 November 2017

What you're describing sounds awfully like the COLAs paper. Have you read it? http://www.vpri.org/pdf/rn2006001a_colaswp.pdf

----

Dan Cook
<br/>7 November 2017

I have read the COLA papers (and seen videos on YouTube about it), and I think what I described shares some principles of fluidity of and between representations. However, I think he achieves it with parsing and grammars (PEGs), and I am talking about using an object model that keeps the structure explicit and clear such that it would be easy to modify or transform directly; but no parsing is involved. I do think that his stays very textually oriented, while the 4 of us are talking about explicit structure and objects.

Though I will say that I think COLA & OROM are a must read for anyone doing anything similar, so thanks

*(TODO: Add links to the above mentioned resources)*

----

Pavel Bažant
<br/>7 November 2017

Here is the rant against flat text I posted at FoNC: https://www.mail-archive.com/fonc@vpri.org/msg04206.html

It is sort of vague and my viewpoint has shifted slightly since then. I started the discussion in a clumsy and impolite way, but I still insist on the core ideas.

----

Dan Cook
<br/>7 November 2017

I enjoyed reading that, and the array of insights you had to support your perspective.

Maybe it would be a good idea at some point to also gather supporting arguments & examples for our concepts & goals.

It looks like we all are essentially looking to the create the same kind thing, which at the very least is promoting a common structure to represent everything, and a way to edit or manipulate such structures directly. And if we want code to be runnable, we necessarily need some sort of compiler or interpreter or translator or mapper of some sort.

I can see that perhaps we do have different approaches in mind:
* Create (or find) support for the structure, create an editor for it, re-create the editor from the structure, and some sort of compiler or interpreter (so that structured code can do anything)
* Create (or find) support for the structure, create an interpreter (so that the structured code can do anything), re-create the interpreter from the structure, and then some sort of editor.

(Am I inferring that properly?)

Essentially the same thing, but a different order.

And I suppose another step somewhere in there would be a way to map that structure to other representations (e.g. a non-structured one, such as machine code or linear data in memory), similar to what Pavol mentioned on our call, and to what Ian Piumarta describes in his COLA papers / videos; though I wonder if that's not fundamentally different from a compiler (well, in this context anyway).

As I said before, we should be careful not to fall into a rut of deciding "the way" to do things; but it seems to me that this particular path is inescapable and perhaps thus fundamental, so maybe it would make sense to lay it out like I've done (or in some other way?) and pursue it -- and whether we approach that from different approaches is fine. I think either way it will run together at some point, or at least provide different but similar outcomes that could probably bootstrap each other.

Does this sound like a good approach / plan? Or are there any other concerns or does anyone see it any differently?

----

Dan Cook
<br/>7 November 2017

For a little bit, I almost forgot that we are only 4 of 10+ other people in the collaboration and that we want it to grow beyond the specific common idea(s) that we share. But since we DO have something in common to pursue (I assume -- I've been speaking faster than everyone can respond), do we (also) want to have a separate smaller collaboration (or at this point, perhaps "project" is a better word)? As for moving to C2 wiki, I think we are talking about moving the larger "collaboration". But I wonder if that's better suited to a wider-scoped collaboration, or more of a specific focus.

Even if we do collaborate on a specific project, I think we should still keep it pretty tied into the larger collaboration.

All of this is probably something to talk more about another time.

----

Pavel Bažant
<br/>8 November 2017

I think that a sub-collaboration of us 4 who are more closely tuned to a common theme would make sense. IMHO there are several things we could/should set up:

1) A public forum/mailing list that will serve the kind of people who followed the FoNC mailing list.
2) A public compendium of approaches to powerful yet humane programming interfaces/environments (current as well as historic ones: MPS, Boxer, Smalltalk, Oberon, Sketchpad, Genera, ...) and related themes. I would try to avoid being too Xerox PARC-centric.
3) A not necessarily public communication channel for us 4 (e-mail + occasional Skype calls work fine for now).
4) A not necessarily public list of interesting resources for us 4.

Occasionally, the sub-collaboration could create some structured outputs that would be shared publicly when they are more streamlined.

----

Joel Jakubovic
<br/>8 November 2017

I've just done some work over the past couple days on a few lines of
JavaScript to persist work done in the browser's console. You folks may be
interested as I intend this to be a qualitative leap in the tools to get
my project off the ground. (a leap for me, at least, but I'm only putting
this out because it's a simple step that *could* have a lotta impact. Let
me know)

https://programmingmadecomplicated.wordpress.com/2017/11/08/1-basic-persistence/

May I just say, I thought we said we could discuss stuff on Issues. I have
a bit of an aversion to whispering around in our little circle of 4,
waiting to release published discussions in a polished form. People should
be able to see the conversations, the ideas going back and forth. Surely?

----

Dan Cook
<br/>8 November 2017

I agree that I've been breaking the rules. I'll transfer these emails over somehow, and going forward I'll make content public and then maybe just email to let everyone know.

I don't know if we decided on opening issues for *all* discussion, but more for action items (albeit *with* discussion). Either way, we can try either docs or issues as we see fit, and see how that works. I am willing to transfer one to the other if it works better one way. (I do like issues as a TODO-with-discussion, though)

----

Pavel Bažant
<br/>9 November 2017

Ok, the sub-collaboration may be public, but it still makes sense IMHO to make it separate with separate goals etc.

----

Dan Cook
<br/>9 November 2017

I think that sounds good, though maybe keeping the general ideas and discussion in the main collaboration (as a place to talk about various ideas, projects, and worthwhile end-goals), and then creating something else that is more focused as one of the specific projects (e.g. the thing we want to make together).

Maybe we can discuss this on a call some time to decide exactly how & what to split.

----

Pavol Privitzer
<br/>9 November 2017

Excellent points you have spotted!

And, IMHO, it is just a slight tap onto what I see is really going on here.

I call this system for idea (re-)presentation „IdeaTree“. Of course, it is yet-to-be-realized system + language + substrate, which is based on and made from itself (more on the S+L+S viewpoints later). We can look at it as a universal meaning bootstrapping system; universal in a very similar way as “universal Turing machine”, but for idea (information with meaning) capturing purpose; but with practicality/daily usefulness in mind, not just a mere mathematical minimum, as is e.g., a minimal definition of a Turing machine or lambda calculus. Trying to find THE minimum is good for pure mathematics, or extreme low-levels of physics, but not as useful for higher levels of information structure (re-)presentation, or for representation/simulation of evolving (eko-)systems (e.g., biological ones; even their substrates are not the minimal ones, they are all multi-level). It has a lot to do with how the right hemisphere works, or how “intuition” works, where instead of making serial proof (with many trivially minimal steps), the information structure can allow “jumps right into conclusions” and the energy can be saved for other useful stuff. Intuition is based on lots of clever memory with a little of computation, not on basic principles and lots of computation step by step (do not make me wrong that I want to emphasize intuition over logic; my point here is that intuition is undermined and we need to re-present it as well as logic; I am for hybrids in general).
 
I am really pleased with your understanding of this. It is really rare (yet! after realizing it, it will be obvious and “easy”).
I am lately (about 5 years) rather reluctant to share these ideas too much, because I have not very positive attitude for big companies that are sucking great ideas and they are making money from them without a fair balance with the source of the ideas. That is why I speak about money more then I would like.
From this technology, an enormous amount of money can be made. I don’t know how to “protect” it from being “lost” in favor of those who already have lots of money.
Maybe, you do not see this part in the open source. I would like to live in a really open world, yet still I see a lot of abuse of the openness and “naïve” individuals.
I feel the need to defend somehow against the imbalance. At the same time, after I saw your understanding, I feel the urge, we should/must work together on this to happen.
 
Only I do not know how to set up an immune system to let us become a strong group in all respects, including the money dimension, before some other already strong group/company could take over us. To clarify my concerns more, I do not think the IdeaTree-like system is a “very small” system. It will grow enormously with a core that can be fully comprehended by an individual, but the overall system to grow will require several man-years of effort. I consider the needed effort as an “activation energy” that is needed to make it. The activation energy is the weak spot where companies can overpower almost anybody (basically they buy the people or the little company) with a great idea which is not yet fully grown but which still needs considerable time/money to be fully grown.
I am trying to figure out, how to create a new kind of company that can grow these ideas fully without being bought by a large company/investment group during the growing process (i.e., a full company bootstrap from “zero investment”). After the company is “fully grown” I have no problem to “release anything to the full openness”, because there is little chance for unfairness at the point.
 
If I sum up the idea, my biggest question now is how to “grow a great tree without letting it to be eaten by an animal during its early years”?
 
What do you think?
