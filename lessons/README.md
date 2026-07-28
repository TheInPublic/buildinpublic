# What Building Kitwork Has Taught Me

> **“I’m not a great programmer, so I’m trying to make programming simpler.”**

I started programming in 2015.

Since then, I have left university, worked at a startup in Đà Nẵng, returned to my hometown, built websites for clients, maintained systems that quietly run every day, and started more projects than I can count.

Some ideas survived.

Many did not.

Today, I build from Da Nang, a city in central Vietnam. I do not have a large team, outside funding, or a famous name behind me. Most of the time, it is simply me, my computer, my family responsibilities, and the belief that software can be built in a smaller and more understandable way.

Kitwork grew from that belief.

It is an open-source runtime written in Go, with its own language, compiler, bytecode engine, and virtual machine. But Kitwork is not only a technical project.

It is the result of a question I have been asking myself for years:

**How much can one independent builder create without becoming dependent on increasingly complex infrastructure?**

I still do not have the complete answer.

These are some of the things I have learned while searching for it.

---

## Simplicity Is Not the Absence of Ambition

For a long time, I thought ambitious software had to look complicated.

It needed more services, more layers, more frameworks, more infrastructure, and more terminology. Complexity made a project appear serious.

Over time, I began to see the cost.

Every new layer has to be understood. Every dependency has to be maintained. Every service introduces another place where the system can fail. For a small team, and especially for a solo builder, unnecessary complexity quietly consumes the time that should have been spent improving the product.

Kitwork is ambitious, but its ambition points in the opposite direction.

I want to discover how much software can be built inside one understandable runtime.

**One process. Many isolated systems.**

Simplicity does not mean building less.

Sometimes it means making more possible with fewer moving parts.

---

## Complexity Must Earn Its Place

I am not against complex engineering.

A compiler is complex. A virtual machine is complex. Scheduling, isolation, concurrency, databases, and distributed systems all contain real complexity.

But complexity should exist because the problem requires it, not because the builder wants the architecture to look impressive.

Before adding something to Kitwork, I try to ask:

* Does the current system have a real limitation?
* Has that limitation appeared in actual usage?
* Is this the smallest solution that addresses it?
* Will I still understand and maintain it years from now?

I do not always get these decisions right.

But I have learned that removing an unnecessary abstraction can be more valuable than creating a clever one.

---

## Real Systems Teach More Than Imaginary Scale

It is easy to design for millions of users who do not exist.

It is harder to operate software for a small number of real users who expect it to work every day.

Real systems reveal problems that architecture diagrams cannot:

A failed request.
A slow query.
A broken deployment.
A tenant that behaves differently from every other tenant.
A feature that sounded useful but nobody actually uses.

Many of my most important lessons did not come from large-scale systems. They came from keeping ordinary websites and services running reliably.

A small production system is still a real system.

Real usage matters more than imaginary scale.

---

## Performance Matters When It Creates Freedom

I enjoy benchmarks.

Watching a runtime complete millions of operations or serve requests with very little memory is satisfying. But performance should be more than a number shared online.

Efficiency can reduce infrastructure costs. It can allow one server to handle more work. It can make deployment simpler and give an independent builder more room to survive.

For a large company, inefficient infrastructure may mean a larger cloud bill.

For an independent developer, it may determine whether a product is financially possible at all.

Performance is valuable when it helps us do more with less.

It should create freedom, not merely win comparisons.

---

## Own the Core, Borrow the Ordinary

Building independently does not mean writing everything from scratch.

There are many problems that already have good solutions: email delivery, authentication, payments, standard interface components, and common infrastructure tools.

Rebuilding all of them can become another form of procrastination.

But the part that makes a project different should remain understandable and controllable.

For Kitwork, that means the runtime model, language, compiler, virtual machine, isolation, and execution architecture.

I want to own the ideas that make Kitwork Kitwork.

Everything else should be evaluated honestly:

Does building this create meaningful value, or am I only rebuilding it because I can?

---

## Dependencies Are Long-Term Relationships

A dependency can save days or months of work.

It can also become part of the architecture for many years.

Libraries change direction. Projects become unmaintained. APIs disappear. Licensing changes. A small convenience can slowly become something the entire system depends on.

This does not mean dependencies are bad.

It means they are decisions, not free gifts.

Every dependency should answer a simple question:

**Does the value it provides justify the control we give away?**

Sometimes the answer is clearly yes.

Sometimes writing a small internal implementation is the more sustainable choice.

The important thing is to make the decision consciously.

---

## Building for the Future Should Not Destroy the Present

Developers often design systems for the company they hope to become.

They create infrastructure for future teams, future traffic, future products, and future problems. Meanwhile, the product in front of them becomes harder to ship.

I have made this mistake many times.

Planning ahead is useful. But the future should not be allowed to make the present system impossible to understand.

The best architecture is not necessarily the one capable of handling every imagined scenario.

It is the one that solves today’s problem while leaving a clear path forward.

---

## Shipping Creates Clarity

Ideas feel complete while they remain inside my head.

Publishing them changes that.

The moment I try to explain Kitwork to another person, write documentation, release a repository, or share an architectural decision, I discover the unclear parts.

Building in public is not only marketing.

It is a way of thinking.

Public work forces an idea to become understandable outside its creator’s mind. It allows other people to question assumptions that have quietly become invisible to me.

I do not need to pretend the work is finished.

I only need to be honest about where it is.

---

