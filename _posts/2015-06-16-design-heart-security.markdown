---
layout: post
title:  "Design 💞 Security"
date:   2015-06-16
---

<p class="intro"><span class="dropcap">L</span>ast year, I went to Kiwicon for the first time. The most frequent question I was (and am) asked is why? As a designer, why did I go?</p>

To many people design and security are at the opposite ends of the tech spectrum. One deals with the deep complexities of how the machines and code work (or don't work). The other deals with how the very surface of the stack is presented to humans.

The reality is that they're two sides of the same coin. They require the same type of thinking. They're both about how people interact with systems, and about what motivates those people, for good or bad.

So, why don't we work more closely together? Why don't we learn from each other and use each other's knowledge, techniques, and tools?

One tool that's extremely popular in the design world is the persona. Personas are example user profiles. These include names, ages, backgrounds, motivations and aspirations, skills and frustrations. They are created by researching your user base and creating fictional composite profiles that reflect the range of your users.

Personas are used to help designers keep the needs and lives of the range of their users in mind when making decisions. This helps them to meet all their needs.

> One thing that's often missing in design personas is any mention of privacy or security concerns. What it would mean for that user to lose access to their account, their personal details, for their business to be compromised. Designers don't think like bad people often enough!

I'm going to break down 3 recent examples I've seen where design and security could've worked together better using personas as a tool.

##Example implementations:

###The sign up form redesign

I recently observed a team redesign their sign up forms. The designers spent a lot of time working with the marketing team to figure out what information needed to be collected, and the best way to collect that information without creating friction for the customer. Versions were iterated over and A/B tested for hours and hours. 

The resulting sign up form created a better experience for sign-up, but didn't make any improvement in the weak security design. 

The passwords had no minimum length, and no indication of strength to help users make smart decisions. No-one considered recommending a password management tool to the business customers of the site, despite the risks to their business. No-one talked to the security engineers.

The designers had created personas - but none of the personas mentioned security or privacy requirements. There were no personas for the bad guys. Nothing to help them think like the bad guys and work to thwart them. Here, security could help designers build the right personas to reduce risk to users.

###The Kiwicon talk

People outside the security community think about being compromised as an 'if'.

The first thing you learn when you first start talking to the security community is that everything is fucked. Everything has holes. Everything is compromised. They don't tell you this to terrify you; it's just the baseline truth they work from.

Once you're working from that baseline truth, it's not a matter of if you'll be compromised, but when.

There's a fundamental difference in the way you approach the problem once you're thinking 'when'. When you're in 'if' mode, you tend to think about it as being something you can stop. You think you can fix all the holes if you just build big enough (metaphorical) walls.

Once you're in 'when' mode, you have to start being strategic. At Kiwicon, one of the speakers discussed this - understanding not only what you have to protect, but who you have to protect it from, and that they're not an amorphous blob of "EV1L HACK3RS".

He discussed understanding the difference in motivation and cost for a pro vs a script kiddie. He discussed the tools available to each of them, and what those tools enabled them to do. He talked about how much they time they were willing to spend, given that time equates to money.

Essentially, he was talking about building attacker personas. These personas could then be used to help make strategic decisions about which parts of the systems to focus on defending. This helps to ensure the most effective defences are built with the limited resources available.

Like interface design, once you understand who you're designing security for, it's a lot easier to place obstacles in their way. Unlike interface design, security design doesn't have a well-established practice for this. Here, designers could help security teams build personas to enable more effective defence.

###The terrible product descended from CERN

I recently stumbled across product: Error Pages from Statuspage.io. The product allows you to enter your brand colours and some details, and gives you a downloadable HTML file for a 404, 503, and maintenance page.

On the surface, it seems like a non-awful idea. Package up a nice, easy way to get a non-ugly error page. Users expect something a bit prettier these days. Everyone has them, and if you don't, you'll look bad.

Take a second glance, and it's a terrible idea from both a design and a security perspective - something security and design personas would have shown in an instant.

For most applications, the majority of your end-users will be non-technical. Your design personas would likely highlight that, when something goes wrong, they feel comforted by professional presentation and clear directions. They don't need or understand technical jargon.

They're not interested in the error code on the page. They're not really interested in your server issues or if you can't find the page. This is superfluous information. They want to know what to do next.

When you're trying to break into someone else's site, information is gold. The security personas would likely have highlighted that they're interested in knowing where and when things are going wrong, because that's somewhere they can start digging.

This is a perfect example of cargo-cult thinking. There is no good reason to _ever_ show an end-user an HTTP status code on a production site. You never, ever want to give an attacker more information than you need to.

But, the early browsers at CERN dumped them there for machines to read. They were never intended for our users to read. But, people didn't understand the specs, and decades later, and in the intervening years, they've become beautiful and on-brand.

Everyone makes them because everyone always has. But your end users don't want or need the error codes. You don't want to give them to your attackers. But here they are, in this product, and in pages all over the web.

Nobody involved in that product, from designers to security folks, sat down and thought about a persona-based design for this: giving the people who need information the right information at the right time, and keeping the stuff we don't want to share out of reach.

<hr>

The scary thing is that the two disciplines are deeply interlinked. Bad design, especially bad UX, can cause bad security - like the banking apps that don't let you paste your password in from your password manager, or don't let you use your browser autocomplete. And bad security can definitely result in a bad user experience. One of the biggest problems in security is the squishy humans, as [Laura Bell](http://www.twitter.com/lady_nerd) would say, and that's a problem that we need to work together to solve.

We don't talk enough about how design and security can help each other. 

We should talk.