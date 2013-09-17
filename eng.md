# Around the World Wide Web in Eighty Minutes

> **A note from the editors:** Each month, a new author from the W3C will keep 
you informed on what we're up to—and how you can be a part of it. This month's 
column is from Richard Ishida, Internationalization Activity Lead at the W3C. — 
Ian Jacobs, Head of W3C Communications.

The year is 2013. London-based web designer Phileas Fogg IV has teamed up with
his internationalization friend Jean Passepartout III to circumnavigate the
globe. Unlike their famous forebears, Fogg and Passepartout will not be bounding
around the planet in hot air balloons and other risky contraptions. Rather, they
plan to explore the world’s typographic conventions from the comfort of Fogg’s
Soho loft. Adventurous? Yes! Risky? Not so much! The only tunnel they might
discover is carpal; the only port, 80; the only mysterious cable received, the
one for Fogg’s router. At least that is what they thought, before discovering
complexities that would baffle the intrepid of any age. And so they set off on
their first investigation…

## 1. IN WHICH MR. FOGG AND PARTY LEARN THAT MUCH PROGRESS HAS BEEN MADE

Fogg and Passepartout decide to travel around the world in the opposite
direction to their more famous namesakes, and set out for the United States of
America.

Not much to report here. Even though Spanish is on the ascendancy, there is
little difference from the typographic approaches that they are used to back in
London.

But wait, what’s this?

As they navigate their way through the American typographic scene, they come
across some very strange lettering.

![Cherokee][Cherokee]

“Ah! This is Cherokee,” exclaims Passepartout, “and it’s an interesting case!”

“Until quite recently, the Cherokee cultural heritage was dwindling because they 
had to use poor transliterations of Cherokee on computers, and had no standard, 
widely-compatible fonts. But after Cherokee syllables were added to Unicode, 
people developed Cherokee fonts and keyboards for a variety of devices–in 
particular, mobile devices. Now that people of the younger generation are able 
to talk to each other in Cherokee on Twitter, Facebook, and the web, the future 
looks much brighter.

“There are many languages around the world in a similar situation,” continues 
Passepartout, “and many other people need support for native typographic 
conventions that have long traditions, but can be very different from what we 
usually see in London.”

“I’ve heard of Unicode” muses Fogg, “though I can’t say I know much about it in 
detail.”

“Unicode,” explains Passepartout, “is a single set of characters that already 
covers pretty much all of the world’s writing needs. It not only enables you to 
write in Cherokee, or Cyrillic, or Cham, or Chakma, or even Cuneiform(!), but it 
allows you to mix languages in any of those scripts on the same page in a way 
that was almost impossible 25 years ago.”

Passepartout goes on to explain that a [recent survey by Google][1] of 6.5 
billion web pages shows that well over 60 percent of web pages around the world 
use Unicode’s UTF-8 character encoding–and if you include the pages using only 
ASCII characters (which are a subset of UTF-8), that figure rises to around 80 
percent!

![Unicode usage on web pages][Unicode]

*Unicode usage on web pages. (Mark Davis, Google Official Blog)*

“Remarkable!” replies Phileas. “This is indeed progress! What can I do as a web 
designer?”

“Adopt Unicode, of course,” explains Passepartout. “If you’re not using it 
already for all your content, you should ask yourself why.”

“But how do I do that?” cuts in Fogg.

“It’s actually pretty simple,” replies Passepartout. “You need to be sure to 
[declare the encoding of your page][2] as UTF-8. But don’t forget that you need 
to actually *save* your files as UTF-8 too! Oh, and ensure that all your 
back-end scripts and server settings don’t mess up the Unicode content! Don’t 
worry, the W3C has [some helpful material][3] to guide you.”

    <meta charset="utf-8"/>

    *A UTF-8 encoding declaration should appear at the beginning of every `<head>` element.*

Passepartout adds, “Fonts and encoding declarations are important, but proper 
typography requires so much more. And so… westward ho… to… the East….”

## 2. IN WHICH PASSEPARTOUT EXPLAINS THAT COLUMNS ARE NOT WHAT YOU MIGHT THINK IN EAST ASIA

Passing on from the Americas, Fogg and Passepartout point their browser toward 
Japan.

Here they find an abundance of strange looking characters, and marvel at the
fact that the Japanese “alphabet” has thousands of characters in it, each of
which is typically pronounced in two or three different ways, depending on the
context. It takes children six years of schooling to learn enough ideographic
characters to scrape by when reading a newspaper, and then there are also two
large syllabic alphabets to learn, too.

“And if you read Chinese,” interjects Passepartout, “you have to learn thousands 
more characters than in Japan.”

