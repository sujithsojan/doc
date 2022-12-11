# Form Config


Form configuration allows us to modify the labels according to our purpose by using dynamic labels in the application. It does not use static labels.

On the User home page, Browse by category, Browse courses by user type and Browse by subject are getting their labels through form configuration. Here we are passing the request, and getting a response accordingly.
1. &nbsp;If Suppose the user is logged in as an admin, the Learn, Manage and Act section in the User home page will appear as shown in the below screenshot.
&nbsp;
![userhome (4) (2).jpg](https://www.dropbox.com/s/sba4nk23ufh2jfw/userhome%20%284%29%20%282%29.jpg?dl=0&raw=1)
&nbsp;
  The request we are passing will be,

```sh
"request": {
   "type": "config",
   "subType": "adminHome",
   "action": "get",
   "component": "app"
 }

```

 and accordingly the response,

```sh
{
       "code": "program",
       "title": "{\"en\":\"Programs\"}",
       "search": {}
   },
   {
       "code": "project",
       "title": "{\"en\":\"Projects\"}",
       "search": {}
   },
   {
       "code": "observation",
       "title": "{\"en\":\"Observations\"}",
       "search": {}
   }
```
  According to the response, we are getting from form config, labels would be different. This is the prime advantage of using form configuration. 
  
  2. &nbsp; When it comes to the search filter in the search tab, it calls a request that will return 9 types of filters.
&nbsp;
![filterpage (5).jpg](https://www.dropbox.com/s/22xc239l7dwixcl/filterpage%20%285%29.jpg?dl=0&raw=1)

Request we are passing is,

```sh
{
   "request": {
     "from": "server",
     "type": "user",
     "subType": "selfDeclaration_v3",
     "action": "submit",
     "component": "app"
   }
  }
```
And the response contains:
```sh
{
   "code": "se_boards",
   "translations": "{\"en\":\"Board/Syllabus\",\"as\":\"ব'ৰ্ড\",\"bn\":\"পর্ষদ\",\"gu\":\"બોર્ડ\",\"hi\":\"बोर्ड\",\"kn\":\"ಮಂಡಳಿ\",\"mr\":\"बोर्ड\",\"or\":\"ବୋର୍ଡ\",\"pa\":\"ਬੋਰਡ\",\"ta\":\"வாரியம்\",\"te\":\"బోర్డు\",\"ur\":\"بورڈ\"}",
   "values": [],
   "name": "Board/Syllabus",
   "index": 1
},
{
   "code": "se_gradeLevels",
   "translations": "{\"en\":\"Class\",\"as\":\"শ্ৰেণী\",\"bn\":\"শ্রেনী\",\"gu\":\"વર્ગ\",\"hi\":\"कक्षा\",\"kn\":\"ತರಗತಿ\",\"mr\":\"इयत्ता\",\"or\":\"ଶ୍ରେଣୀ\",\"pa\":\"ਜਮਾਤ\",\"ta\":\"வகுப்பு\",\"te\":\"క్లాసు\",\"ur\":\"کلاس\"}",
   "values": [],
   "name": "Class",
   "index": 2
},

```



