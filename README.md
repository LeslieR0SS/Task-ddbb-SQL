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
    
```mysql
UPDATE Vol SET Dia="2009-10-15" WHERE NumVol=222;
```
    
![1-updateBefore](https://user-images.githubusercontent.com/91556932/168100964-abe3b4dd-9ddc-41cd-83b5-bd246ab9a0d8.png)

![1-updateAfter](https://user-images.githubusercontent.com/91556932/168100990-7c194f27-73af-44e5-8073-c5997cb2f04c.png)

### Task 2

    The plane for flight 999 has been changed, the new one has 128 seats and is from the company Air France.
    Set its new values.
    
**Before**

![2-before](https://user-images.githubusercontent.com/91556932/168103163-24f399c4-ad6a-4ec6-ab39-e6bcbd8b807c.png)
![2-before2](https://user-images.githubusercontent.com/91556932/168103173-2a278dab-cb28-443e-8549-504f472d740e.png)

```mysql
UPDATE Vol SET Capacitat="128", NomCo="Air France" WHERE NumVol=999;
```

**After**

![2-after](https://user-images.githubusercontent.com/91556932/168106982-bf385337-e0cc-493a-866c-0c91f31d1d32.png)
![2-result](https://user-images.githubusercontent.com/91556932/168106995-f5918c93-13b0-4a32-85af-5dd975b2ff0c.png)



### Task 3

    Flight 666 has been canceled.
    Remove it from the database.

**Before**

![3](https://user-images.githubusercontent.com/91556932/168107547-d9c1fea5-5c4b-406c-abdd-8e79f4dcf927.png)

```mysql
DELETE * FROM Vol WHERE NumVol=666;

```

**After**

![3-after2](https://user-images.githubusercontent.com/91556932/168108299-73cf8f02-c990-430e-9518-20d9d75faa1f.png)


### Task 4

    The user with ID Z23456K has asked us to remove all of it's data.
    Remove the user from the database.
    
**Before**

![4-before](https://user-images.githubusercontent.com/91556932/168112216-dd5928fc-d8b5-4d7d-ac6c-342df844cfea.png)

```mysql
DELETE FROM Passatger WHERE ID="Z23456K";
```

**After**

![4-after](https://user-images.githubusercontent.com/91556932/168111552-d2f3fc91-55d7-448c-82c1-36ed36c2a233.png)



### Task 5

    Using a subquery.
    Find all cities with flight departures from the company Iberia.


```mysql
SELECT Ciutat FROM Aeroport WHERE NomAeroport IN (SELECT NomAerOrigen FROM Vol WHERE NomCo = "Iberia");
```

**After**


![5-after](https://user-images.githubusercontent.com/91556932/168114720-c427c316-a202-44d3-b18e-14219811b256.png)


### Task 6

    Using a subquery.
    Find the maximum amount of arrivals in a single airport.
    
**Before**

```mysql
SELECT MAX(Arrivals.CountArrivals) AS 'MaxCountArrivals' FROM (SELECT COUNT(NomAerDesti) AS 'CountArrivals' FROM Vol GROUP BY NomAerDesti) Arrivals;
```

**After**

![6](https://user-images.githubusercontent.com/91556932/168115045-b5d3b12c-7e91-484f-a6bb-ced71a475119.png)