“But how can they represent all that in a computer?” asks Fogg.

“Well,” says Passepartout, “with Unicode the number of characters is no problem. 
Later I’ll tell you about ingenious keyboards that let you choose the one 
character you need out of thousands while you are typing. However, children (and 
sometimes adults) get help to read the characters they aren’t familiar with 
through special annotations called [‘ruby’][4]. These tell you how to pronounce 
the character they are associated with. They run alongside the base characters, 
without increasing line height, and have to wrap to the next line at the right 
place.”

![Ruby annotations over ideographic text][Ruby]

*Ruby annotations over ideographic text.*

Passepartout goes on to explain that although you can already see ruby on the
web, the W3C is currently in the process of [redefining how ruby should be
marked up][5] for the HTML5 specification. People like the markup model, but
there is a need for implementations if we’re to see it in the 5.0 version of
HTML. Unfortunately, even for a large market like Japan, getting browser
developers to implement these local requirements is often difficult, unless you
have volunteers who are able to provide patches. And, by the way, the CSS Ruby
styling specification still needs work, too. This will apply the necessary fine
typographic control over the placement of ruby in relation to the base text.
Basically, there’s a need for assistance to make these things happen.

But Fogg has become distracted.

“Look at this! The lines of text flow vertically, rather than horizontally. Is 
that possible on the web too?”

“It’s on its way,” answers Passepartout. “This and ruby were the top 
requirements arising from the [recent ebooks workshop][6] held in Tokyo. Printed 
novels are set vertically in Japanese. Developers of ebooks are unwilling to 
release readers unless they support vertical text, and so they have gone so far 
as to produce their own extensions while they wait for the W3C to finalize the 
finer details of how to do that in CSS. Once the CSS is ready, they’ll switch to 
the standard though.”

Passepartout goes on to show how vertical alignment of text also has
dependencies on font technologies, but Fogg is particularly impressed when he is
shown an example of vertical text in columns.

![Horizontal columns in Japanese text][columns]

*Horizontal columns in Japanese text.*

“This is extraordinary!” he says, “Look at that term ‘Universal Character Set.’ 
The characters are oriented differently, but not only that, it shows that the 
columns run right to left instead of top to bottom! Life must be hell if you are 
an Asian content developer… And you need to say ‘top’ and ‘bottom’ where we say 
‘left’ or ‘right.’ It must get confusing if you work on horizontal content too.”

“Well, most things should happen automatically once you set the CSS text 
direction to vertical,” Passepartout reassures him. “However, one thing for 
content developers around the world to look out for is that the CSS Working 
Group is going to be encouraging designers and developers to use the logical 
terms ‘start’ and ‘end,’ rather than fixed terms like ‘left’ and ‘right,’ for 
new content. That will make it much easier to design content that can be adapted, 
or to design styles that can be ported quickly to various languages.”

“It’s particularly useful for scripts like Arabic and Hebrew, where the basic 
text direction is right to left. But let’s wait until we get there before 
discussing that.”

“The key thing is that you are now beginning to see that there are some aspects 
of what you do that can have an impact when your web content or page design 
reaches an audience that lives beyond your back yard.”

“Yes, I see.” says Fogg. “I’d like to see some more of those things. Where to 
next?”

### Stay tuned for future Tales of Web Typography

3. IN WHICH PHILEAS FOGG AND PASSEPARTOUT VISIT THE FORM FIELDS OF SUMATRA
4. IN WHICH PASSEPARTOUT ASTOUNDS PHILEAS FOGG WITH NEWS ABOUT BURMESE RENDERING
5. IN WHICH PHILEAS FOGG EXAMINES THE SCRIPT OF THE HINDOO
6. IN WHICH PHILEAS FOGG CAN’T DECIDE WHETHER HE IS COMING OR GOING
7. SHOWING WHAT HAPPENED ON THE WAY THROUGH EUROPE
8. IN WHICH IT IS SHOWN THAT PHILEAS FOGG GAINED MUCH BY HIS TOUR AROUND THE 
WORLD, BUT MUCH IS YET TO BE DONE

[1]: http://googleblog.blogspot.co.uk/2012/02/unicode-over-60-percent-of-web.html
[2]: http://www.w3.org/International/questions/qa-html-encoding-declarations
[3]: http://www.w3.org/International/techniques/authoring-html#charset
[4]: http://www.w3.org/International/questions/qa-ruby
[5]: http://darobin.github.io/html-ruby/
[6]: https://www.w3.org/2013/06/ebooks/report.php

[Cherokee]: img/cherokee.png
[Unicode]: img/unicode.png
[Ruby]: img/ruby.png
[columns]: img/columns.png