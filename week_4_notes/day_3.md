Attended a process workshop. I did the Leap Year exercise.

Overall an interesting experience as I was being watched for 30 mins while I worked through a TDD approach design and build of the leap_year method

Key feedback on this was regarding not reading an error message properly and Not using IRB enough

I worked a little on the BOokmark manager and set up te test environment again.

I worked more on the Chitter challenge and wrapped by peep class data into program objects. THis was quite a faff, many errors from this. I spent a fair amount of time working out how to parse the TIMESTAMP type from the database. Turns out it was quite simple...

`DateTime.parse(created_at).strftime("%d/%m/%Y %I:%M %p")`

I also did a few other things like break permissions on the table.. THat was fixed by the below. Not an ideal solution but got me working again.

`ALTER TABLE peeps OWNER TO bromley`


