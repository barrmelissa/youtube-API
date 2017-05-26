## YouTube iFrame API

<li><a href="#aboutThisGuide">About the Guide</a></li>

## AboutThisGuide


<!--
Design by TEMPLATED
http://templated.co
Released for free under the Creative Commons Attribution License

Name       : PlainDisplay 
Description: A two-column, fixed-width design with dark color scheme.
Version    : 1.0
Released   : 20140309


<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Info</title>
<meta name="keywords" content="" />
<meta name="description" content="" />
<link href="http://fonts.googleapis.com/css?family=Varela" rel="stylesheet" />
<link href="default.css" rel="stylesheet" type="text/css" media="all" />
<link href="fonts.css" rel="stylesheet" type="text/css" media="all" />

<!--[if IE 6]><link href="default_ie6.css" rel="stylesheet" type="text/css" /><![endif]-->

</head>
<body>
<div id="wrapper">
	<div id="header-wrapper">
	<div id="header" class="container">
		<div id="logo">
			<h1><a href="#">Mountain Project API</a></h1>
		</div>
		<div id="menu">
			<ul>
				<li  id ="home"><a href="#" accesskey="1" title="">Home</a></li>
				<li id="start" ><a href="#" accesskey="2" title="">Getting Started</a></li>
				<li id="info" class="current_page_item"><a href="#" accesskey="3" title="">Info</a></li>
				<li id="using" ><a href="#" accesskey="4" title="">API Code</a></li>
				<li id="end"><a href="#" accesskey="5" title="">Tying It All Together</a></li>
			</ul>
		</div>
	</div>
	</div>
	<div id="banner">
		<div class="container">
			<div class="title">
				<h2>Mountain Project API JavaScript Tutorial</h2>
				<span class="byline">B</span> </div>
		</div>
	</div>
	<div id="extra" class="container">
		<div class="title">
			<h2>Basics of the Mountain Project API</h2>
			<span class="byline">In this section we will go over basic information of the Mountain Project API. Specifically we will briefly discuss the methods that can be used and how they return data.
			</span> 
		</div>
		<div id="three-column" class = "title">
			<h3>Methods</h3>
			<span class="words">There are four methods that can be used with the Mountain Project API, each one serves a specific purpose. Below are the four methods that can be used with the API. Below each method are the keys that are returned within each JSON response from the method. We will use these keys when we need to access data. This page will serve as a good reference for our future endeavors.
				<ol type="1">
					</br>
					<li>
						getUsers: Gets infomation about the requested user.
						<br>
						<span style="padding-left: 50px">Returned Properties in JSON:</span> 
						<ul style="padding-left: 100px">
							<li>id: The users id number.</li>
							<li>name: The users name.</li>
							<li>memberSince: The date the user became a Mountain Project member.</li>
							<li>lastVisit: The last time the user visited Mountain Project.</li>
							<li>favoriteClimbs: Climnbs the user has favorited.</li>
							<li>otherInterests: The users other interests.</li>
							<li>postalCode: The postal code where the user lives.</li>
							<li>location: Where the user lives</li>
							<li>url: The url for the users profile</li>
							<li>personalText: The additional information the user has provided about themselves</li>
							<li>styles: The preferred climbing styles of the user, this is stored as an object that contains other objects. Each object within styles has two properties, one that holds the value of what they lead climb and another for what they can follow in that style. The six styles are:
								<ul style="padding-left: 150px">
								<li>Aid</li>
								<li>Boulders</li>
								<li>Ice</li>
								<li>Mixed</li>
								<li>Sport</li>
								<li>Trad</li>
								</ul>
							</li>
						</ul>
					</li>
					</br>
					<li>
						getTicks: Gets 200 most recent ticks of the user specified.
						<br>
						<span style="padding-left: 50px">Returned Properties in JSON:</span> 
						<ul style="padding-left: 100px">
							<li>average: The average climbing grade of the users ticks.</li>
							<li>hardest: The hardest grade in the users ticks.</li>
							<li>ticks: This property holds contains an array of the users ticks. Each tick can be accessed by accessing its element number in the array. For example tick 1 is at ticks[0]. Within each object in the array there are four properties:
							<ul style="padding-left: 150px">
							<li>date: The date the route was ticked.</li>
							<li>notes: The user's notes on the route.</li>
							<li>pitches: How many climbing pitches the ticked route has.</li>
							<li>routeId: The id of the route on Mountain Project.</li>
							</ul>
							</li>
						</ul>
					</li>
					</br>
					<li>
						getToDos: Gets the specified user's To Dos.
						<br>
						<span style="padding-left: 50px">Returned Properties in JSON:</span> 
						<ul style="padding-left: 100px">
						<li>toDos: This key is an array of route id for the routes that are on the users To Do list. Each element in the array corresponds to one route id.</li>
						</ul>                 
					</li>
					</br>
					<li>
						getRoutes: Gets details for up to 200 routes
						<br>
						<span style="padding-left: 50px">Returned Properties in JSON:</span> 
						<ul style="padding-left: 100px">
						<li>routes: This is an array of objects where each element is an object containing infromation about the route that was queried. The amount of elements in the array is dependent on the amount of route ids that were queried. The keys within each object are:
						<ul style="padding-left: 150px">
						<li>id: The route id that was used in the request.</li>
						<li>imgMed: A medium sized image of the route.</li>
						<li>imgSmall: A small image of the route.</li>
						<li>location: An array that contains information about the route's location. The array can have a variable length but the first lement is the route's state and the second element is the route's city. The other elements are additional information.</li>
						<li>name: The routes name.</li>
						<li>pitches: The number of climbing pitches on the route.</li>
						<li>rating: The climbing grade for the route.</li>
						<li>starVotes: The amount of ratings by users for the route.</li>
						<li>stars: The rating for the route by other climbers.</li>
						<li>type: The type of climbing the route involves.</li>
						<li>url: The url for the routes page on Mountain Project.</li>
						</ul>
						</li>
						</ul>
					</li>
					</br>
				</ol>
				Each of these methods can be used to access various forms of data provided by Moutain Project. Additionally each of these methods takes specific arguments. However, Mountain Project provides information about each method's arguments and thus we will not repeat it here to avoid redundancy. If you have questions about an argument please refer to the Mountain Project API page <a href="https://mountainproject.com/data">here.</a>
			</span>
			</br></br>
			<h3>What Returns To You When You Call A Method</h3>
			<span class="words">
				Just as a quick aside we will discuss what a method returns to you when you call it. Mountain Project API send is response in JSON. For a quick looks lets what happens when we call getRoutes for the famouse Snake Dike route on Half Dome, Snake Dike's route id is 105836362,we'll call it by simply passing the route id and our api key in to the url like this:
				</br>
			<span class="words" style="color: red">
				https://www.mountainproject.com/data?action=getRoutes&routeIds=105836362&key=112477755-36ba8a3e0e6c4b2297518a31b679d122
			</span>
			</br>
			<span class="words">
				The repsonse looks like this:
				<img height="500px" width="900px" src="responsedemo.png">
				</br>
				Our results are given to us in JSON and you can see we are provided with the location of the route, its rating, and other information.
			</span>
			</br></br>
			<span id="ender3">
				Now thats all fine and dandy but we can get the information from the webpage for halfdome and it would look prettier. Additionally we're here to learn about how to use the Mountain Project API to build cool stuff with Javascript so let's get into that!
			</span>
		<ul class="actions">
			<li><a href="#" class="button" id="nexter">Next</a></li>
		</ul>

	</div>
<div id="bottom">
	<div id="copyright" class="container">
	<p>&copy; Connor Wallace All rights reserved. | Design by <a href="http://templated.co" rel="nofollow">TEMPLATED</a>. | 2017</p>
</div>
<script src="howto.js"></script>
<script type="text/javascript">
	document.getElementById("nexter").addEventListener("click",changeCode);
	function changeCode(){
	window.location="code.html";
}
</script>
</body>
</html>

You can use the [editor on GitHub](https://github.com/barrmelissa/youtubeAPI/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/barrmelissa/youtubeAPI/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
