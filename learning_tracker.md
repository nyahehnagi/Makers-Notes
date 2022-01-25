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

## What I've done
* https://github.com/nyahehnagi/skills_workshops
* https://github.com/nyahehnagi/boris_bikes


