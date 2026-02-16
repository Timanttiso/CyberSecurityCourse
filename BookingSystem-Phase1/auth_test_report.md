### **Guest**

---

**✅ Can do**

List every action a *Guest* can perform, with the page or endpoint.
* Can view frontpage and reservations `/`
* Can view register page `/register`
* Can register a new user `/register`
* Can view log-in page `/login`
* Can log-in as an already existing user `/login`
* Can view resources page and add resources `/resources` Note: Should not happen and is a flaw in authorization(bug)



---

**❌ Cannot do**

List every action that a *Guest* is blocked from doing.
* Cannot access reservation page `/reservation`
* Cannot access reservation edit page `/reservation?id`
* Cannot access resources edit page `/resources?id`


---

### **Reserver**

---

**✅ Can do**

List actions a *Reserver* can do according to specs + actual test results.
Include visible pages **and** API endpoints.

* Can view frontpage and reservations `/`
* Can view login page `/login` Note: This should not happen, instead it should redirect to the fronpage(bug).
* Can log-in as an already existing user `/login` Note: should also not happen(bug).
* Can view register page `/register` Note: This should not happen(bug).
* Can register a new user `/register` Note: This should not be possible(bug).
* Can view add resources page `/resources`
* Can add resources `/resources`
* Can view create reservations page `/reservation`
* Can make reservations `/reservation` Note: user can also make reservations to the past(bug/unintended feature)
* Can edit and delete own reservations `/reservation?id` Note: In update view user can also change the reservation name to be someone else besides themselves allowing them to make reservations for others, which is a flaw in authorization(bug).
* Can logout of user `/logout`
* Can edit and delete resources `/resources?id` Note: This is unintended and while the user is blocked from opening the edit resource page in the UI they can still just enter the parameter ?id and the right id into the URL and get to the edit page. This is a failure of authorization(bug). Also user can open already deleted resources to edit, which is also a bug(bug)
* Can edit others reservations `/reservation?id` Note: As a reserver you are blocked in the UI from accessing the editing page of other people's reservations. This is easily side stepped by just editing the URL parameter to have the other person reservation's id and you are able edit it. Problem with authorization(bug).

---

**❌ Cannot do**

List actions a *Reserver* is correctly blocked from.
* Cannot delete other people's reservations. Note: you are still able to delete other people's reservations by changing the reserver of the reservation to your profile and then editing and clicking delete. You can change reserver by the before mentioned manner of being able to access the edit page of another person's reservation, so this does not work perfectly(bug).


---

### **Administrator**

---

**✅ Can do**

List actions an *Administrator* can perform.

* Can view frontpage and reservations `/`
* Can view login page `/login` Note: This should not happen, instead it should redirect to the fronpage(bug).
* Can log-in as an already existing user `/login` Note: should also not happen(bug).
* Can view register page `/register` Note: This should not happen(bug).
* Can register a new user `/register` Note: This should not be possible(bug).
* Can view add resources page `/resources`
* Can add resources `/resources`
* Can edit resources `/resources?id` Note: seems to also work on already deleted resources, which should not happen(bug).
* Can make reservations `/reservation` Note: user can also make reservations to the past(bug/unintended feature)
* Can edit reservations `/reservation?id` 
* Can delete reservations `/reservation?id`
* Can logout of user `/logout`

---

**❌ Cannot do**

List prohibited behaviors, if any, or incorrect implementation issues.

* Cannot delete resources correctly. From the log it seems that this is because the resource is tied to a reservation as a foreign key. This is proplematic, since from what I can tell you are not able to access the resources in the UI from anywhere else besides the reservations and that would mean it is always tied to a reservation. Resources can be deleted if they are not linked to any reservation and you access the page by editing the URL (poorly implemented feature) `/resources?id`

