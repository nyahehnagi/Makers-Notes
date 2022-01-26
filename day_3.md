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

Katheleen's Boris Bike Repo

https://github.com/heykathl/boris-bikes2

## git

git is a git! spent a couple of hours working out how to merge, then revert a commit and force pulls - because of setting the merging strategy to default - which at the time felt like the right thing to do. Next time rebase-true is probably the way to go for our problem

So what did I learn.. 

`git pull origin main --allow-unrelated-histories`
This enables you pull the remote repo to your local repo irrespective of never being linked in the past
`git revert <commit hash> -m 1 `
This puts you back to a previous commit
`git push --force`
This forces the local repo onto the remote repo
