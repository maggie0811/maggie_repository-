| [home page](https://maggie0811.github.io/maggie_repository-/) | [visualizing government debt](visualizing_debt) | [critique by design](critique_by_design) | [final project I](final_project_1) | [final project II]() | [final project III]() |

# Critique by Design: Pittsburgh Regional Transit Trends

The goal of this assignment was to find a published data visualization that could be adjusted to convey the meaning in a more powerful way.

### Original Visualizations

For this project, I selected several simple data visualizations from [Pittsburgh Regional Transit's (PRT) Annual Service Report 2022](https://www.rideprt.org/inside-Pittsburgh-Regional-Transit/Transparency/surveys-and-reports/). The purpose of this report was to highlight service trends of this local transit agency in the year 2022. Specifically, I focused on trends related to ridership and crowding on buses, which is an important trend for the agency to focus on as they continue to emerge from the COVID-19 pandemic and it's impact on ridership.

The data was visualized in three simple charts, which attempted to convey meaning about how each route is recovering with respect to ridership levels and bus crowding levels. While the agency has a desire to return to high ridership levels, it also wants to ensure that people do not experience highly crowded buses, which it defines as not having seats available on any given trip.

The first chart visualizing ridership trends can be seen below. This chart is essentially a stylized table, which attempts to demonstrate low levels of passengers per revenue vehicle hour (PPH), which is essentially average passengers per hour. However, what exactly this metric is is difficult to discern by glancing quickly at the chart, and how the routes selected compare to both themselves and other routes in the system is difficult to discern from the visualization. 

<img src ="https://raw.githubusercontent.com/maggie0811/maggie_repository-/main/PRT%20og%20data%201.JPG" width = "700"/>

Additionally, the creator of the report wanted to convey information about the routes that had high levels of crowding. They visualized this using a simple bar chart. As with the first visualization, however, this chart makes it very difficult to compare the crowded routes with routes that had very low levels of ridership, and is overly simplistic. Additionally, the chart does not provide information about passengers per hour for these highly crowded routes, which makes it difficult to see if the routes are becoming too crowded for pandemic safety standards.

<img src = "https://raw.githubusercontent.com/maggie0811/maggie_repository-/main/prt%20og%20data%202.JPG" width = "700"/>

The full set of data was also provided in the report, with each route highlighted if it was achieving low performance standards in any measurement category.

<img src = "https://raw.githubusercontent.com/maggie0811/maggie_repository-/main/PRT%20og%20data%203.JPG" width = "700"/>

Overall, the combination of charts and metrics, while potentially useful for understanding one single metric, makes it very difficult for the reader to get a good understanding of the larger ridership trends present in the agency. Additionally, the information conveyed in the chart could be very easily conveyed ina  written sentence or two, which made me wonder why the data was being visualized at all. The purpose of this critique by design is to create a single visualization that better captures the larger trends of the data, with the assumption that if a reader wants information on a particular route, they will look into the larger dataset.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------
### Stage 1: Sketch

I began by first sketching my idea for my visualization on a piece of paper. This helped me convey the general concept of my visualization, without spending too much time on the technical back-end before recieving my first round of critiques.

<img src = "https://raw.githubusercontent.com/maggie0811/maggie_repository-/main/critique%20sketch%201.jpg" width = "600"/>

I presented this sketch to two students in my program, both in their mid 20's. Regarding the initial sketch, I had a variety of feedback. The feedback that stood out most was that I likely was trying to show too many variables with my initial sketch. The students I interviewed did not see the purpose of having a variable designating the route type (ie. if it was a commuter bus or not). They spoke about the importance of showing the most important point of the data, rather than as many variables as possible. They did like the idea of combining the variables, but did stress the idea of only including the necessary ones. For this reason, I decided to show only three variables in my next iteration of the visualization, which was done in Tableau and can be seen below. These three variables ended up being how crowded the trips were, how many passengers were carried per hour, and how many weekday riders were on each bus, which I hoped would give the reader a sense of if the route was a commuter route or not.

### Stage 2: Tableau Iteration

<div class='tableauPlaceholder' id='viz1675817021177' style='position: relative'><noscript><a href='#'><img alt='Ridership Levels Decline in FY22, only 3 routes in Compliance with PPH standards ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;PR&#47;PRTRidership&#47;Sheet1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='PRTRidership&#47;Sheet1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;PR&#47;PRTRidership&#47;Sheet1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div> 
<script type='text/javascript'>                    
  var divElement = document.getElementById('viz1675817021177');                    
  var vizElement = divElement.getElementsByTagName('object')[0];                   
  vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    
  var scriptElement = document.createElement('script');                    
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    
  vizElement.parentNode.insertBefore(scriptElement, vizElement);                
</script>


After creating this visualization, I presented it to my two roommates, both also students in their mid 20's. I also let them see my initial sketch, to see if there were any elements they felt I should incorporate since I had not included everything from my initial sketch in the digital version. My first roomate primarily discussed the importance of adding color to the chart. She felt it was hard to tell what the colors meant, and noted that they were not very bold. Additionally, she noticed the word "decline" in the title, but did not see any declining trend in the data, so was curious what type of trend she should be looking for. She also talked about the sizing of the circles, and wanted to know what that meant. Essentially, having just looked at the chart with no context, she felt like she still had a lot of questions about the data and what story I was trying to tell. Additionally, after seeing my initial sketch, she liked the idea of a dividing line to separate the "good" quadrants from the "bad," since this was not apparent ust by looking at the x & y axes.

My other roommate had similar feedback. By this time in the process, I had converted the chart to a Flourish visualization with separate quadrants for "good" and "bad" ridership metrics, since I could not figure out how to add quadrants easily in Tableau. However, much of the remaining visualization looked the same. My other roommate also wanted to know about the color scheme, since the meaning behind this was not easily apparent to her. She also wanted to know why the dots were different sizes. Finally, the fact that the points themselves represented bus routes was initially unclear to her. She recommended to clarify this in the title of the visualization, as well as by using labels for the points, so the reader could understand that they represented different bus routes.

Taking this feedback, I created the final visualization as can be seen below.

### Stage 3: Final Visualization

<div class="flourish-embed flourish-scatter" data-src="visualisation/12669184"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

This final visualization incorporates much of the feedback I recieved with my first two iterations of the design. I redesigned the chart using Flourish, which allowed me to incorporate the quadrants with a small label that clearly identifies which section of the chart is "ideal" for PRT's service goals. Additionally, I used distinct colors, gold for the routes that satisfied the desired critera, and grey for the routes which did not. I also changed the title and added a subtitle to make it cery clear what message the graph is conveying. I also added hovering data keys, so the reader could assess each route and the metrics associated with it individually. This also helps them understand that the size of the dot relates to the weekday ridership levels. I added a key which only lists the three routes achieving ideal standards, which makes it clear that these are the routes of focus. Additionally, the high ridership routes can still be seen in the quadrant on the high end of the ridership scale, and the low crowding routes can also be distinguished. Finally, I added small route number labels to the dots, to make it clear that these dots are unique bus routes. This idea is also reflected in the updated subtitle.

Overall, the iterative process of redesigning these graphics was useful, and resulted in a chart that paints a clearer picture of overall trends, rather than just summarizing small components of the data.

-------------------------------------
 






