State, that usually goes into your Redux store, is the most important aspect of any front-end application. Most people think it's the views that are most important, but that's a mistake. State trumps everything. Quality of your state design reflects quality of your application. Hence state needs to be designed thoughtfully.

There are a bunch of things you need to keep in mind when designing state.

# Single Source of Truth
For any piece of information, there needs to be a single source of truth. Multiple sources of truth will cause confusion, and can degrade quality of your application.

# Optimize for Reads
Any datastore can be optimized for either reads or writes. Since, primary function of font-end state is to provide information to components, it needs to be optimized for reads. That means, critical pieces of information should be able to be accessed in constant time.