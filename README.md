# aLLBALL

A two-sided, video-streaming marketplace platform that features credit card payment capabilities, user role management, complex user interfaces, and advanced database relationships.

<img src="images/index.PNG">

## Database Architecture

Created five tables within a PostgreSQL database (courses, enrollments, lessons, sections & users).
  > A Course belongs to a User, and has many Sections and Enrollments. <br />
  > Enrollments belong to both a Course & a User. <br />
  > Lessons belong to a Section. <br />
  > Thus a Section belongs to a Course and also has many Lessons. <br />
  > Users will have many Courses, Enrollments and Enrolled Courses (keep track of courses the user is enrolled in). <br />

## RESTful Routing w/ CRUD actions

Created two branches of entry into a Course (Instructor & Student) using a namespace. <br />
  > This allows for two different views of the same Course (edit & read only) privledges. <br />
      &nbsp;&nbsp; /instructor/courses/1 (edit) <br />
      &nbsp;&nbsp; /courses/1 (read only) <br />
  > The ability to Enroll in a course is routed only through a Course. <br />
  > Both privledges react the same when navigating to Lessons & Sections. <br />

## Courses/Lessons

<img src="images/courses.PNG" width="434"> <img src="images/lessons.PNG" width="434">

  > instructor can sort Lessons & Sections with Drag 'n Drop Functionality.

## Authentication/eCommerce

<img src="images/auth.PNG" width="434"> <img src="images/payment.PNG" width="434">

## Video Player

<img src="images/vid.PNG">

## Deployment

* [https://allball-app.herokuapp.com/](https://allball-app.herokuapp.com/)


## Tech

* [Ruby](https://www.ruby-lang.org/en/documentation/) v: 2.5.3
* [Rails](https://rubyonrails.org/) - v: 5.2.3
* [Bootstrap](https://getbootstrap.com/docs/4.4/getting-started/introduction/) - v: 4.0.0.alpha6
* [jQuery](https://jqueryui.com/download/) - v: jQuery-rails
* [postgreSQL](https://www.postgresql.org/) - Database
* [Heroku](https://devcenter.heroku.com/) - Deployment

## Built With
* [jQuery Sortable](https://jqueryui.com/sortable/) - Drag 'n Drop functionality
* [Stripe](https://stripe.com/docs) - Used for eCommerce capability
* [Carrierwave](https://github.com/carrierwaveuploader/carrierwave) - File uploads
