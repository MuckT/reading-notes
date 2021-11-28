# Prep: Readings and Videos

# Articles

## [How to Solve Programming Problems](https://simpleprogrammer.com/solving-problems-breaking-it-down/)

"The most common mistake I see when conducting interviews or watching someone try to solve a programming problem is they try to start writing code as soon as possible." - John Sonmez

### A simple set of steps

1. Read the problem completely twice.
  - If you don’t understand the problem, you cannot solve it.
2. Solve the problem manually with 3 sets of sample data.
  - “Nothing can be automated that cannot be done manually!”
3. Optimize the manual steps.
  - Figure out if there is another way you can solve the problem easier. It's easier to do this prior to coding.
4. Write the manual steps as comments or pseudo-code.
5. Replace the comments or pseudo-code with real code.
6. Optimize the real code.

## [Pretend Your Time is Worth $1,000/Hour and You’ll Become 100x More Productive](https://medium.com/swlh/pretend-your-time-is-worth-1-000-hour-and-youll-become-100x-more-productive-f04628bb3e6d)

"Indeed the state of all who are preoccupied is wretched, but the most wretched are those who are toiling not even at their own preoccupations…If such people want to know how short their lives are, let them reflect how small a portion is their own.” - Seneca, Emperor Nero’s speech writer and adviser

This reads like someone who places little value on the work of the 'preoccupied', such as those likely doing the work fundamental to a functional house and society. Such as the slaves that Seneca argued are enslaved simply due to unfavorable chance: about 1/3 Roman population during Seneca's time.

“People are unhappy in large part because they are confused about what is valuable.” - William Irvine

"They spend hours watching low-quality television and social media when they should be productive and effective." - Anthony Moore

While I think the article does hit on the fact it's important to value your time so that you prioritize your work and saying no can be a big part of that. But it disingenuously leads readers to were where we should view our free-time as squandered if nothing of value is produced. Sometimes it's important to watch 'low-quality  television' or gossip, it's how we connect as humans. Viewing oneself value of yourself as a sum of your work can make us less resilient.


## [How to think like a programmer — lessons in problem solving](https://medium.freecodecamp.org/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2)

### Problem Solving as Skill

- Having a framework and practicing it.

#### Sample Method

1. Understand - Know exactly what is being asked most problems are hard because you don't understand them.

2. Plan - Nothing can help you if you can’t write down the exact steps. To get a good plan known “Given input X, what are the steps necessary to return output Y?”. For Programmers use comments.

3. Divide - Break it into sub-problems. These sub problems are easier to solve: solve them one by one. Begin with the simplest. Connecting the sub-solutions will give you the solution to the original problem.

4. Stuck? - Take a deep breath. <b>Debug</b> by stepping through your solution trying to find where you went wrong. <b>Reassess</b> by taking a step back look at the problem from another perspective. If that fails start anew - delete it all and start again with fresh eyes.

### Practice

- If you want to be a good problem-solver, solve a lot of problems!

