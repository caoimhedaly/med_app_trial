# Medication Manager App

View the Med App [here](https://flask-med-app.herokuapp.com/).



 
## Introduction
 
This website is a CRUD app designed as a tool to help people manage medication. It can be used either for personal use or by a carer, as an aid to organise their patient's medications. 

It is often the case that on presenting to a medical practitioner, either GP or specialist, that patients do not have a list of their medications at hand. Many people are not aware of what medications they take regularly, who prescribed them, why or when. This makes it difficult for medical practitioners to alter patient medication. Similiarly it is difficult for the patient to adhere to their treatment plan. People are at a real risk not only of missing vital medication but also of overdosing on medication. 

Read below to find out how the Medication Manager App aims to reduce these risks and increase medication saftey and adherence. 


## Wireframe 

Click the link to view my wireframe for The Med App on [balsamiq](https://balsamiq.cloud/s3pki77/p4agro5).
 
 

 
## UX

As described above, the Med App is designed for personal or professional use, as an aid to manage medication. Below are some examples of potential user experiences. 

####Megan: I am a 41yr old woman and personal carer to my elderly mother, Mary, who has severe rheumatoid arthritis. Mary takes over 20 medications per day, with different medications due at different times each day. Her medication list changes frequently as she is in and out of hospital. It is difficult to keep track of her medications from one day to the next. The Med Manager app allows me to create a list of my mother's medications including doseage, administration time and even who the prescriber is. I can add and delete medications as needed and change the doseage. By clicking on the "NOW" link I know which medications Mary is due at any given time so it is less likely that I will give her the wrong medication or miss a dose. The Med Manager app has made taking care of my mother much easier and I feel more confident about managing her medications. 

####John: I am a 75yr old widower with some memory problems and heart troubles. I have to take lots of different medication every day for my high blood pressure. When I use the Med Manager App, it reminds me what day it is, what time it is and what medications i have to take at that time. I can check off my medications as i take them so i dont take the same medication twice by accident, which could be very dangerous for me. I can also check what date my prescription expires so I know in advance when I have to fill a new one. When i visit my GP or my cardiologist, I have an uptodate list of my medications with me. 
 
####Sarah: I'm a 35yr old emergency doctor. Often patients arrive to the emergency department alone or confused. It can be impossile to get a list of a patients medications outside of normal working hours. If a patient is using the Med Manager app, I can see exactly what medications they are taking and have a good idea of what illnesses they have. This saves time and allows for quicker and safer treatment. I can also update the list before the patient is discharged home to allow for any changes to medications in hospital. Overall the Med Manager App makes my job easier. 


## Features
 
### Existing Features

* Home page with clear, easy navbar links to website pages.
Parallax scrolling. 
A large 'lets go!' button on the centre of the homepage which will bring you directly to your medications due in real time. 
The homepage describes some features of the app with links to these features and hover-sweep-to-bottom effect. 
Writing overlays a grayscale picture of an elderly gentleman using the app. 

* The 'NOW' link will bring the user to a page displaying real-time date, day and time with a clear list of mediations due with doseage. The user can clear the list after they have taken the medication and click the 'show medication list' button if they wish to see the list again.

* The 'Add Medication' link in the navbar will render a form to add a new medication. This includes a pop up calendar to save the date prescribed and discontinued.

* Edit Medications- this link will bring you to a list of all current medications. When each individual medication is clicked on, an accordian opens to reveal all details of that medicatiion. An edit and delete button will appear. The edit button will bring you to a form prefilled with that medication's details. You can now change any details and save the form to save the changes. Alternatively you can click the delete button to delete the medication from the list (and from the database).
This page also has a large red button which will bring you to the 'add medication' page. 

* The "Week" link in the navbar will navigate to a list of medications by day and time. By clicking on each day an accordian will open with medications divided into subsections of morning, afternoon, evening and night. 

* I used @media query to adjust text size according to VPW to make the website more responsive. 


### Features Left to Implement

- Ideally i would like to create a second collection in the database that would hold 'deleted medications' for future reference. 
- I would like to have a further collection which would hold a patient medication allergy list. 
- I would like to implement a function so that medications that are past 'date discontinued' would move to a separate collection, again for future reference. 

## Tech Used

### Some of the tech used includes:
- **HTML**, **CSS** , **python**,  **JQuery**

[FLASK](http://flask.pocoo.org)
  - I used the framework flask and jinja2 templating for python. 
  - Flask allowed me to build my web app quickly and easily. 
  
[Jinja2](http://jinja.pocoo.org/docs/2.10/)
 - Jinja is easy to debug, has ahead-of-time compilation and sandboxed template execution. 
  
[MongoDB](https://www.mongodb.com/)
[PyMongo](https://api.mongodb.com/python/current/)
   - I used PyMongo to work with my database in MongoDB
   - MongoDB allows me to store my data in familiar, json-like documents. 
   - I was able to changes the structure of my data as the application developed and I added new features. It will also make it easy to add new features in future. 
 

[JQuery](https://jquery.com)
- I used jquery  for the following functions:
1. sidebar nav which is collapsible
2. 'hide'and 'show' function to hide and display medication list onclick
3. 'datepicker' for the pop up calendar
4. 'select' to select days of the week for drug administration
    

[Materialize](https://materializecss.com/about.html)
- I used Materialize as an alternative to bootstrap to give a simple responsive layout.


[Balsamiq](https://balsamiq.com/)
- I used Balsamiq cloud to create my mockup. 


## Libraries:

- Fontawesome- (https://fontawesome.com/)
- Hover.css- (http://ianlunn.github.io/Hover/)
- Google Fonts- (https://fonts.google.com)


## Testing

- Manual testing was carried out as follows: 
  

### Home page:

* Mobile view:  
  On smaller screens, the navbar collapses to a dropdown menu.   
  The 'Let's go! button navigates to the 'Now' page with a list of current medications.   
  The hover-to-sweep action does not work on smaller screens. However clicking on each of the icons will take the user to the appropriate page.   

* Larger screens:  
  The navbar is clear and functioning.   
  The hover-to-sweep action works on the 'create a medication'/'weekly calendar'/'view current medications' links. These links are functioning and open the appropriate pages.   
  The 'Let's go! button navigates to the 'Now' page with a list of current medications.   

### Now page:

* Mobile view:  
  By clicking on the 'Now' link in the navbar the "Now page" with a list of currently due medications. 

* Larger screens:  
  By clicking on the 'Now' link in the navbar the "Now page" with a list of currently due medications. 

### Your Weekly schedule:

* Mobile view/larger screens:   
  By clicking on the "your weekly schedule" link in the navbar this page opens.   
  An accordian of the days of the days of the week opens to display medication list for each day of the week.   
  By clicking on the floating addition button at the bottom right corner of the page, the 'add medication' form will render.  
  By clicking on the floating edit button on the bottom roght corner of the page, the 'edit medications' form will render.   

 

### Add medication:

* Mobile View/larger screens:  
  By clicking on the "Add medication" link in the navbar this form opens.   
  By clicking on the calendar icon, a popup calendar appears to select the dates prescribed and discontinued.   
  By clicking om each of the 'time of day' and 'weekday' boxes, a tick will appear.   
  I can enter the name, generic name, doseage and physician name.   
  By clicking on the 'add medication' button, I am brought to the 'edit medication list' page and the new medication has been added to the list. 

### Edit Medication: 

* Mobile View/larger screens:  
  By clicking on the "Edit medications" link in the navbar,  a list of all medications appears in accordian form.   
  By clicking on each medication name, the accordian opens to display the details of that medication.   
  By clicking on the delete button i can delete the medication from the list.  
  By clicking on the edit icon, the edit form renders.  
  By clicking on the calendar icon, a popup calendar appears to change the dates prescribed and discontinued.   
  By clicking on each of the 'time of day' and 'weekday' boxes, a tick will appear.   
  I can edit the name, generic name, doseage and physician name.   
  By clicking on the 'save' button, I am brought to the 'edit medication list' page and the medication has been edited and saved.   



## Contributing

Css validated by [jigsaw](https://jigsaw.w3.org/css-validator/)

I followed a [materialize tutorial](https://www.um.es/docencia/barzana/materializecss/parallax.html) in order to implement the parallax scrolling on the home page. 


## Deployment

Find the Med App deployed on heroku [here](https://flask-med-app.herokuapp.com/).

1. I deployed The Med App using the Heroku cloud app platform as follows: 

2. I logged into my Heroku account and clicked on my dashboard link. From here I clicked on the 'New' link in the top right corner and chose 'create new app'.

3. I typed in my app name and chose Europe region in the drop down menu and clicked the 'create app' button. 

4. I scrolled down to deployment method and clicked the 'github' link. I connected to my github account and chose the Med App repository name. 

5. I clicked on the settings link and entered configuration variables. 

5. I scrolled down to manual deploy and chose 'master' branch to deploy and clicked the 'deploy branch' button. Finally I enabled automatic deploys so that with each Github push, the updated App would be deployed. 

* I used os.getenv(PORT, 8080) as the port and os.getenv(IP, 0.0.0.0) as the host in my scripts. 



## Credits

I would like to thank my tutor Mr Michael Park for help with my code lines 17 to 61 of week.html which consists of multiple for loops within a for loop. 

### Media

#### Images
- The photos used in this site were obtained from [Unsplash](https://unsplash.com/)

### Content

- No external information sources were used. 

