# How to Review a Pull Request

*A guide for developers who are new to reviewing.*

Reviewing is a separate skill from writing code, and nobody is born good at it. This guide gives you an order of operations so you catch the things that matter before you spend attention on the things that don't.

---

## 1. The mindset

Three ideas to hold onto:

**You are not looking for mistakes. You are answering one question: "Am I comfortable with this being in our product?"** That reframe changes what you look at.

**Once you approve, the code is yours too.** You share responsibility for what it does. This is the single idea that raises review quality the most.

**A review is a conversation between two people who both want the feature to work.** It is not a test the author has to pass.

---

## 2. Before you read a single line

**Read the PR description and the linked story.** If you can't tell what problem this solves and how to verify it works, that is your first comment. A reviewer who doesn't understand the goal cannot tell correct code from incorrect code.

**Pull the branch and run it.** Click through the feature the way a user would. A surprising number of bugs are invisible in a diff and obvious in thirty seconds of actual use.

**Check the size.** If the PR is over a few hundred lines of real change, your attention will drop off a cliff partway through and you'll rubber-stamp the rest. Asking "can this be split?" is legitimate, useful feedback.

---

## 3. Read in passes, biggest concerns first

Go through the diff more than once. Each pass looks for one kind of thing. Resist the urge to fix indentation on pass one.

### Pass 1: Does it do what it claims?

Compare the actual behavior to the acceptance criteria in the story. Missing cases matter more than anything else on this list.

- Does every acceptance criterion have code behind it?
- Did it change behavior somewhere it wasn't supposed to?
- Is there anything in the diff that isn't related to this story? (Leftover debug code, an unrelated "while I was in here" refactor, a commented-out block.)

### Pass 2: What happens when things go wrong?

This is where you will find the most real issues. New developers write the happy path well and forget everything else.

- Empty array, empty string, zero results
- `null` / `undefined` where an object was expected
- The API call fails, times out, or returns a 500
- The user isn't logged in, or is logged in without permission
- Loading states: what does the user see for the two seconds before data arrives?
- Double-click, double-submit, rapid navigation away

### Pass 3: Security and data handling

- Secrets, API keys, or connection strings committed to the repo
- User input rendered without escaping, or interpolated into a query
- An endpoint with no auth check on it
- Sensitive data logged to the console or sent to the client
- Dependencies added that nobody has looked at

### Pass 4: Tests

- Are there any?
- Do they test *behavior* or just restate the implementation? A test that would still pass if the function were broken isn't a test.
- Do they cover at least one failure case, not just the happy path?
- Do they actually run in CI?

### Pass 5: Readability and structure

- Would you understand this in three months with no context?
- Are the names honest about what the thing does?
- Is there logic duplicated from somewhere else in the codebase?
- Is a function doing three jobs that should be three functions?
- Are comments explaining *why*, rather than restating *what* the line already says?

### Pass 6: Style and formatting

Last, and mostly the linter's job. If you find yourself arguing about formatting in a comment thread, the project needs a formatter, not a debate.

---

## 4. How to write a comment

**Say what you observed, why it concerns you, and what you'd suggest. In that order.**

> This crashes if `results` comes back empty. Could we default to `[]` in the fetch?

That gets fixed. "This is wrong" starts an argument.

**Ask questions when you're unsure instead of asserting.**

> Is there a reason this runs on every render?

This leaves room for the author to have a good answer, and often they do. You learn something either way.

**Label the weight of every comment** so the author knows what's blocking:

| Prefix | Meaning |
| --- | --- |
| `blocking:` | I can't approve until this changes. |
| `suggestion:` | I think this is better; your call. |
| `question:` | I don't understand this yet. |
| `nit:` | Tiny, non-blocking, take it or leave it. |
| `praise:` | This is good and I want you to keep doing it. |

Ten seconds to adopt, and it removes all the guessing about which comments have to be addressed.

**Say what's good.** If someone handled a tricky edge case well, note it. This is not politeness padding. It tells the whole team what "good" looks like in this codebase.

---

## 5. Things to avoid

**Don't rewrite the PR in the comments.** If your feedback amounts to "I would have built this differently," ask whether the current approach is actually wrong or just not yours. Only the first one is worth a change request.

**Don't approve because you don't want to seem difficult.** And don't pile on because you want to look thorough. Both of those are about you rather than about the code.

**Don't review 800 lines in one sitting.** Your judgment degrades after roughly 20 minutes. Take a break or split the review.

**Don't comment on things the tooling already handles.** Formatting, import order, trailing whitespace.

**Don't make it personal.** Talk about the code, not the person. "This function is confusing" instead of "you wrote this confusingly."

---

## 6. When to approve

Approve when:

- It does what the story says
- It won't fall over in the obvious failure cases
- You'd be comfortable being paged at 2am for it

Do not wait for perfect. Perfect never ships. Leave the small stuff as `nit:` and let the author decide.

**Request changes** when something is functionally wrong, unsafe, or untested in a way that matters. Say clearly which comments are the blocking ones.

**Comment without approving** when you have questions you need answered before you can judge it.

---

## 7. Quick checklist

Print this, or keep it in a tab.

- [ ] I read the story and understand what this is supposed to do
- [ ] I pulled the branch and used the feature
- [ ] Every acceptance criterion is covered
- [ ] Empty / null / error cases are handled
- [ ] Loading and failure states exist in the UI
- [ ] No secrets, no unescaped user input, no unprotected endpoints
- [ ] Tests exist, test behavior, and pass
- [ ] I could understand this code in three months
- [ ] Every comment is labeled with its weight
- [ ] I said at least one specific thing that was good

---

## 8. For the author: making your PR easy to review

Reviews get better when the PR is reviewable in the first place.

- Keep it small and about one thing
- Write a description that says what changed, why, and how to test it
- Include a screenshot or short clip for UI changes
- Review your own diff first and leave comments on the parts you're unsure about
- Respond to every comment, even if it's just "good catch, fixed"
- Push fixes as new commits so the reviewer can see what changed
- Don't take it personally. The review is about the code.
