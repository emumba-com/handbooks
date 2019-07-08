# Problem Solving
Algorithms and data structures

Table of Content
*  [Data Structures](#data-structures)
*  [Algorithms](#algorithms)

## Data Structures
Most of the computer science problems, if not all, become quite simpler if you choose the right data structure. You must understand, at least, data structures given in this section and their right usage. Good news is that only handful of these data structures are used in tackling 80% of the problems we encounter.
### List
List is a collection of items. It is the default choice for storing multiple values for most of the beginners.
```
//a list of team members
team_members = ['Ahmed', 'Rashid', 'Ayesha', 'Khalid']
```
But it may not be the wisest default in all scenarios. For example, imagine if you have to check if `Ahmed` is already in the list. It works fine if you do
```
team_members.index('Ahmed') // returns 0 against our list
```
But under the hood, your code is going through each team member one by one and matching it with `Ahmed`. In worst case, i.e. `Ahmed` is last value in `team_members`, your code will have to do N comparisons where N is the number of team members, not very efficient. A better choice in this case would be a ##Set.

### Set
Set is a collection of unique values. Think about it as a list with two special properties.
1. It  cannot hold duplicate values.
2. Instead of doing brture force comparison with each element, like we saw in case of Set, it uses efficient algorithm to check if an item already exists.

These properties makes it the default choice for storing unique values. Also it comes very handy in situations where you want to search items in a collection.

### HashMap
HashMap can be considered an extension of Set. In addition to the two primary properties of set, it provides a way to associate a `value` with a `key`.

Going back to our list
```team_members = ['Ahmed', 'Rashid', 'Ayesha', 'Khalid']```
Imagine you also want to store score of each member. You can do something like this
```
team_members = [{"name": "Ahmed", "score": 74},
				{"name": "Rashid", "score": 68},
				{"name": "Ayesha", "score": 91},
				{"name": "Khalid", "score": 55}]
```
Here `team_members` is a collection of objects where each object has two properties `name` and `score`. Let's assume you have to find score of `Ahmed`. You can do something like this.
```
for item in team_members:
    if item['name'] == 'Ahmed':
        print(item['score']) //prints 74
```
You may have noticed, if suffers from same limitation as `List` i.e. in order to find the right object (where name is `Ahmed`) you have to go through each object and do the comparison on `name` property. And in case `Ahmed` is the last item or if `Ahmed` doesn't exist in the list you will end up doing N comparisons where N is the number of items in the list.

HashMap can help here because, like set, it uses optimized algorithm to find the element with a specified `key` (Ahmed in our example).
```
team_members = {}
team_members['Ahmed'] = 74
team_members['Rashid'] = 68
team_members['Ayesha'] = 91
team_members['Khalid'] = 55
```
Now to find Ahmed's score you can simply do
```
if 'Ahmed' in team_members:
    print(team_members['Ahmed']) //prints 74
```
This way, behind the scene, your code won't be doing comparison against each team member, rather it will be using hashing to quickly find the `key` (Ahmed) in the HashMap. For further reading, it is highly recommended to learn how `HashMap` is implemented in language you are most comfortable with.

## Algorithms
At any day of the week, and at any time of the day, even if there is a nuclear apocalypse or (in any other parallel universe) Pakistan has beaten India in the World Cup,  point is no matter whatever state of mind you are in you should be able to write these algorithms within a minute or two.
### Tree Traversal

This is a `Tree` data structure. It is a binary tree as any node has at max 2 children.

```
          10
         /  \
        8   16
       /\    \
      1  3    8
```

You should be able to a method that takes this tree in input and
 - Prints all elements of a tree
 - Find minimum or maximum number in a tree
 - Find out of all the elements in the tree are unique

or any variation of these problems. By doing this you will have a pretty solid grip on a concept called `recursion` which is abosultely necessary to understand if you want to succeed as a programmer. Moreover, you should be able to explain how much time (Big O) your implementation will take and how much space/memory will be consumed by it.
