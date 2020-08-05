One to Many Relationships
===

## SWBATs

- [ ] Implement a one-to-many object relationship
    - One object _has many_ objects
    - One object _belongs to_ another object
- [ ] Demonstrate the concept of an Entity Relationship Diagram
- [ ] Demonstrate Single Source of Truth
- [ ] Infer type of method (class or instance) through naming conventions

## Outline

Quick review of OOP:
- we created classes
- we created instances of classes using `initialize`
- we created instance and class methods
- we used `attr_` macros for getters and setters
    - attr_reader - getter, retrieve data
    - attr_writer - setter, set data
    - attr_accessor - getter/setter, combine the two
- we looked at `self`

## Discussion

What do the following mean in plain English? What do they mean in programming?

- Model
- Domain
- Domain modeling - Entity Relationship Diagram (ERD)
- Relationships
    - One to many relationship
    - Many to many relationship

_Why do we care so much about codifying and being really specific about the terminology of has-many/belongs-to?_ The terms are very powerful because we can use the same idea to describe relationships across many different types of domains. The relationship between artist and song, is the same as book and author, user and tweets, etc.


### How to think about relationships
1. For every one (x), how many (y)?
2. For every one (y), how many (x)?

- Schema
- Single Source of Truth
- How can we start thinking about the data in our models?

### Deliverables

Create a User class. The class should have these methods:
  - [x] `User#initialize(username, bio)` takes a username and a bio and creates a User instance.
  - [x] `User#username` returns a string for the user's username. _Should not_ be able to change after the user is created.
  - [x] `User#bio` returns a string for the user's bio. _Should_ be able to change after the user is created.
  - [ ] `User#post_tweet(message)` takes a message an argument, creates a new tweet, and adds it to the user's tweet collection.
  - [ ] `User#tweets` returns an array of Tweet instances.
  - [x] `User.all` returns all the User instances in our app.
  - [ ] *bonus* `User.print_tweets` that prints the message of each tweet to the screen in a pretty way.
  - [ ] *bonus* `User.most_tweets` returns the instance of the user who has made the most tweets.

Create a Tweet class. The class should have these methods:
  - [ ] `Tweet#initialize(message, user)` takes a message and a user and creates a Tweet instance.
  - [ ] `Tweet#timestamp` returns the time the Tweet was created. _Should not_ be able to change after the tweet is created.
  - [ ] `Tweet#message` returns a string. _Should not_ be able to change after the tweet is created.
  - [ ] `Tweet#user` returns an instance of the User class. _Should not_ be able to change after the tweet is created.
  - [ ] `Tweet.all` returns all the Tweet instances in our app.
  - [ ] `Tweet#username` returns the username of the tweet's user.

### Discussion Questions

- What is a one-many-relationship? How would we draw that in an ERD?
- What does Single Source of Truth mean?
- What is a model? Domain? Domain model?
- What is the relationship between a class and an instance?
