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

SRP! Single Responsibility Principle


## Coding

Learned Ruby!

- I can write a basic web site that has been test driven!
- Post, Redirect, Get pattern
- Dependancy injection
- Delegate 
- RESTful routes
- Database connection classes
- Wrapping database data into program objects
- Class methods (self.)
- Instance methods

## RSpec
Good site for writing good specs
https://www.betterspecs.org/

use of the change matcher

e.g `expect{ oyster_card.top_up (1) }.to change{ oyster_card.balance }.by 1`

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

Doubles
The use of let
allow/receive
alias'ing subject

class_doubles

 let(:twilio_client_class) { class_double("Twilio::REST::Client") } 
~~~~
  it "raises an error when not successful in sending an SMS" do
    stub_const('Twilio::REST::Client', twilio_client_class)
    allow(twilio_client_class).to receive(:new).and_return(failed_twilio_client)
    expect { twilio_sms.send(from, to, body) }.to raise_error "Failed to send SMS"
  end
~~~~

## Test behaviour not state!

Realised I had exposed the implementation and thus the state of my code during the Boris Bike challenge. The code was not cohesive, It's since been refactored. 

## Slack

I know how to make a workflow in Slack

## What I've done (Evidence)
* https://github.com/nyahehnagi/ruby_learning
* https://github.com/nyahehnagi/skills_workshops
* https://github.com/nyahehnagi/skills_learning


* https://github.com/nyahehnagi/airport_challenge
* https://github.com/nyahehnagi/takeaway-challenge
* https://github.com/nyahehnagi/rps-challenge
* https://github.com/nyahehnagi/chitter-challenge
* https://github.com/nyahehnagi/bowling-challenge-ruby

