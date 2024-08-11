## FlightBooking App

### Tech Stack: 

    1. Backend: Django 
    3. Data Base : Postgres (hosted)

### Note : These Apis Are deployed and Postgres Data Base is also Deployed.

### NOTE : ( If DB not working then Please refer Git repo metioned Below as may be the free postgres version might get expired)

### Git repository : https://github.com/Prashant-Bhatt-2000/FlightNotify

### Authentication : Multi user (Admin , Customer)

### Project Setup 

    1. Git Clone : git clone https://github.com/Prashant-Bhatt-2000/FlightNotify_Backend.git

    2. Download requirement.txt: 

---


### API's

    Authentication APIs : 

    Admin Signup : 

        API : https://flightnotify-backend.onrender.com/api/accounts/adminsignup

            data :{ 
                "username": "Prashant", 
                "email": "bhatt.prashant2018@gmail.com", 
                "password": "Password"
            }
    
    Note : You can't sign in without verifying email.

    Admin Signin : 

        API : https://flightnotify-backend.onrender.com/api/accounts/adminsignin

            data :{ 
                "email": "bhatt.prashant2018@gmail.com", 
                "password": "Password"
            }

    
    Customer Signup : 

        API : https://flightnotify-backend.onrender.com/api/accounts/customersignup

            data :{ 
                "username": "Prashant", 
                "email": "bhatt.prashant2000@gmail.com", 
                "password": "Password"
            }
    
        Note : You can't sign in without verifying email.
    
    Customer Signin : 

        API : https://flightnotify-backend.onrender.com/api/accounts/customersignin

            data :{ 
                "email": "bhatt.prashant2018@gmail.com", 
                "password": "Password"
            }


<!-- TOKEN NEEDED FOR SIGNOUT -->
 <!-- Bearer <TOKEN> -->
    Customer SIgnout: 

        API: https://flightnotify-backend.onrender.com/api/accounts/customersignout
---



### FlightOperations

    <!-- TOKEN NEEDED for all Flight Operations -->
    <!-- Bearer <TOKEN> -->

    ADMIN ONLY ROUTE : 

    Create Flight : 
             
        API : https://flightnotify-backend.onrender.com/api/flight/createflight

        Data : { 
            origin: newFlight.origin,
            destination: newFlight.destination,
            departure_time: newFlight.departure_time,
            arrival_time: newFlight.arrival_time,
            status: newFlight.status
        }


    UpdateFlight: 

    API : https://flightnotify-backend.onrender.com/api/flight/updateflight/<str:flight_id>

    Data : { 
            origin: origin,
            destination: destination,
            departure_time: departure_time,
            arrival_time: arrival_time,
            status: status
        }

        Onevery change the Customers who booked that flight will get an email


    
    Customer: 

    Bookflight : 
    API : https://flightnotify-backend.onrender.com/api/flight/bookflight

    Data : { 
        flight_number: flight_number,
        seats: seats,
        departure_city: origin,
        arrival_city: destination,
        departure_date: departure_time,
        arrival_date: arrival_time,
    }


    Get Flights : 

    API : https://flightnotify-backend.onrender.com/api/flight/getflights



    MyBookings : 

    API : https://flightnotify-backend.onrender.com/api/flight/mybookings

----
