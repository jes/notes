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
