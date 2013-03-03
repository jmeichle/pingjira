pingjira
========

- Repo for querying of Jira via Ruby.

- It queries for tickets matching the following JQL:

	Assignee = currentUser() AND NOT (status = Closed OR status = Done)

nd displays new information about your queue relative to the last time it ran. 

- For tickets in your queue not seen before, it prints the ticket header info, in red, 
	then prints all 'new' comments in yellow. 

- For tickets in your queue with new updates, it prints the ticket header info and the new comment in yellow 

- For tickets unchanged since last run, it prints the ticket key, title, and time since the last update in green.

- Tickets in your last execution but no longer in your queue are marked as teal upon display.


INSTALL: 

1) Install rubygems and the 'json' gem: "sudo gem install json" 

2) Setup credential file, default at ~/.jiraupdatercreds.json with format:

	{ "hostname" : "https://jira.web.com", "username" : "yourusername", "password" : "thepassword" }

3) chmod credential file to 400 permissions

RUN:

- Run 'ruby pingJira' or add it to your $PATH

