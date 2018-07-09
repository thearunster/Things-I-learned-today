# CQRS - Command Query Responsibility Segragation

CQRS is simply the creation of two objects where there was previously only one. The separation occurs based upon whether the methods are a command or a query (the same definition that is used by Meyer in Command and Query Separation, a command is any method that mutates state and a query is any method that returns a value).

When most people talk about CQRS they are really speaking about applying the CQRS pattern to the object that represents the service boundary of the application. 

Consider the following pseudo-code service definition:

### CustomerService

```c#
void MakeCustomerPreferred(CustomerId);
Customer GetCustomer(CustomerId);
CustomerSet GetCustomersWithName(Name);
CustomerSet GetPreferredCustomers();
void ChangeCustomerLocale(CustomerId, NewLocale);
void CreateCustomer(Customer);
void EditCustomerDetails(CustomerDetails);
```
 

Applying CQRS on this would result in two services:


### CustomerWriteService

```c#
void MakeCustomerPreferred(CustomerId);
void ChangeCustomerLocale(CustomerId, NewLocale);
void CreateCustomer(Customer);
void EditCustomerDetails(CustomerDetails);
```

### CustomerReadService

```c#
Customer GetCustomer(CustomerId);
CustomerSet GetCustomersWithName(Name);
CustomerSet GetPreferredCustomers();
```
