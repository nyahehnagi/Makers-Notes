# Peer Groups

## What is a peer group for?
* Support
* Sharing knowledge
* Bouncing ideas between members

## What would I like to see from a peer group
* Sharing knowledge
* Code reviews

## What can you do to facilitate the above
* Encouragement
* Regular comms
* Honesty
* Understanding
* Offering help

# Test Driven Development (John Forster)

# Goals
* explain why we do TDD
* Describe the steps of a TDD dev process

# Why are test useful?
* Make sure it works
* Understanding and clarifying the user requirements
* Opportunity to find missing requirements
* Provides confidence when making changes
* Form of documentation
* Test coverage, helps you find non functional code.
* Capture unhappy paths
* Save time in the long run
* help design incrementally

# Why write tests first
* Structure code and write what's necessary
* Incremental development
* Stick to the specification
* Help with clarity of requirements
* Help think about only one thing at a time.
* Planning ahead and focusing on where you want to be
* Ensuring you have good code coverage

We ran through a quick exercise to see what the TDD process is.

https://excalidraw.com/#room=321f6ec44e4fab20c9d0,qCZC1K-lsQ-fceG8p88TUQ
useful tool for knocking up diagrams

# Exercises

## Piggy Bank
First stab at Test Driven Development with a Piggy Bank
https://github.com/nyahehnagi/skills_workshops/tree/main/test_driven_development/piggy_bank

**Key note to take away - ensure to write the code to pass the test!!**


`require_relative` is used to provide access to local files in the same project

`require` is generally used to include gems.

## Boris Bikes
Started on Boris Bikes challenge as a pair programming exercise
https://github.com/nyahehnagi/boris_bikes

Discovered the use of one line syntax for RSpec
https://relishapp.com/rspec/rspec-core/v/3-10/docs/subject/one-liner-syntax
 e.g 
 ~~~~
 describe DockingStation do
  describe "#release_bike" do
      it { is_expected.to respond_to :release_bike }
  end
 end
 ~~~~

which is better than

~~~~
 describe DockingStation do
  describe "#release_bike" do
    it "should response to the method call release_bike" do
      docking_station = DockingStation.new
      expect(docking_station).to respond_to(:release_bike)
    end
  end
 end
~~~~

## My initial thoughts on Pair Programming

Pair programming is fun but also currently rather difficult (for me at least). It's a skill I need to learn through doing a lot more of it. We all have different ways of working and approaches to coding, acquiring information and problem solving.