# Task-ddbb-SQL

## How to create the db for this task using the shell:

```shell
mysql -u leslie -p #to acces to mysql account
CREATE DATABASE vols; #to create the db
SHOW DATABASES; #To show all the ddbb
```

![database](https://user-images.githubusercontent.com/91556932/167886717-054e72c9-311a-4fe4-9dbf-bef3e4cb821c.png)
![show_tables](https://user-images.githubusercontent.com/91556932/168091163-17d5652f-c64a-4e60-a352-ccb0ec35affc.png)

---

## Task

After changing the values of any table perform a Select from all the table values to check it worked.

### Task 1 

    The flight with number 222 has suffered a delay.
    Change its Dia to 15/10/2009.
    
'''
UPDATE Vol SET Dia="2009-10-15" WHERE NumVol=222;
'''
    
![1-updateBefore](https://user-images.githubusercontent.com/91556932/168100964-abe3b4dd-9ddc-41cd-83b5-bd246ab9a0d8.png)

![1-updateAfter](https://user-images.githubusercontent.com/91556932/168100990-7c194f27-73af-44e5-8073-c5997cb2f04c.png)

### Task 2

    The plane for flight 999 has been changed, the new one has 128 seats and is from the company Air France.
    Set its new values.

### Task 3

    Flight 666 has been canceled.
    Remove it from the database.

### Task 4

    The user with ID Z23456K has asked us to remove all of it's data.
    Remove the user from the database.

### Task 5

    Using a subquery.
    Find all cities with flight departures from the company Iberia.

### Task 6

    Using a subquery.
    Find the maximum amount of arrivals in a single airport.
