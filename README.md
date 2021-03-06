# ASSIGNMENTS-VM

## Installation and Test requirements

All the projects for this assignment are built and tested on Windows 10 OS.

1. Create a new project folder.
2. Clone this repository to that folder with `git clone` command.
3. **cd** into the folder named **vagrant** and run `vagrant up` from command prompt.
4. Once done, run the command `vagrant ssh`.
5. On the vagrant command line, `cd /vagrant`.
6. Install python-pip with `sudo apt-get install python-pip`.
7. Install flask with `sudo pip install flask`.
8. Install postgresql with `sudo apt-get install postgresql postgresql-contrib`
9. Log in as superuser **postgres** with `sudo su - postgres`.
10. Run the command `psql` to get the psql command line.
11. Run the following commands in the psql command line:
    ```
    CREATE DATABASE users;
    CREATE DATABASE mobileusers;
    CREATE USER dbuser;
    ALTER ROLE dbuser WITH PASSWORD 'users';
    GRANT ALL PRIVILEGES ON DATABASE mobileusers TO dbuser;
    GRANT ALL PRIVILEGES ON DATABASE users TO dbuser;
    ```
12. Exit psql command line with Ctrl+Z and `logout`.
13. Be sure that you have logged out by checking the shell. It should display
    `vagrant@vagrant:/vagrant$` instead of `postgres@vagrant:~$`.
14. Install SQLAlchemy with `sudo pip install sqlalchemy`.
15. Install psycopg2 with `sudo pip install psycopg2`.
16. Install twilio with `sudo pip install twilio`.
17. Install flask_mail with `sudo pip install flask_mail`.
18. Clone the Email-Verification-System project from [https://github.com/MANOJPATRA1991/Email-Verification-System](https://github.com/MANOJPATRA1991/Email-Verification-System) with `git clone` command into the **vagrant** directory.
19. Clone the OTP-based-verification project from [https://github.com/MANOJPATRA1991/OTP-based-verification](https://github.com/MANOJPATRA1991/OTP-based-verification) with `git clone` command into the **vagrant** directory.

20. Create your own Twilio account and get the following information:
	1. TWILIO_ACCOUNT_SID
    2. TWILIO_AUTH_TOKEN
    3. TWILIO_NUMBER
    
    Update OTP-based-verification project's config.py file with the above information.
21. Run each project with `python run.py` from within the respective project directories(i.e., OTP-based-verification and Email-Verification-System).

## References
1. [Vagrant](https://www.vagrantup.com/)
2. [PostgreSQL](https://www.postgresql.org/)
