# Hello Rails

## Previous requirement

- Ruby
- pgAdmin 4

## Then I Followed these steps:

  - `gem install rails`			
				
1.- In the command prompt	(the name should have been Hello-Rails		
  - `rails new Project --database=postgresql`
  - `cd Project`
  - `code .`
				
2.- Open config/database.yml and scroll down to line 23 (default section), then add:
	- username: postgres
	- password: MyPassword (your pgAdmin password)

3.- Back to command prompt
  - `rails db:create`
  - `rails s`

4.- In the browser you can use any of these:
  - `localhost:3000`
  - `[::1]:3000/`
  - `127.0.0.1:3000`
				
## To avoid showing passwords to all people who clones your repo:

  - `bundle add dotenv-rails`

  1.- Create file `.env`
  
  2.- Ignore `.env` in `.gitignore` file
		
Usage example:
  - .env file
    - `PG_PASSWORD = thisIsThePassword`
  - config/database.yml file
	  - `<%= ENV['PG_PASSWORD'] %>`
