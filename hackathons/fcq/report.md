{% data src="fcq.clean.json" %}
{% enddata %}

# Report

As a class, we brainstormed and came up with a long list of further questions we
can ask based on the FCQ data. Out of these questions, our team chose to tackle on
the following questions. Each member on our team is reponsible for one question.

# Which instructor's course has the highest enrollment? by Zhili Yang

{% lodash %}
var list = _.map(data, function(course){
  var instructors=course['Instructors']
  var enroll=course['N']['ENROLL']
  var courseName=course['CourseTitle']
  return _.map(instructors, function(instructor){
    return {"instructor": instructor['name'], "courseTitle": courseName, "enrollment": enroll}
  })
})

var maxGroups=_.max(_.flatten(list), function(course){
	return course['enrollment']
})
return maxGroups
{% endlodash %}
The professor is {{result['instructor']}}, the course title is {{result['courseTitle']}}.

# How many courses in IPHY that has 4 credits hours ? by Zhili Yang

{% lodash %}
var course = _.filter(data,function(n){
 return n['CrsPBADept'] == 'IPHY'
})
var hour = _.filter(course,function(d){
 return d['Hours'] == 4
})

return _.size(hour)
{% endlodash %}

They are {{ result }} courses that have 4 credits hour.


# (Question 3) by (Name)

{% lodash %}
return "[answer]"
{% endlodash %}

# (Question 4) by (Name)

{% lodash %}
return "[answer]"
{% endlodash %}

# (Question 5) by (Name)

{% lodash %}
return "[answer]"
{% endlodash %}
