List the last time a User registered on a Lync pool and it's client type
========================================================================

            
**Update: 5-July-2014:**

We've added some new functionally to the script:


  *  Check if the User is running under Administrator elevation privileges 
  *  The Information also includes results from the Get-CsUserPoolInfo cmdlet, meaning that you can now see when the user last logged in, and also see what his primary main server is and what his backup servers are.

  *  Added additional validation tests 

---


Recently I’ve been asked to pull out a list of all users connected to Lync, their Last Logon date and the type of client they were using.


There were already a lot of articles around this subject, but I couldn’t find anything which output both Client last logon and the type of client it was logged on with.


Based on the following great articles which go into details with what are the required SQL queries and how to combine it into a PowerShell script, I’ve created a SQL Query command and a dedicated PowerShell script which will provide with the desired
 output.


  *  [How to Get the Last Time a User Registered with a Front End](http://blogs.technet.com/b/dodeitte/archive/2011/05/11/how-to-get-the-last-time-a-user-registered-with-a-front-end.aspx)

  *  [Script: Get-CsConnections.ps1 – See User Connections, Client Versions, Load Balancing in Lync Server](http://www.ehloworld.com/269)

  *  [List the Users and Client Endpoint Versions Connected to a Registrar Pool: Direct Connection](http://blogs.technet.com/b/nexthop/archive/2011/03/10/list_2d00_users_2d00_and_2d00_endpoints_2d00_direct.aspx)

  *  [List Connections and Users connected to Lync Registrar Pool](http://blogs.technet.com/b/meacoex/archive/2011/07/19/list-connections-and-users-connected-to-lync-registrar-pool.aspx)


**The SQL Query:**

** The PowerShell Script:PowerShell Options:![Image](https://github.com/Guy-Bachar/list-the-last-time-a-user-registered-on-a-lync-pool-and-it's-client-type/raw/master/01.png)**

**![Image](https://github.com/Guy-Bachar/list-the-last-time-a-user-registered-on-a-lync-pool-and-it's-client-type/raw/master/02.png)
**

** Output example:**
![Image](https://github.com/Guy-Bachar/list-the-last-time-a-user-registered-on-a-lync-pool-and-it's-client-type/raw/master/untitled.png)

        
    
