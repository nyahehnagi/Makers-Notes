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