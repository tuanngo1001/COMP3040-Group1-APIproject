# COMP3040-Group1-APIproject

Theme:

- profs in the university
    - prof → courses they teach
        - return professor rating on rate my prof

# Parameters

- **firstName** (string): professors first name
- **lastName** (string): professors last name
- **order** (int): 0 for asc  1 for desc

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
