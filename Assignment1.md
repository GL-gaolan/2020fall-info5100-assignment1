# Assignment1

##1.A course management system
*-Student*<br>
*   Data: StudentId StudentName Age Gender Phone emailAddress Major Department requiredCourse optionalCourse <br>
*   Behavior: Login Logout Search uploadAssignment 

*-Teacher*<br>
*   Data:TeacherId TeacherName Age Gender Phone emailAddress Major Department teachCourse<br>
*   Behavior:Login Logout Search sendMessage Grade publicAssignment
     
*-Online course registration system*<br>
*   Data:Courses<br>
*   Behavior:alertDdl checkOut remind
    
*-Courses*<br>
*   Data: courseId Name Teacher Schedule Assignments Syllabus<br>
*   Behavior:<br>

*-Assignment*
*   Data: assignNumber,ddl,requirements
*   Behavior:

>```java
>Student bonnie;
>Teacher siva;
> OnlineCourseRegistrationsystem canvas;
>bonnie.login(studentId);
>siva.login(teacherId);
>Course info5100=bonnie.search(courseId,name,teacher);
>Assignment assignment1=siva.publicAssignment(courseId,assignNumber,ddl,requirements);
>if assignment1 ddl is nextday& bonnie does not upload her assignment1
>    canvas.alertDdl(bonnie.emailAddress);
>    bonnie.uploadAssignment(assignment1);
>    canvas.remind(siva.emailAddress);
>    siva.grade(assignment1);
>    canvas.remind(bonnie.emailAddress("Your assignment1 has been graded."));
>else canvas.remind("assignment1 has been created"); 

##2.A pet adoption platform
*-Adopter*
*   Data:Id,Name,Age,Gender,MHI,Ownedpet,emailAddress,Phone,Address
*   Behavior:login,logout,search,requestAdopt,requestCancle,search

*-Pet*
*   Data:Id,Breed,Name,Age,Gender,recommendadoptercondition,pic
*   Behavior:

*-PetAdoptionPlatform*
*   Data:pets
*   Behavior:checkOut,sendReceipt,refund,sendtoPetnursinghome,sendFailemail,showPetinfo

*-PetNursingHome*
*   Data:pets,adopters
*   Behavior:contactadopter
>```java
>Adopter bonnie;
>PetAdoptionPlatform lovePetApp;
>PetNursingHome petHome;
>bonnie.login(id);
>Pet dollar = bonnie.search(id,breed,age,gender);
>lovePetAPP.showPetinfo(id,breed,name,age,gender,recommendadoptercondition,pic);
>if bonnie.MHI & bonnie.Ownedpet meet the request of dollar.recommendadoptercondition
>   bonnie.requestAdopt(dollar);
>   lovePetApp.checkout(bonnie.emailAddress,bonnie.phone,bonnie.address);
>   lovePetApp.sendReceipt(bonnie.emailAddress);
>   if bonnie change her mind
>        bonnie.requestCancle(dollar);
>        lovePetApp.refund(dollar,bonnie);
>    else
>        lovePetApp.sendtoPetnursinghome(dollar,bonnie);
>        petHome.contactadopter(bonnie.phone);
>else sendFailemail(bonnie.emailAddress);   

##3.An app to book airline ticket
*-Passager*
*   Data:emailAddress, Name, loginCredentials, Address, Phone, credit card
*   Behavior:logIn, Pay, writeReview, requestCancelOrder, requestRefund, Search

*-AirlineCompany*
*   Data:Airlines
*   Behavior:

*-Airline ticket booking App*
*   Data:AirlineCompanies,Airlines,Passagers
*   Behavior:remindlate,sendReceipt, checkOut, refund, sendToAirlineCompany

*-Airline*
*   Data:AirlineNumber,Company,Price,DepartureTime,ArrivelTime,OriginStation,ArrivalStation
*   Behavior:

