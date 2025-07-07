# Vehicle Management

# Project Title

The project is a comprehensive web-based application designed to streamline and automate the process of managing vehicle maintenance, repairs, and service history. 


## Functions
### Customer
* Customer will signup and login into system
* Customer can make request for service of their vehicle by providing details (vehicle number, model, problem description etc.)
* After Request approved by admin, customer can check cost, status of service
* Customer can delete request (Enquiry) if customer change their mind or not approved by admin (ONLY PENDING REQUEST CAN BE DELETED )
* Customer can check status of Request(Enquiry) that is Pending, Approved, Repairing, Repairing Done, Released
* Customer can check invoice details or repaired vehicles
* Customer can send feedback to admin
* Customer can see/edit their profile

### Mechanic
* Mechanic will apply for job by providing details like (skills, address, mobile etc.)
* Admin will hire(approve) mechanic account based on skill
* After account approval, mechanic can login into system
* Mechanic can see how many work (vehicles to repair) is assigned to me
* Mechanic can change status of service ('Repairing', 'Repairing Done') according to work progress
* Mechanic can see salary and how many vehicles he/she have repaired so far
* Mechanic can send feedback to admin
* Mechanic can see/edit their profile

### Admin
* First admin will login (for username/password run following command in cmd)
```
py manage.py createsuperuser
```
* Give username, email, password and your admin account will be created.
* After login , admin can see how many customer, mechanic, recent service orders on dashboard
* Admin can see/add/update/delete customers
* Admin can see each customer invoice (if two request made by same customer it will show total sum of both request)
* Admin can see/add/update/delete mechanics
* Admin can approve(hire) mechanics (requested by mechanic) based on their skills
* Admin can see/update mechanic salary
* Admin can see/update/delete request/enquiry for service sent by customer
* Admin can also make request for service (suppose customer directly reached to service center/office)
* Admin can approve request for service made by customer and assign to mechanic for repairing and will provide cost according to problem description
* Admin can see all service cost of request (both approved and pending)
* Admin can see feedbacks sent by customer/mechanic

### Others features
* We can change theme of website: Dark mode and Light mode
* If customer is deleted by admin then their request(Enquiry) will be deleted automatically

## Screenshots
### Homepage
![homepage ss](https://github.com/cryptic-vedant/vehiclemanagement/vehicle management/static/screenshots/home.png?raw=true)
### Admin
![admin dark](https://github.com/cryptic-vedant/vehiclemanagement/vehicle management/static/screenshots/admin_dark.png?raw=true)

![admin light](https://github.com/cryptic-vedant/vehiclemanagement/vehicle management/static/screenshots/admin_light.png?raw=true)

## HOW TO RUN THE PROJECT
* Install Python(3.7.6) (Dont Forget to Tick Add to Path while installing Python)
* Open Terminal and Execute Following Commands :
```
python -m venv myenv
myenv\Scripts\activate
pip install django==3.0.5
pip install django-widget-tweaks
pip install pillow
py manage.py
```
* Download This Project Zip Folder and Extract it
* Move to project folder in Terminal. Then run following Commands :
```
py manage.py makemigrations
py manage.py migrate
py manage.py runserver
```
* Now enter following URL in Your Browser Installed On Your PC
```
http://127.0.0.1:8000/
```
## CHANGES REQUIRED FOR CONTACT US PAGE
* In settings.py file, You have to give your email and password
```
EMAIL_HOST_USER = 'youremail@gmail.com'
EMAIL_HOST_PASSWORD = 'your email password'
EMAIL_RECEIVING_USER = 'youremail@gmail.com'
```
* Login to gmail through host email id in your browser and open following link and turn it ON
```
https://myaccount.google.com/lesssecureapps
```

