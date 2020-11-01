# Logger Design

## Story
Production systems usually need to record user behavior and provide self (or manager) to trace the behavior of (someone) at certain times.
So provide simple log back-end library and front-end page examples.

---

## Use Case
### Log action
Log user's behavior when he do any action on system.


### View self-behavior records
- Joe wants to find his actions on last night, he goes to specific page and searches for data by date range.
- He wants to see information as: datetime, user, function, action, status, message.

#### Collection
- list page, has search form as date range, sort
- fields: datetime, user, function, action, status, message
- Data permission for user
- Support search for "user" field. but user can only select himself.
- Support search for "data time range" field.

### View someone's behavior record as an administrator
- The manager wants to find Joe's 10 o'clock action, he needs to go to the behavior record page to search for data.

#### Collection
- Data permission for manager
- Support search for "user" field.

### Export behavior records
- Joe wants to search for someone's behavior record and export it to excel.

#### Collection
- send export signal with search parameter.
- Excel builder.

### Data isolation
- Joe is normal user, he can only search his own data, but cannot get other people's data.
- Mars is a manager, he can search the data of everyone under his leadership.
- Eric is the manager of another company, and he cannot search Joe's data.

#### Collection
- Data permission for manager,user.
- Data isolation through company feature.

### Search logs for specific features
- Joe wants to search for his behavior data in the member center.

#### Collection
- Support search for "function" field.

### Log rotate
- After a period of time, the behavior data will be automatically deleted.

#### Collection
- A schedule tools, it will delete old data and running as schedule.

---

## Requestment
- list page.
- add, read, export, search, sort, pagination.
- fields: datetime, user, function, action, status, message.
- Permission for Organization.
- Data isolation by Permissions and Organizations.

---

## Affect


---

## Functions & Flows

### Log view
- A page for user to view log data.
- Element: List table, Search form, Export button

### Log library
- A library which Provide function to add, read, export, rotate


---

## Pages

---

## Data formate

---

## Interfases

---

## Libraries

---

## Tasks

---

## Test Items

---

## Reference

---

## Logs