>```java
>Passager bonnie;
>AirlineCompany southernAirlinesCompany;
>AirlineticketBookingApp ctripApp;
>bonnie.login(loginCredentials);
>Airline beijingToShanghai = bonnie.search(AirlineNumner,departureTime,arrivelTime,originStation,arrivalStation);
>if beijingToShanghai haveset
>   emma.pay(bejingToShanghai);
>   ctripApp.checkOut(bonnie.emailAddress,bonnie.phone,bonnie.creditCard);
>   ctripApp.sendReceipt(bonnie.emailAddress);
>   if bonnie change her mind;
>        bonnie.requestCancelOrder(bejingToShanghai);
>        ctripApp.refund(bejingToShanghai,bonnie);
>    else
>        ctripApp.sendToAirlineCompany(bejingToShanghai,bonnie);
>        southernAirlinesCompany.contactPassager(bonnie.emailAddress);
>    if bejingToShanghai not delay
>        bonnie.writeReview("*****");
>    else 
>        emma.writeReview("ooooo");
>        emma.requestRefund(bejingToShanghai, ctripApp);
>        ctripApp.refund(bonnie);
>else ctripApp.remind("Sorry,No set for bejingToShanghai.")

##4.A course registration platform
*-Student*<br>
*   Data: StudentId StudentName Age Gender Phone emailAddress Major Department requiredCourse optionalCourse <br>
*   Behavior: Login Logout Search registeCourse dropCourse sendMessage

*-Teacher*<br>
*   Data:TeacherId TeacherName Age Gender Phone emailAddress Major Department teachCourse<br>
*   Behavior:Login Logout Search courseAssign addStudent courseDrop sendMessage
    
*-Online course registration system*<br>
*   Data:Courses<br>
*   Behavior:ddlAlert overflowAlert sentSuccessemail sentFailemail checkOut
    
*-Courses*<br>
*   Data: courseId Name Teacher Capacity Schedule<br>
*   Behavior:<br>

>```java
>Student bonnie;
>Teacher siva;
>Online course registration system myNEU;
>siva.login(teacherId);
>siva.courseAssign(infor5100);
>canvas.sentSuccessemail(siva.emailAddress);
>bonnie.login(studentId);
>Courses info5100 = bonnie.search(courseId,Name,Teacher,Capacity,Schedule); 
>if info5100 havevacancy
>    bonnie.registeCourse(ainfo5100);
>    myNEU.checkOut(emma.studentId,emma.emailAddress,emma.phone,info5100.teacher,infor5100.schedule);
>    myNEU.sentSuccessemail(bonnie.emailAddress);
>    if bonnie change her mind  
>        bonnie.dropCourse(info5100);
>else 
>   canvase.sentFailemail(bonnie.emailAddress);

###5.A food delivery app(Like Uber Eats)
*-Customer*
*   Data:emailAddress, Name, loginCredentials, Address, Phone, credit card
*   Behavior:login, orderFood,search,Pay, writeReview, requestCancelOrder, requestRefund

*-Restaurant*
*   Data:name,Dishes,Address,Phone
*   Behavior:contactConsumer

*-food delivery app*
*   Data:Restaurants,Couriers
*   Behavior:allocateCourier,deliver,sendReceipt, checkOut, refund, sendToRestaurant

*-Couriers*
*   Data:Id,Name,Phone,Gender
*   Behavior:contactConsumer,login,deliver

>```java
>Customer bonnie;
>Restaurant panda;
>FooddeliveryApp uberEats;
>bonnie.login(loginCredentials);
>Restaurant panda=bonnie.search(name,dish,address);
>bonnie.orderFood(panda,dish);
>uberEats.checkOut(bonnie.address,bonnie.phone,bonnie.creditCard);
>uberEats.sendReceipt(bonnie.phone);
>if bonnie change her mind
>   bonnie.requestCancelOrder(panda,dish);
>   uberEats.refund(panda,dish,bonnie);
>else
>    Couriers justin=uberEats.allocateCourier(panda,dish,id,name,phone);
>    uberEats.sendToRestaurant(panda,dish,bonnie,justin);
>    justin.contactCustomer(bonnie);
>    jamie.deliver(panda,dish, emma.address);
>    if bonnie satisfied with the food
>        bonnie.writeReview("*****");
>    else
>        bonnie.writeReview("ooooo");
>        bonnie.requestRefund(panda,dish,uberEats);
>        uberEats.refund(bonnie);