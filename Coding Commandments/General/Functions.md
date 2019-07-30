When writing functions, a few things need to be kept in mind:

# Naming

Use verbs for naming your functions. Verbs, in English language, refer to names of actions. For example, `jump`, `get`, `set`, `go`, etc. are examples of verbs. This is a nice [introduction to verbs](https://www.khanacademy.org/humanities/grammar/parts-of-speech-the-verb/introduction-to-verbs/v/introduction-to-verbs-the-parts-of-speech-grammar) from Khan Academy.

# Coupling

Make sure the function is [as little coupled with its environment as possible](./coupling.md).

# Purity

Write [pure functions](https://www.sitepoint.com/functional-programming-pure-functions/) whenever possible. Avoid intertwining your logic and IO operations, so your logic remains testable and reusable.

# Size

Do not create a function that is doing too many things. Keep functions small. A function should only do what it's name suggests. Same principle apply to classes as well.
