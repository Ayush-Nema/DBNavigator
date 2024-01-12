# DBNavigator
Learn about how to setup PGAdmin and connect to PostgreSQL server using `SQLAlchemy` and `psycopg2`

## Installing PGAdmin 4  
Follow [this](https://www.pgadmin.org/download/) download link.  
Choose operating system and version to download.  

## Setting up the `postgresql`
(Instructions here for setting up server in MacOS)
1. `brew doctor`
2. `brew update`
3. `brew install libpq`
4. `echo 'export PATH="/opt/homebrew/opt/libpq/bin:$PATH"' >> ~/.zshrc`
5. `source ~/.zshrc`
6. `brew link --force libpq`
7. `psql —version`
8. Search for `install postgres in mac`: [Download link](https://www.postgresql.org/download/macosx/)
9. `brew install postgresql@15`
10. echo `'export PATH="/opt/homebrew/opt/postgresql@15/bin:$PATH"' >> ~/.zshrc`
11. To start the server: `brew services start postgresql@15`
12. To stop the server: `brew services stop postgresql@15`
 
### `postgresl shell`  
`psql -d postgres`  
-> opens postgres shell
- run `\l` command to list the servers: “postgres=# \l” 
- run `\q` to quiet the shell and return to normal terminal

Reference link for installing `psql`:  
1. Source 1: [Click here](https://www.timescale.com/blog/how-to-install-psql-on-mac-ubuntu-debian-windows/)
2. Source 2: [Click here](https://mcengkuru.medium.com/how-to-install-psql-on-your-mac-a-step-by-step-guide-with-troubleshooting-tips-ade65c441abf)

## Setting up `PgAdmin 4`
- open PGAdmin UI
- Give server name: `sample_server`
- Username: Go to terminal and run `$ whoami`. Copy the output and paste in username field
- Port: 5432
- Host: localhost
- password: password
- Click on Save in the bottom right. And done!
