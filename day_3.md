discovered the use of `subject' with RSpec

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

* Can ask a coach to observe a pairing session...
* How much have I practiced on something?
* What am I unsure of regarding TDD?
* What process am I following.. am I following a TDD approach. e.g commiting at suitable times

Goal - Plan - Evidence

Ensure goals are SMART - specific, measurable, achievable, relevant and time bound

Get the TDD & Debugging airtable