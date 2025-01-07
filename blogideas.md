# Blog ideas

## Utility & Morality

* exchange rate between morality points and utility points (e.g. how much would I have to pay you to steal from an old lady if noone will ever find out?)
* diminishing marginal returns to utility, because of a maximum amount of utility points you can possibly make use of in one lifetime
* morality arbitrage, if you spend morality to earn utility which you then spend on others ("OK, Pay me to steal from the old lady and I'll donate all the money to charities", robbing Peter to pay Paul)

## Products vs Techniques

In the olden days people solved problems by knowing techniques. Now we solve problems by buying products.
What have we lost? What have we gained? Give examples.

* waterproof coats (wax it yourself, or buy one)
* house insulation (use random waste, or buy insulation)
* making gravy vs buying bisto

## The decline of the physical realm

How everything in the physical world is getting worse. Roads are always closed, restaurants make you piss
about with QR codes, bins only collected every 3 weeks, etc.

## Grbl vs LinuxCNC

Grbl:

* cheaper hardware
* higher step rate achievable (compared to parallel port)
* better UIs available
* no need for dedicated PC
* less bugs

LinuxCNC:

* more features (e.g. cutter compensation, movement coordinated with spindle rotation for rigid tapping)
* supports more complex motion systems

## 4 polite disagreements

A series of 8 very-short stories in which the main character disagrees with a decision made by someone else.

We explore every combination of (rude or polite disagreement), (they acquiesced or didn't), (it worked out well or didn't)

## The hero and the villain

It's a story about a series of events involving a hero and a villain, and the twist at the end is that they're the same
person. Even better if the hero's events and the villain's events are the *same* events but viewed from different perspectives
(and you only work this out at the end).

## Locality

Prefer to put configuration near where it is used. Prefer to put utility functions near where they are used. Maybe draw
an analogy with cache locality, where a single page of code is your "cache" and accessing information in that same page
is way faster than having to look elsewhere, and that's even if you already know where to look.

Obviously you need to make exceptions for things that genuinely need to be configured elsewhere, but if it doesn't need
to be configured elsewhere, please just configure it right by where you use it. It makes debugging and understanding
the code a lot easier.

Option 1:

    sub truncate {
        my ($self, $str, %opts) = @_;
        my $max_length = $opts{max_length} // $self->max_length // get_optional_config('max_length') // 15;
        return substr($str, 0, $max_length);
    }

Option 2:

    sub truncate {
        my ($self, $str) = @_;
        my $max_length = 15;
        return substr($str, 0, $max_length);
    }

In option 1 you have 3 different places to specify `max_length` (and you just know that `$self->max_length` is going to look
in more than one place as well...). Trying to divine the actual behaviour of `truncate()` from this code is very difficult.

In option 2 you know it truncates at 15 characters, no exceptions.

"No exceptions, no exceptions".

## Apartheid web

About how CAPTCHAs, anti-bot tactics, etc. are like apartheid for the web.

Also about how one day the AI will use these things against us ("anti-human tactics").

## Context

About how you take a different approach to programming depending on the surrounding "context". (What is a better word here?).

Is there a customer? What is the worst case if there are bugs? Is this just a one-off task to process some data? Will you be supervising it while it runs? Will you be able to ship bugfixes after it's deployed?

Lots of different approaches to quality and reliability.

Beginners are just happy if they can get the program to work (and rightly so!). And then "junior devs" (what's a better word here?) focus too much on "quality" at inappropriate times. "Senior devs" know when to spend time on quality, and when velocity is more important. When to "do the most immediately expedient thing".

## The 3 efforts

Effort before: "That sounds like a drag, I don't want to do it."

Effort during: "Man, this is hard work."

Effort after: "I need a lie down."

## Soft morality, hard morality

Some moral principles are universal (hard morality), and some
vary between different schools of thought (soft morality).

## Subconscious as homunculus

Modelling the subconscious mind as its own conscious mind that is able to observe
everything you observe, but its only output is to pop up thoughts into the conscious mind.

Intrusive thoughts about my subconscious working against me by popping up intrusive thoughts.

https://www.lesswrong.com/posts/xtuk9wkuSP6H7CcE2/ayn-rand-s-model-of-living-money-and-an-upside-of-burnout

Parallels between this "subconscious" and god.

Idea that if you don't work in the subsconsious's best interests, it will take matters into
its own hands. Important to cultivate a good relationship with the subconscious.

If you find some unanchored thought popping up telling you that you want something,
don't just bat it away. Bargain with it. "OK, we'll go and make another cup of tea soon,
let's just focus on the task for now". And then *actually do* go and get the cup of tea soon.
Your subsconscious needs to learn that it can trust you, and you need to learn that you can
trust it.

The Abramelin ritual for summoning your Holy Guardian Angel involves depriving yourself
of food, sex, and social interaction for up to 18 months, all while praying for a Holy
Guardian Angel. At the end your subconscious presents itself to you as
a hallucinated Holy Guardian Angel because of the extended abuse you've been giving it.

https://slatestarcodex.com/2020/06/01/book-review-origin-of-consciousness-in-the-breakdown-of-the-bicameral-mind/

Before the bronze age, the subconscious was basically running the entire show. The conscious
mind was too stupid to contribute. When the conscious mind was getting in the way, the
subconscious presented itself as the gods and told the conscious mind what to do.
But something changed at some point, the conscious mind became more powerful. Either the
conscious mind became powerful enough not to fall for simple hallucinations, or the
conscious mind started having a better relationship with the subconscious such that the
subconscious no longer felt the need to play tricks.

## The 50th hour

Imagine a project that will take 100 hours.

The 1st hour of the project creates 100% of the work that has been done.

The 100th hour completes 100% of the work that remains.

The 50th hour barely moves either the current state or the work remaining. That's why
you run out of steam in the middle.

C.f. https://incoherency.co.uk/blog/stories/free-space.html
