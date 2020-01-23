# Writing Release Notes

Here's some basic guidelines for how we write our release notes and what we include in them. `yarn draft-release` is a great starting point, but not a final version.

## Anatomy of a Release Note 👩🏼‍⚕️

A release note has three (or four) parts.

```
[Tag] Description of work or change - #{issue_number}
```

If it was done by an external contributor, we'll add an extra part — a thank you!

```
[Tag] Description of work or change - #{issue_number}. Thanks @{contributor_username}!
```

## Writing Style 🖊️ 

These mostly apply to writing the release note description itself.

### User Facing

We don't include release notes that don't impact the user's experience using Desktop. For example, we wouldn't include a release not about fixing our Appveyor CI config or upgrading Electron. We'll make exceptions for security vulnerability fixes, especially if they're high profile.

### User Impact

We describe our work in terms of impact on our users, not technical process. How does this work change the user's workflow or experience? What does it help them do?

For example, we might say:

```
[Fixed] Keep PR badge on top of progress bar - #8622
```

but **not**:

```
[Fixed] Increase z-index of the progress bar PR badge - #8622
```

### Present Tense

We can never remember if we're supposed to active, present, or past tense, but I think we're mostly using present.

For example:

```
[Fixed] Fix arrow key navigation of Changes and History lists - #6845
```

but **not** this

```
[Added] Adding integration for Xcode as external editor - #8255
```

## Tags 🛄

We use four different tags to organize our release notes: [New], [Added], [Fixed], [Improved], [Removed]. Here's when to use which one.

These aren't hard and fast rules or categories, 🙃 so utilize with your own judgment and nuance.

### [New]

[New] is usually reserved for our shiniest features. The note itself might be short and very high level and encapsulate a _lot_ of development work.

### [Added]

[Added] is basically [New] but for a smaller feature. Or its just not something that's highlighted as much as the [New] things in this release.

We often use [Added] for new editor and terminal integrations.

### [Fixed]

Good ol' [Fixed], the bread and butter of release notes. We use this to indicate that something was broken but now it's not!

### [Improved]

Somewhere in between [Added] and [Fixed] lies [Improved]. The idea is that we've made an existing feature or part of the app better, but it wasn't necessarily broken before. Think of it like an "enhancement" release note.

Does this sound like [Added]? Is that confusing? Yes.

### [Removed]

We rarely use this. Historically, I think it's been primarily used when we've unshipped a feature.

## Release Channel

It's worth noting we are more rigorous about our release notes for production releases than for beta releases.