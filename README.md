# osTicket: Creating and Working Tickets

In this lab we will be highlighting the life cycle of tickets in a ticketing system

This lab builds off of: [osTicket: Post Installation Configuration](https://github.com/jeremiahgriffit/osTicket-Post-Installation-Configuration)

## Environments and Technologies Used

- Microsoft Azure
- Virtual Machines
- osTicket

## Operating Systems Used 

- Windows 10 Pro, version 22H2 - x64 Gen2
 
## High-level Configuration Steps

1. As an end-user create a ticket
2. As a Help Desk Agent, observe the ticket’s properties
3. Set Properties to the ticket
4. Work the ticket, communicate with customers
5. Close ticket


## Configuration

### As an end-user create a ticket

Navigate to http://localhost/osTicket/open.php

I have created a ticket as karen describing an online banking system being down:

![image](https://github.com/user-attachments/assets/c958b676-fa5a-4adb-b16b-f5f13600559e)

### As a Help Desk Agent, observe the ticket’s properties

Navigate to http://localhost/osTicket/scp/login.php

login as agent John Doe:  

Username: `john`  
Password `osTicketPassword123!`

#### Observe the ticket end-user karen created

As you can see everything is set to default including "assigned to" and SLA

![image](https://github.com/user-attachments/assets/13722557-2a17-443e-b6b8-5aa049626918)

Because of the severity of this ticket mainly because end users can't access a system (online banking) I will configure the following: 

Update the SLA Plan to Sev-A the most severity SLA so the issue will be worked on ASAP

![image](https://github.com/user-attachments/assets/cadbffb7-c6c3-4119-9d15-f7e05b04c6e6)


Update the help topic to "Business Critical Outage" because "Report a prolbem" isnt as relevant for this ticket

![image](https://github.com/user-attachments/assets/101aed75-c2b5-47e6-bef0-015516d85894)

Next I will assign the ticket to the online banking team

![image](https://github.com/user-attachments/assets/905071a0-7394-4388-bf8a-d601668807dd)

Now let observe the changes made: 

As you can see towards the bottom a log was created for each entry we changed 

![image](https://github.com/user-attachments/assets/5c562c96-aafe-41eb-aee7-93630bea81ce)

### login as jane and work the ticket

Now we will be simulating jane who is on the online banking team and we will work the ticket

logout as john and log back in as jane
 
username: `jane`  
password: `osTicketPassword123!`  

Even though john assigned the ticket to the online banking team lets reassign it to jane because she will working the ticket

![image](https://github.com/user-attachments/assets/9738e64f-7431-4bb6-899a-02c55aa8f1bc)

Jane will now update the customer/end-user on what she suspects the problem might be keeping the customer in the loop and letting the customer know that thier inquiry is being looked into

![image](https://github.com/user-attachments/assets/5aa0ff92-c029-4e67-87d1-04d377291cde)

In this made up scenario Jane was right it was the update that was preventing users from logging in and she rolled the update back so that the customers could access the banking systems

Now she will update the customer: 

![image](https://github.com/user-attachments/assets/8cb4d96b-6a37-41a9-af19-518d70fb244c)

Then she closes the ticket:

![image](https://github.com/user-attachments/assets/335ea23c-cd1e-40cd-99aa-b3d3deb082b4)


### Observe the completed ticket:

As you can see osTicket created a log of all the communications and status changes when we worked the ticket

![image](https://github.com/user-attachments/assets/fb9f7400-b4ca-49e2-91ce-22040575aacf)


Thats it for this lab we have successfully created and worked a ticket to completion!