[codewars](https://www.codewars.com/)

[leetcode](https://leetcode.com/)

[https://projecteuler.net/archives](https://projecteuler.net/)

## [The 5 Whys](https://www.mindtools.com/pages/article/newTMC_5W.htm)


### Steps
#### 1. Assemble a Team
- Gather with people who are familiar with the specifics of the problem.
#### 2. Define the Problem
- Write a brief, clear problem statement that you all agree on.
#### 3. Ask the first "Why?"
- Ask why the problem is occurring.

- Your team members may come up with one obvious reason why, or several plausible ones. Record their answers as succinct phrases.

#### 4. Ask why 4 more times.
- Answers should be grounded in fact: they must be accounts of things that have actually happened, not guesses at what might have happened. 

#### 5. Know When To Stop
 - You'll know that you've revealed the root cause of the problem when asking "why" produces no more useful responses, and you can go no further. 

#### 6. Address the Root Causes(s)
- Discuss and agree on the counter measures that will prevent the problem from recurring.

#### 7. Monitor Your Measures
- Track how counter-measures eliminate or minimize the initial problem. If you need to amend or replace repeat the 5 Whys to ensure that you've found the correct root cause.

### Print Shop Example

Problem: Our client is refusing to pay for leaflets we printed.

Why #1: The delivery was late, so the leaflets couldn't be used.

Why #2: The job took longer than we expected.

Why #3: We ran out of printer ink.

Why #4: The ink was all used on a large last-minute order.

Why #5: We didn't have enough ink in stock, and couldn't order new supplies in time.

# Videos

## [What the heck is the event loop anyway](https://www.youtube.com/watch?v=8aGhZQkoFbQ) [@philip_robers](https://twitter.com/philip_roberts)

- How does JavaScript even work?

#### The Call Stack 
- A data structure which records where in the program we are. If we step into a function we push to the top stack if we return we pop off the top of the stack.
- one thread == one call stack == one thing at a time
- Stacktrace is the state of the stack when an action happened.

#### Blocking
- What happens when things are slow? e.g. image processing or network requests.
- Why is this a problem? Because we are running code in browsers and if we block the stack the browser can't do anything else.
- Simplest solution is asynchronous callbacks.

#### Concurrency and the Event Loop
- The runtime can only do one thing at a time, but the browser is more than the JavaScript Runtime. There are supporting API's that can be threaded.

- The event loop job is to look at the stack and look at the task queue. If the stack is empty it takes the first thing form the task queue and pushes it to the stack.

```JavaScript 
// Differing the execution of the code until the stack is clear
setTImeout(function cb() {
  console.log('Hello world!')
}, 0)
```

- Set timeout isn't a guaranteed time to execution it's a guaranteed minimum time to execution. 

- Showing the JavaScript runtime with runtime with [loupe](http://latentflip.com/loupe/?code=JC5vbignYnV0dG9uJywgJ2NsaWNrJywgZnVuY3Rpb24gb25DbGljaygpIHsKICAgIHNldFRpbWVvdXQoZnVuY3Rpb24gdGltZXIoKSB7CiAgICAgICAgY29uc29sZS5sb2coJ1lvdSBjbGlja2VkIHRoZSBidXR0b24hJyk7ICAgIAogICAgfSwgMjAwMCk7Cn0pOwoKY29uc29sZS5sb2coIkhpISIpOwoKc2V0VGltZW91dChmdW5jdGlvbiB0aW1lb3V0KCkgewogICAgY29uc29sZS5sb2coIkNsaWNrIHRoZSBidXR0b24hIik7Cn0sIDUwMDApOwoKY29uc29sZS5sb2coIldlbGNvbWUgdG8gbG91cGUuIik7!!!PGJ1dHRvbj5DbGljayBtZSE8L2J1dHRvbj4%3D)

- Triggering a bunch of events can <b>flood the queue</b> preventing other callbacks and other events from being picked up by the event loop quickly.

## [The Super Mario Effect - Tricking Your Brain into Learning More | Mark Rober | TEDxPenn](https://www.youtube.com/watch?v=9vJRopau0g0)

- "The Super Mario Effect Focusing not on the pits, to stick with a task and learn more." - [Mark Rober](https://www.youtube.com/channel/UCY1kMZp36IQSyNx_9h4mpCg)

- If we are not penalized by failure are more likely to try again - if you don't concern yourself with failure how much more could you learn?

- The concept of life gamification is more than just a positive attitude or never give up, because those sort of imply that you're having to endure against your true desire to quit.  When you frame a challenge or a learning process you actually want to do it.

- By reframing the learning process to focus on the cool end goal the fear of failure is taken off the table and the learning comes more naturally.

- [April Fools' Day Pranks with Mark Rober - Jimmy Kimmel Live!](https://youtu.be/hdDBKxJSAHQ?t=424)
