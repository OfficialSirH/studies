[[Grokking Algorithms]]

## Classifying oranges vs. grapefruit

If you wanted to differentiate a fruit on whether it was an orange or a grapefruit, a characteristic to compare against oranges is that grapefruits are bigger and redder. If we have a chart showing a bunch of plotted points of oranges and grapefruits, then say a new point is plotted, what determines that point is which fruit? By checking the nearby points, you can determine if the new point is an orange or a grapefruit based on if there's more nearby oranges or more nearby grapefruits.

## Building a recommendations system

Say you wanted to recommend movies to people like Netflix, how would that be done? Simple, by recommending movies that others with similar interests have liked. Getting the data necessary to define how two or more users are similar is the next piece of the puzzle.

### Feature extraction

In this example, users could be featured via 5 characteristics:
- comedy
- action
- drama
- horror
- romance
With these 5 data points, a user could compared to another with the *Distance Formula*:

$$
\sqrt{ (x_{1} - x_{2})^2 + (y_{1} - y_{2})^2 }
$$
An example of this being applied to 2 users could look like this:
- Priyanka
	- Comedy: 3
	- Action: 4
	- Drama: 4
	- Horror: 1
	- Romance: 4
- Morpheus
	- Comedy: 2
	- Action: 5
	- Drama: 1
	- Horror: 3
	- Romance: 1
$$
\sqrt{ (3 - 2)^2 + (4 - 5)^2 + (4 - 1)^2 + (1 - 3)^2 + (4 - 1)^2 }
$$
Which comes out to being $2\sqrt{ 6 }$, meaning those 2 users aren't that similar.

### Exercises

- 10.1: In the Netflix example, you calculated the distance between two different users using the distance formula. But not all users rate movies the same way. Suppose you have two users, Yogi and Pinky, who have the same taste in movies. But Yogi rates any movie he likes as a 5, whereas Pinky is choosier and reserves the 5s for only the best. They’re well matched, but according to the distance algorithm, they aren’t neighbors. How would you take their different rating strategies into account?
	- Infer that the average or higher ratings from Pinky would also be liked by Yogi and that Yogi's liked movies could be given average or higher ratings by Pinky
- 10.2: Suppose Netflix nominates a group of “influencers.” For example, Quentin Tarantino and Wes Anderson are influencers on Netflix, so their ratings count for more than a normal user’s. How would you change the recommendations system so it’s biased toward the ratings of influencers?
	- Users will get recommendations from the influencers with much longer distances than the average users.

### Regression

How would you predict someone's rating for a movie that you're recommending to them? Well, you could take their 5 (or any number) nearest neighbors and get the average of their ratings on the movie, getting a decent prediction on what that user might rate the movie as. Another use case would be to predict how much bread you would need to bake for a day if you run a bakery. You could take weather on a scale of 1 to 5, weekend or holiday being a 1 if it is one of those or 0 if not, and 1 or 0 if there's a game. All of that combined to measure how much bread you sell on each of these characteristics and then predicting how much bread you need for a day based on the average of the nearest neighbors with these determined points could give a helpful estimation.

### Picking good features

When deciding on the features for something, they should have an actual use to what they're featuring. This means they should both:
- describe features that actually give a distinction between each thing that's being compared against
- not be heavily bias/repetitive towards characteristics of one thing over another.

Do you think ratings are a good way to recommend movies? Maybe I rated *The Wire* more highly than *House Hunters*, but I actually spend more time watching House Hunters. How would you improve this Netflix recommendations system?
- Take into account the series watch time from a user to better determine what content that user watches more.
can you think of two good and two bad features you could have picked for the bakery?
- Good Features
	- Is it an outside eventful day like fireworks where people might want to make sandwiches before watching fireworks
	- Is it a Friday, where people may want to get shopping done after a 5 day work week
- Bad Features
	- Did your country of origin decide to invade another country for oil?
	- Is it a full moon?

### Exercise

- 10.3: Netflix has millions of users. The earlier example looked at the five closest neighbors for building the recommendations system. Is this too low? Too high?
	- Too low, because with only 5 users, just one user having a sudden big rating difference could completely shift how the system could interpret the compared against user's potential recommendations. 1000 or even up to 10000 would give much higher precision for the user's recommendations with the many many other neighboring users.

## Introduction to machine learning

Building a recommendations system with KNN is one form of machine learning as more data points builds onto how the algorithm understands what it should or shouldn't recommend to the user.

### OCR

OCR, also known as *optical character recognition*, is an algorithm that is aimed to recognize characters based on characteristics like lines, curves, and points. It does this with the help of the KNN algorithm but a lot more complex as it learns what characters *should* generally look like based on given images for its *training* to recognize what curves, lines, and points every kind of character should have.

### Building a spam filter

A simple algorithm, called *Naive Bayes classifier*, is first trained by giving it some data, an example like below:

| Subject                                        | Spam?    |
| ---------------------------------------------- | -------- |
| "Reset your password"                          | Not Spam |
| "You have won 1 million dollars"               | Spam     |
| "Send me your password"                        | Spam     |
| "Nigerian prince sends you 10 million dollars" | Spam     |
| "Happy birthday"                               | Not Spam |

The algorithm calculates the probability that something is spam by determining how likely a word, like *million* as an example, appears in an email. This is similar KNN in that it finds what's most similar to another "neighbor".

### Predicting the stock market

The stock market is a very unpredictable mess with so many variables that can determine whether a stock is gonna go up or down. So how would one predict it? One could try to assume that if it went up yesterday that it might go up today as well or you could assume that it goes up for all of May, but these assumptions are just never gonna work with near to baseless assumptions. This makes the stock market really hard to predict unless you know beforehand what a company is going to announce or release (this is called insider trading, sadly illegal for us peasants).