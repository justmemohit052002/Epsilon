
# Epsilon App
 
Epsilon app is a cross-platform mobile application that has been developed using React Native for the frontend and Django for the backend, with REST APIs serving as the connectivity layer. The app is designed to provide home tutor services to special and disabled students, catering to their specific needs and requirements.

The frontend of the app has been developed using React Native, which is a popular open-source framework for building mobile applications for both Android and iOS platforms. It allows for the creation of a responsive and visually appealing user interface, which is essential for providing an engaging user experience.

On the other hand, the backend of the app has been developed using Django, which is a high-level Python web framework that facilitates rapid development and clean, pragmatic design. It provides a range of tools and libraries for building scalable and secure web applications, making it an ideal choice for the Epsilon app.

The REST APIs serve as the connectivity layer between the frontend and backend of the app, allowing for seamless communication and data exchange. The APIs have been designed to be fast, efficient, and easy to use, ensuring that the app provides a smooth user experience.

Overall, the Epsilon app is a powerful and versatile mobile application that leverages the best of React Native and Django to provide a reliable and user-friendly solution for special and disabled students who require home tutor services.expertise.

 

 


 


 
## Acknowledgements

React Native framework for enabling the development of cross-platform mobile applications.

Third-party libraries and tools used in the development process, such as Redux for state management or Axios for HTTP requests.

Design resources used to create the user interface, such as icons, fonts, and color palettes.

Testing and debugging tools used to ensure app quality, such as Jest or React Native Debugger.

Open-source projects or code snippets used as a reference or inspiration for specific features.

Contributions and support from other team members or stakeholders involved in the project.

## API Reference

 Epsilone Auth

  //creat_user:
  //Creates a new managed user in an enterprise. This endpoint is only    available to users and applications with the right admin permissions.

    {
    "email":"gwar619908@gmail.com",
    "name" :"Piyush Khanchandani",
    "password" : "Piyush1234",
    "re_password":"Piyush1234"

    }

// active_user:

//An API for activating a user would typically involve sending an activation link to the user's email address. The activation link would contain a unique token or code that would be used to verify the user's identity and activate their account.


    {
    "uid":"Mg",
    "token": "biplkd-7c250b1b60748d06117c0352e95f9226"
        
    }

//get token:
//An API for getting tokens would typically involve exchanging a user's credentials for an access token and a refresh token. The access token is used to authenticate subsequent API calls, while the refresh token is used to obtain a new access token when the current one expires.
    
    {
    "email":"gwar619908@gmail.com",
    "password": "Piyush1234"

    }

//new_token_acess
//An API for obtaining a new access token would typically involve sending a refresh token to the API in exchange for a new access token. The refresh token is a long-lived token that is used to obtain new access tokens when the current one expires. This approach helps to prevent the need for the user to constantly re-enter their credentials.
     
    {
    "refresh":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTY3NDkyOTgyOCwianRpIjoiN2ZlZTcwOTllMDY1NDUzOTgzZDRiMTY5N2ZhMzUzM2QiLCJ1c2VyX2lkIjoyfQ.coP0gJI3yO9lFtS3cZS_CffsCqgzzloapviLcjwoAoE"

    }

//verify_user: 

//The "verify user" API is used to verify the email address of a user.
    
    {

    "token":""
    }

//user reset password confirm

//The API may verify the token to ensure that it is valid and that it matches the user who requested the password reset.
    {
    "uid":"MQ",
    "token":"birc23-7a09b68eedabdb1e1291675fafbdf382",
    "new_password":"Piyush123456",
    "re_new_password":"Piyush123456"
    }

//reset password request
//The "reset password request" API is used when a user has forgotten their password and wants to reset it 
   
    {
   
    "email":"piy42k@gmail.com"

    }

EpsiloneRagistration

   //Teacher_registration:

   //The "teacher_registration" API is used to register a new teacher in a system.
The API typically provides endpoints that enable clients to interact with the application and perform actions such as creating new teacher records, retrieving teacher data, and updating teacher information.

    {
    Name:Piyu
    Email:ddacnj@gmail.com
    Gender:Male
    Experience:5 years
    Date_of_Birth:2019-1-1
    Addrese:dssadjsakb
    Expert_IN:asda
    Payment:10000
    }

  //Student_Registration
  //The "Student registration" API is used to register a new Student in a system.
