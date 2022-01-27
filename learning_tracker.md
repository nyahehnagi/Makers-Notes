# Week 1

## Techniques and Approaches to Software Development
Key take away regarding tracking ones learning
  - Goal/Plan
  - Do/Practice
  - Evidence/Reflection

Test Driven Development
  * Ensure to only write the code to pass the test

Pair Programming
  * Currently feeling a complete novice in this area. But the concept I fully embrace and feel I understand

## Coding

### RSpec
Use of one line syntax for RSpec
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

https://relishapp.com/rspec/rspec-expectations/docs/built-in-matchers/predicate-matchers

This is wrong!
~~~~
expect(bike).to be_working? 
~~~~
This is right.. Mind the question mark.. you don't need it with predicate matching
~~~~
expect(bike).to be_working 
~~~~


Discovered the use of `subject' with RSpec

instead of writing this inside the description of a DockingStation class test..

~~~~
it "releases a bike that is working" do
  docking_station = DockingStation.new
  bike = docking_station.release_bike
  expect(bike).to be_working 
end
~~~~

you can write this.. You can reduce the line count by one as you do not need to explicitly
instantiate a DockingStation object.

~~~~
it "releases a bike that is working" do
  bike = subject.release_bike
  expect(bike).to be_working 
end
~~~~

## Test behaaviour not state!

Realised I had exposed the implementation and thus the state of my code during the Boris Bike challenge. The code was not cohesive, It's since been refactored. 

## What I've done
* https://github.com/nyahehnagi/skills_workshops
* https://github.com/nyahehnagi/boris_bikes


