# Day 4

Continued my work on SecretDiary

## Debugging

https://github.com/makersacademy/skills-workshops/tree/main/test_driven_development/debugging_fizzbuzz

Process of debugging is the same, but different languages have different tools to help with debugging

### What is a bug?

An unexpected behaviour or output in your program / any deviation from expected behaviour

* We want to have a clear idea of the behaviour we expect from our code
* write out what I expect to happen when I run my code
* Once you're clear on what you think you code should be doing, step by it line by line to make sure each step of this is actually happening as expected

Learned how to make a workflow in Slack - I used this to create a feedback form

## Exercises

Looked at 2 exercises to practice debugging

https://github.com/nyahehnagi/skills_workshops/tree/main/test_driven_development/debugging_fizzbuzz

## RSPEC Usage

Let aliases a piece of code
`let(:bike) { Bike.new }`

Mocks - The use of Double, allow and recieve and_return

General line for when under it
`allow(bike).to receive(:working?).and_return(false)`

One liner example - Good for Don't Repeat yourself code (DRY)
` let(:bike) { double(:bike, :working? => true) }`

Worked on Boris bike challenge 12 -20

https://github.com/nyahehnagi/boris_bikes