The API typically provides endpoints that enable clients to interact with the application and perform actions such as creating new student records, retrieving student data, and updating student information.
    
    {
    Name:Poy
    Gender:Male
    Date_of_Birth:2012-1-2
    Desability:D_747
    Education_level:12th
    }

  //Post_Student_Disabilitys:
 
 //that allows students with disabilities to choose the accommodations and support services they need in order to succeed in their academic endeavors.
  
    {
    Category:Two
    Disabilitys:ISL
    }

  //Gardian_Registration:

  //a guardian registration API is a tool that streamlines the process of establishing legal guardianship and enables authorized parties to access and manage important information related to the minor or incapacitated individual

    {
    S_id:S_338
    G_Name:Meeeee
    contact_number:+919876787876
    Relationship:Father
    Gender:Male
    Addresse:asdadas
    gmail:kkd@asd.com
    }
  //Post_FingerPrint
//it is an API that provides developers with the necessary tools and functions to enable users to register their fingerprints within an application. This can be useful in a variety of contexts, such as secure authentication or biometric identification. 
    
    {
    Date:2023-12-2
    T_id:
    Start_time:
    End_time:
    }

//Request_to_Teacher

// These api deals with all requests made by students to the teacher .
    
    {
    S_id:S_628
    T_id:T_100
    }

//Help_Genrate

//it allows users of an application to request assistance from an administrator, and enables the administrator to manage and respond to those requests.

    {
    ids:S_12
    Messsage:hii Admin I need This Help
    }
## Features

The app has the following features:
```
•	User authentication (login and registration)
•	Search for tutors based on location and subject
•	View tutor profiles and their availability
•	Schedule and book tutor sessions
•	In-app chat for communication between students and tutors
•	Payment processing for tutor services

```
## Environment Variables

 You can do it by importing os and creating a .env file where you will specify all the database details for connection.

settings.py file:

    import os
    DATABASES = {
    "default": {
    "ENGINE": "django.db.backends.postgresql",
    "NAME": os.environ.get('DB_NAME'),
    "USER": os.environ.get('DB_USER'),
    "PASSWORD": os.environ.get('DB_USER_PASSWORD'),
    "HOST": os.environ.get('DB_HOST'),
    "PORT": os.environ.get('DB_PORT'),
    }
    }
.env file:

    export DB_NAME = dbname
    export DB_USER = root
    export DB_USER_PASSWORD = root
    export DB_HOST = localhost
    export DB_DB_PORT = 5432
1.	Clone the repository from Github.
2.	Install the required dependencies for the frontend using npm install.
3.	Create a virtual environment for the backend using python -m venv env.
4.	Activate the virtual environment using source env/bin/activate.
5.	Install the required dependencies for the backend using pip install -r requirements.txt.
6.	Create a PostgreSQL database for the app and update the database configuration in settings.py.
7.	Migrate the database schema using python manage.py migrate.
8.	Run the Django server using python manage.py runserver.
9.	Run the React Native app using npm start.

## Prerequisites

```
•	Node.js
•	Python 3
•	MySQL
•	Django
```
## Technology Stack


The app has been developed using the following technologies:

    •	React Native for the frontend
    •	Django for the backend
    •	REST APIs for connectivity between frontend and backend
    •	PostgreSQL as the database management system
    •	Google Maps API for location-based search

## Configuration

•	The app requires Google Maps API credentials for location-based search. Add your API key to the .env file in the frontend directory.
•	The backend server URL is defined in the constants.js file in the frontend directory.

## Deployment

The app can be deployed to a cloud hosting service such as AWS or Google Cloud. To deploy the app, follow these steps:
```
1.	Set up a virtual machine instance on your cloud hosting service.
2.	Install the required software on the virtual machine (Node.js, Python 3, PostgreSQL).
3.	Clone the repository onto the virtual machine.
4.	Install the required dependencies for the frontend and backend.
5.	Update the database configuration and API credentials as necessary.
6.	Run the Django server using a production-grade web server such as Gunicorn or uWSGI.
7.	Build the React Native app for production and deploy to the app stores.

```


## Screenshots

![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)


## Conclusion

```
This cross-platform app provides home tutor services to special and disabled students, and has been developed using React Native for the frontend and Django for the backend with REST APIs serving as the connectivity layer. With its easy-to-use interface, location-based search, and payment processing, the app is designed to provide an optimal user experience.


```