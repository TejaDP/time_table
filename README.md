# Ex03 Time Table
# Date:28.09.2025
# AIM
To write a html webpage page to display your slot timetable.

# ALGORITHM
## STEP 1
Create a Django-admin Interface.

## STEP 2
Create a static folder and inert HTML code.

## STEP 3
Create a simple table using `<table>` tag in html.

## STEP 4
Add header row using `<th>` tag.

## STEP 5
Add your timetable using `<td>` tag.

## STEP 6
Execute the program using runserver command.

# PROGRAM
```
urls.py
from django.contrib import admin
from django.urls import path
from app import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.time_table,name="time"),
]

views.py
from django.shortcuts import render
def time_table(request):
    return render(request,"time.html")

templates
time.html
{% load static %}
<html>
    <head>
        <title>
            TIME TABLE
        </title>
         <style>
       h1 { text-align: center; font-size:xx-large; font-style: initial;}   
       th,td { border:3px solid black; padding: 6px;}  
      .table1{ width: 100%; height: 33%; border: 3px solid black; border-collapse: collapse;padding: 6px; text-align: center; }
       .coursetable{ width: 60%; height:27%; border: 3px solid black; border-collapse: collapse;padding: 6px; border-collapse: collapse;padding: 6px; text-align: center;
                 margin: auto; }
      </style>
    </head>
    <body> 
        <img src="{% static 'sec_logo.png' %}", height="23%", width="100%">
         <h1 > SLOT TIME TABLE  - TEJA DP 25018004 </h1>
        <table class="table1">
        <tr style="background-color: darkseagreen;" >
                <td style="font-size: larger;" , >DAY </td>
                <td style="font-size: larger;">  8am - 10 am </td>
                <td style="font-size: larger;" >  10am - 12pm </td>
                <td style="font-size: larger;">  12pm - 1 pm </td>
                <td style="font-size: larger;">   1pm - 3 pm </td>
                <td style="font-size: larger;">   3pm - 5 pm </td>
            </tr>
               <tr style ="background-color: darksalmon;">
                <td>  MONDAY</td>
                <td> FREE  </td>
                <td>  WEB DEVELOPMENT </td>
                <td rowspan="6"> L <br><br> U<br> <br>N <br><br> C <br><br> H</td>
                <td>   PUBLIC SPEAKING</td>
                <td>   FREE </td>
            </tr>
             <tr style ="background-color: darksalmon;">
                <td>  TUESDAY </td>
                <td>  WEB DEVELOPMENT</td>
                <td rowspan="5" >  F<br><br>R<br><br>E<br><br>E </td>
               <td>  WEB DEVELOPMENT </td>
                <td>  PUBLIC SPEAKING  </td>
            </tr>
             <tr style ="background-color: darksalmon;">
                <td>  WEDNESDAY </td>
                <td rowspan="2">   F<br>R<br>E<br>E  </td>
                <td>   MENTOR MEETING  </td>
                <td rowspan="3">  F<br><br>R<br><br>E<br><br>E   </td>
            </tr>
             <tr style ="background-color: darksalmon;" >
                <td>  THURSDAY </td>
                <td> PUBLIC SPEAKING</td>
            </tr>
             <tr style ="background-color: darksalmon;" >
                <td> FRIDAY </td>
                <td> PUBLIC SPEAKING </td>
                 <td>  WEB DEVELOPMENT </td>
            </tr>    
                <tr style ="background-color: darksalmon;">
                <td> SATURDAY</td>
                <td>  WEB DEVELOPMENT </td>
                <td>  PUBLIC SPEAKING </td>
                <td>   PUBLIC SPEAKING  </td>
            </tr>
        </table>
        <br>
        <br>
          <table class="coursetable">
                <tr style="background-color:gray" >
                <td> S.NO </td>
                <td>  COURSE CODE</td>
                <td>  COURSE NAME </td>
                </tr>
            <tr style="background-color:palevioletred">
                <td>  1  </td>
                <td>   19AI414 </td>
                <td> Fundamental Of Web Application Development  </td>
              </tr>  
                 <tr style="background-color:palevioletred">
                <td>  2 </td>
                <td>   19EN105 </td>
                <td >  Public Speaking </td>
                 </tr>
        </table>
    </body>
     </html>
```
# OUTPUT
![alt text](<Screenshot (41).png>)

# RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
