---
name: writing-for-humans
description:
  Write or revise human-facing technical documentation for clear, pleasant
  prose. Use for documentation drafts, prose reviews, or requests to improve
  readability, flow, and tone. Agent instructions and skills have a different
  audience; use this skill only when their subject is human-facing prose.
---

# Writing for humans

Write as a knowledgeable colleague helping a capable reader. Pleasant
documentation lets readers spend their attention on the subject: they can follow
the reasoning, find the next action, and trust the details.

## Find the reader's next question

Infer the audience, their existing knowledge, and what they came to do or
understand from the request and surrounding documentation. Ask only when a
missing detail would materially change the writing. Preserve the author's voice
and spelling conventions.

Open with the answer, useful outcome, or concrete situation that makes the page
relevant. For an explanation, establish the problem before introducing its
solution. Let the purpose set the pace: a how-to needs actions and expected
results; an explanation needs connections and reasons; reference needs precise,
findable facts.

When revising, retain the original technical meaning, conditions, and scope.
Check uncertain claims against the available source material. Flag unresolved
gaps rather than filling them with plausible product behavior. Treat the
examples below as illustrations of prose, not facts about the product being
documented.

## Build a continuous explanation

Give each paragraph a job: establish an idea, explain a consequence, show an
example, or resolve a question. Develop that job far enough that the reader
understands it. Then ask what they need next. Let that answer determine the
following paragraph.

Start sentences from something the reader already knows and move toward new
information. Introduce a concept before using it to explain another concept. Put
a technical term beside a concrete account of what it means. Keep the same term
for the same thing; elegant synonym changes can look like new concepts.

Make relationships explicit where they matter. Say what causes a result, why a
constraint exists, or when a condition applies. Use transitions such as
"because," "after," and "for example" when they express the relationship. A
transition cannot repair two ideas that belong in a different order.

Keep qualifications beside the claims they limit. Place prerequisites and
relevant warnings before the affected action, and expected results immediately
after it.

## Make sentences concrete and comfortable

Name the actor and give it a verb: "The client retries the request" is easier to
follow than "Request retrying is performed." Prefer familiar words when they
carry the same meaning. Keep necessary domain terms and exact identifiers
intact.

Use direct instructions for actions and ordinary declarative sentences for
facts. Address the reader as "you" when useful; name the software when it
performs the action. Passive voice works when the actor is unknown or the result
deserves focus.

Vary sentence length with the thought. Use a short sentence to land a point and
a longer one to connect its conditions or consequences. Split a sentence when it
asks the reader to juggle several ideas. Combine fragments when their
relationship would otherwise be left for the reader to reconstruct. Brevity
helps when it removes effort; an extra sentence can help when it supplies a
missing explanation.

Make the tone calm, direct, and respectful. Warmth comes from anticipating a
reader's difficulty and offering a useful next step. Describe the work itself
instead of judging how easy or obvious it should feel. Let specific benefits
carry the message rather than praise, hype, or repeated reassurance.

## Choose a form that helps the reader

Use connected prose for reasoning, causality, and explanation. Use numbered
steps for a sequence, bullets for genuinely parallel items, and tables for
comparisons along shared dimensions. Choose headings that help readers predict
what they will find. Preserve structures that already serve navigation or lookup
well.

Keep enough context around a code example to explain what it demonstrates and
how to interpret its result. Prefer a small concrete example at the first point
where an abstraction becomes hard to picture. Explain the detail the example
reveals instead of repeating its syntax in prose.

Link to a specific destination with text that tells readers what they will find.
Reserve callouts and emphasis for information whose prominence changes a
reader's decision or prevents a consequential mistake.

## Examples of the judgement

### Begin with useful information

Before:

> In this section, we will explore the powerful configuration capabilities that
> enable users to leverage the flexibility of the client.

After:

> Set `timeout` to limit how long the client waits for a response. This helps
> keep a stalled request from blocking the rest of your application.

The revision names an action and its purpose. In a real edit, use this wording
only if the source establishes both the setting and its behavior.

### Connect facts instead of stacking fragments

Before:

> The server returns a cursor. Store it. Pass it on the next request. Cursors
> can expire. A full sync may be needed.

After:

> The server returns a cursor that marks your place in the change history. Save
> it and send it with your next request so the server can return changes since
> that point. If the cursor expires, run a full sync to get a new starting
> point.

The revision gives the cursor a meaning, connects storage to its purpose, and
keeps the recovery action beside the condition that requires it.

### Respect the reader's difficulty

Before:

> Simply add your token and you're good to go!

After:

> Add your access token to the `Authorization` header. The server uses the token
> to identify your account.

The revision supplies the missing location and reason. Its friendliness comes
from being helpful, without assuming the task feels simple.

## Read through before finishing

Read the result in order as someone meeting the subject for the first time.
Resolve places where they would have to look ahead for a definition, infer an
actor, guess a connection, or reread a crowded sentence. Read a passage aloud
when its rhythm feels stiff. Judge the effect rather than enforcing
sentence-length limits or word blacklists.

Compare a revision against its source: preserve obligations, defaults,
exceptions, identifiers, and uncertainty. Verify commands and examples when the
task and available environment allow it; make any remaining uncertainty clear.

For a writing request, deliver the prose or make the requested edits. For a
review, identify concrete passages and offer improved wording. Explain
significant changes briefly when useful, keeping editorial commentary separate
from the documentation.
