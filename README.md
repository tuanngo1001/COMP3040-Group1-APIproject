# University of Manitoba professor's ratings API

Our API provides the **ratings and courses** of the professors that teach at the University of Manitoba.  
You can request the professor's overall rating and their top/bottom rated courses using  **firstName** and **lastName**.  
It is also possible to request for top/bottom rated professors, top/bottom rated courses, and a list of all professors by **order**.

## API Documentation
We provide a REST API that is very easy to use. All the requests are done using GET, to the following URL: **https://api.uofm-ratings.ca/**

### Parameters

- **firstName** (string): professor's first name. Optional
- **lastName** (string): professor's last name. Optional
- **order** (int): 0 for ascending order and 1 for descending order. Optional

### Sample requests

```markdown

https://api.uofm-ratings.ca/get-prof/json?firstName=Roger&lastName=Snack

https://api.uofm-ratings.ca/get-rated/json?order=0

https://api.uofm-ratings.ca/get-course/json?order=1

https://api.uofm-ratings.ca/get-all-profs/json?order=0

```

### Response

1. Response example for `https://api.uofm-ratings.ca/get-prof/json?firstName=Roger&lastName=Snack`
```markdown
{
	"results":
		{
			"professor": Roger Snack, 
			"Overall Rating": B
			"top_rated_courses": ["COMP3430","COMP3330"],
			"bottom_rated_courses": ["COMP3130","COMP3030"]
		},
	"status": "OK"
}

```
2. Response example for `https://api.uofm-ratings.ca/get-course/json?order=0`
```markdown
{
	"results":
		{
			//TODO
		},
	"status": "OK"
}

```
3. Response example for `https://api.uofm-ratings.ca/get-rated/json?order=1`
```markdown
  {
    "results":
      [
        {
		"Professor" : "James Xidos",
	 	 "avg_rating" : "A" 
	},
        {
		"Professor" : "Mike Zwapp",
	 	 "avg_rating" : "A" 
	},
        {
		"Professor" : "Rob Kovitz", 
	  	"avg_rating" : "A" 
	},
        {
		"Professor" : "Karen Sera",
	  	"avg_rating" : "A" 
	},
        {
		"Professor" : "Mike Shaw",  
	  	"avg_rating" : "B+" 
	},
      ],
    "status" : "OK"
  }
```

4. Response example for `https://api.uofm-ratings.ca/get-all-profs/json?order=0`
```markdown
{
	"results":
		[
			{
				"rating" : "A+", 
				"firstName" : "Michael", 
				"lastName" : "Scott",
				"courses" : ["COMP1999","COMP2999"]	
			},
			{
				"rating" : "A", 
				"firstName" : "Dwight", 
				"lastName" : "Schrute"
				"courses" : ["COMP2999","COMP3999"]	
			},
			{
				"rating" : "B+", 
				"firstName" : "Jim", 
				"lastName" : "Halpert",
				"courses" : ["COMP1000","COMP1999"]	
			},
			{
				"rating" : "B", 
				"firstName" : "Pam", 
				"lastName" : "Beesly"
				"courses" : ["COMP4000"]
			},
			{
				"rating" : "C", 
				"firstName" : "Kevin", 
				"lastName" : "Malone",
				"courses" : ["COMP1000","COMP1999"]	
			},
			{
				"rating" : "F", 
				"firstName" : "Andy", 
				"lastName" : "Bernard",
				"courses" : ["COMP1000","COMP2000"]	
			}
		]
	"status": "OK"
}

```
