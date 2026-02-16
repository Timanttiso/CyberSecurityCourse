### **Guest**

---

**✅ Can do**

List every action a *Guest* can perform, with the page or endpoint.
* Can view frontpage `/`
* Can view register page `/register`
* Can register a new user `/register`
* Can view log-in page `/login`
* Can log-in as an already existing user `/login`



---

**❌ Cannot do**

List every action that a *Guest* is blocked from doing.



---

### **Reserver**

---

**✅ Can do**

List actions a *Reserver* can do according to specs + actual test results.
Include visible pages **and** API endpoints.

* Can view frontpage `/`
* Can view login page `/login` Note: This should not happen, instead it should redirect to the fronpage(bug).
* Can log-in as an already existing user `/login` Note: should also not happen(bug).
* Can view register page `/register` Note: This should not happen(bug).
* Can view add resources page `/resources`
* Can add resources `/resources`
* Can view create reservations page `/reservation`
* Can make reservations `/reservation` Note: user can also make reservations to the past(bug/unintended feature)
* Can edit own reservations `/reservation?id` Note: In update view user can also change the reservation name to be someone else besides themselves allowing them to make reservations for others, which is a flaw in authorization(bug).
* Can logout of user `/logout`

---

**❌ Cannot do**

List actions a *Reserver* is correctly blocked from.



---

### **Administrator**

---

**✅ Can do**

List actions an *Administrator* can perform.

* Can view frontpage `/`
* Can view add resources page `/resources`
* Can add resources `/resources`
* Can edit resources `/resources?id`
* Can make reservations `/reservation` Note: user can also make reservations to the past(bug/unintended feature)
* Can edit reservations `/reservation?id`
* Can delete reservations `/reservation?id`
  

---

**❌ Cannot do**

List prohibited behaviors, if any, or incorrect implementation issues.

* Cannot delete resources, from the log it seems that this is because the resource is tied to a reservation as a foreign key, this is proplematic, since from what I can tell you are not able to access the resources in the UI from anywhere else besides the reservations and that would mean it is always tied to a reservation. (poorly implemented feature) `/resources?id`