## You Do Not Need a Large Audience to Share

I am not naturally good at marketing myself.

For years, I believed I should wait until I had achieved something significant before talking about my work. I thought people would only care after Kitwork became successful.

But an audience does not always come before the journey.

Sometimes it grows because the journey is shared.

Writing about unfinished work has allowed me to meet people I would never have reached through code alone. It has also helped me understand why I am building in the first place.

You do not need thousands of followers to build in public.

You need something honest to say and the courage to publish it.

---

## Writing Preserves What Code Cannot

Code records what a system does.

It rarely records why the system exists.

A repository cannot fully explain the doubt behind a decision, the years that shaped an idea, the alternatives that were abandoned, or the personal meaning of continuing to build from a small city.

That is why I write.

I write about runtime design, performance, independence, failed ideas, and building in public. Not because I have completed the journey, but because I do not want the journey to disappear inside commit histories.

Writing helps me connect years that might otherwise feel unrelated.

Sometimes I am not writing to be read.

I am writing to hear myself more clearly.

---

## Not Every Project Must Become a Company

I have created many projects, purchased many domains, and explored many ideas.

Some may become businesses.

Some may become open-source tools.

Some may become articles, experiments, or components that later find a place inside something else.

Some will quietly disappear.

Not every project needs to become a startup to be valuable.

A project may teach a new technical idea, reveal a market that does not exist, introduce me to someone important, or help me understand what I do not want to build.

Sometimes the result of a project is not a company.

Sometimes the result is a better builder.

---

## Stopping Is Also Part of Building

Independent builders often become emotionally attached to the time already invested in an idea.

We continue because stopping would make those months or years feel wasted.

But previous effort is not always a reason to invest more effort.

An idea may be technically interesting but unnecessary. It may solve a problem people do not feel strongly enough. It may belong to an earlier version of the builder who created it.

Letting go does not erase the work.

The knowledge remains. The code may be reused. The failed assumptions become part of the next decision.

Stopping an idea can be an act of honesty rather than defeat.

---

## Small and Sustainable Is a Real Form of Success

The technology industry celebrates large outcomes.

Millions of users.
Large funding rounds.
Fast-growing teams.
Global companies.

Those things may be meaningful, but they are not the only definition of success.

A small product that earns enough to support its creator, serves a real group of people, and remains understandable can already be extraordinary.

I do not need Kitwork to replace every cloud platform.

I want it to become useful to people who value ownership, portability, efficiency, and a simpler way to build.

A small honest system is better than a large imaginary one.

---

## Independence Does Not Mean Isolation

I care deeply about technical independence.

I want to understand the systems I operate. I want the freedom to move between providers, control my data, maintain my core technology, and avoid unnecessary lock-in.

But independence does not mean refusing all help.

Open source exists because people build on the work of others. Communities help ideas grow. Feedback reveals blind spots. Tools created by other builders make my own work possible.

The goal is not to build alone at all costs.

The goal is to choose dependencies, partnerships, and tools without losing the ability to continue on my own terms.

---

## Trends Should Not Replace the Mission

Technology moves quickly.

Cloud, blockchain, Web3, AI, agents, and new frameworks repeatedly promise to redefine software. Some changes are genuinely important. Others disappear after a brief period of attention.

Kitwork may support AI agents and new kinds of applications in the future.

But it should not change its identity every time a new term becomes popular.

The deeper mission remains the same:

**Build software systems that are smaller, more understandable, more portable, and more independent.**

Trends may influence what Kitwork can do.

They should not decide why it exists.

---

## Family Is Not an Interruption

For a long time, I imagined that serious builders had to put life on hold.

Work first. Success first. Everything else later.

But products can take many years to become meaningful. Some never reach the destination we imagined for them.

Life cannot wait for the product to succeed.

Being a husband, a father, and a member of a family does not make me less committed to building. These responsibilities give the work a reason to exist beyond technical ambition.

I want to build something meaningful.

But I also want to be present while building it.

---

## Continue When Nobody Is Watching

There are long periods when an independent project receives almost no attention.

No new users.
No stars.
No comments.
No clear sign that the world needs what you are creating.

These periods are difficult because attention provides energy.

But they are also revealing.

They force me to ask whether I care about the work itself or only about the identity that comes from being seen doing it.

External recognition matters. We are human, and encouragement helps.

But the work must eventually be supported by something deeper: curiosity, discipline, responsibility, and belief in the question being explored.

---

## Kitwork Is Still an Unfinished Question

Kitwork is not a success story.

It is still being designed, rewritten, benchmarked, documented, and questioned. Some of its current ideas may turn out to be wrong. Its direction may change many more times.

But Kitwork already represents something important to me.

It represents more than ten years of trying to understand software in my own way.

It represents the decision to stop waiting for permission.

It represents an independent developer in Da Nang attempting to build infrastructure from first principles, even when the goal appears too large for one person.

Perhaps Kitwork will become a widely used runtime.

Perhaps it will remain a small open-source project that influences the next thing I build.

I cannot know yet.

For now, I will continue doing what I have always done:

Building.
Measuring.
Simplifying.
Writing.
Learning.
And trying again.

---

> **Build what you can understand.
> Own what makes you different.
> Let complexity earn its place.
> Make more possible with less.
> Share the unfinished journey honestly.
> And do not postpone your life while waiting for the work to succeed.**

*Written by Huỳnh Nhân Quốc, an independent Go developer building Kitwork from Da Nang, Vietnam.*
