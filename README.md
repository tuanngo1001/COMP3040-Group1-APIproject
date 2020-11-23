# COMP3040-Group1-APIproject

Theme:

- profs in the university
    - prof → courses they teach
        - return professor rating on rate my prof

# Parameters

- **firstName** (string): professors first name. Optional 
- **lastName** (string): professors last name. Optional 
- **order** (int): 0 for asc  1 for desc. Optional

# 3 end points

`www.our_uofm_resource/get_profs` - choose a firstName / lastName

`www.our_uofm_resource/get_rated` - top 5 / bottom 5 ascending/descending

`www.our_uofm_resource/get_course` - get_course - top / bottom rated courses

`www.our_uofm_resource/get_all_profs` - chose an order

### sample requests

```markdown

http://www.our_uofm_resource/get_profs/json?firstName=Roger&lastName=Snack
http://www.our_uofm_resource/get_rated/json?order=0
http://www.our_uofm_resource/get_course/json?order=0

```

### response

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


- **get_course:**
```JSON
  {
    "results":
      [
        { "courseId" : "COMP1010", "avg_rating" : "A" },
        { "courseId" : "COMP2150", "avg_rating" : "A" },
        { "courseId" : "COMP3040", "avg_rating" : "A" },
        { "courseId" : "COMP3380", "avg_rating" : "B" },
        { "courseId" : "COMP4710", "avg_rating" : "B" },
      ],
    "status" : "OK"
  }
```
- **get_rating:**
```JSON
  {
    "results":
      [
        { "Professor" : "James Xidos", "avg_rating" : "A" },
        { "Professor" : "Mike Zwapp",  "avg_rating" : "A" },
        { "Professor" : "Rob Kovitz",  "avg_rating" : "A" },
        { "Professor" : "Karen Sera",  "avg_rating" : "A" },
        { "Professor" : "Mike Shaw",   "avg_rating" : "A" },
      ],
    "status" : "OK"
  }
```

