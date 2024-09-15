# Blog ideas

## Surplusness equation

examining the relationship between "free space", "used space", and "total space", like if you're considering
making a disk 10% bigger but it gets you more than 10% more free space, because the used space stays the same;
but not specific to disks, it's a very general function (how wide are parking spaces? how wide is the shower? what's
the use in earning 5% more money? etc.)

Needs a better name.

If you have used U0 proportion of the total space (say 0.5), and the total space grows by factor G (say 2),
how much U1 of the new space have you used?

U1 = U0/G

If you have free F0 proportion of the total space (say 0.5), and the total space grows by factor G (say 2),
how much F1 of the new space have you used?

F1 = 1 - (1 - F0)/G

https://img.incoherency.co.uk/5576

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

## The tunnel locked room murder idea

Probably in 2 parts, first part with the clues and puzzle setup, second part with the conclusion

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

## Electric cars

I've become "EV-curious" lately.

It's because I saw a Citroen Ami on the road and thought what a cool little car. I looked it up and discovered that it
is electric! I didn't realise they made small and simple electric cars. I thought if you wanted an electric car you were
going to be saddled with something massive like a Tesla or an SUV.

It turns out the Ami can only do 30mph and only
go 46 miles on a charge, so it's not going to be any use to me, although it does mean in most of Europe
you can drive it without a licence. But the Ami piqued my interest and led to me looking at other cheap electric cars on
Autotrader. Check out this one:

https://img.incoherency.co.uk/5411

£2450? Where do I sign?!

I'd never heard of a Peugeot iOn before. It turns out there are 3 models almost identical, the Peugeot iOn, the
Mitsubishi i-MiEV, and the Citroen C-zero. They have a claimed range of 93 miles, and supposedly a "real-world" range
of 65 miles.

(How do they get away with claiming such an absurd overestimation of range?
If they're allowed to assume you're driving downhill with a tailwind, why not just say it's infinite?)

I know what you're thinking: 65 miles isn't very practical, I'm going to need a proper car as well.
But I'm not interested in using this as my only car. We have 2 cars already so that Emma can go out
when I'm at work, I'm
interested in a Peugeot iOn purely for commuting. I have a 60-mile round trip, up to 2 days a week,
so if the 65 miles real-world
range is reliably achievable then I won't have any problem with it. I can roll onto my drive with an easy 5 miles remaining,
and have it fully charge overnight.

Currently I commute in a Nissan Micra, but it has a lot of issues and I'll probably have to get rid of it soon. When
that time comes should I buy a Peugeot iOn? It's certainly tempting.

For just a bit more money you can get a Renault Zoe or Nissan Leaf of a similar age. Those are both much "better" cars, but
I've always been drawn to very small cars.

I think I pay about 14.8p/mile to drive the Micra (calculated as £1.50/litre at 46mpg) and would pay 6.5p/mile to drive
a Peugeot iOn (65 miles range out of 14.5 kWh "usable", and 29p/kWh).

Using https://petrolcalculator.co.uk/ev-vs-petrol-cost-per-mile/

So I'd be saving 14.8-6.5 = 8.3p/mile

If I were to commute twice a week (reality is less on average) then I'd drive it
120*52 = 6240 miles per year, so I'd save 8.3*6240 = £518/yr on fuel.

That's not enough saving to make it worth buying a cheap electric car compared to a cheap petrol car, still good though.

There have been a few occasions where I encountered road closures on my commute and had to go quite far out of my way.
I'm not thrilled by the idea of getting stranded halfway home just because of another surprise flood.

Also, just talk to anyone who owns an electric car. They'll probably tell you all about how far they can go on one charge,
where are the best places to charge, how good the charging network is getting, what a delightful experience they had with
one particular charger, how they only rarely encounter vandalised chargers, etc.; what they're really telling you is
"I spend a lot of brainpower worrying about charging my car". That won't be a problem in my case because I'd
plan to charge only at home, although I'm not thrilled by the idea of getting stranded halfway home just because
of a surprise road closure with a diversion that pushes me over 65 miles.
