
<!DOCTYPE html>
<html lang="en-us">
  <head>
    <meta charset="UTF-8">
    <title>YouTube iFrame API</title>
    <meta name="description" content="API for YouTube videos"/>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="theme-color" content="#157878">
    <link href='https://fonts.googleapis.com/css?family=Open+Sans:400,700' rel='stylesheet' type='text/css'>
    <link rel="stylesheet" href="/youtubeAPI/assets/css/style.css?v=7e70b5d52d227263449982905952e7be597a1ba1">
  </head>
  <body>
    <section class="page-header">
      <h1 class="project-name">YouTube API Tutorial</h1>
      <h2 class="project-tagline">API for YouTube videos</h2>
      
        <a href="https://github.com/barrmelissa/youtubeAPI" class="btn">View on GitHub</a>
      
      
    </section>

    <section class="main-content">
      <h2 id="youtube-iframe-api">YouTube iFrame API</h2>

<li><a href="#aboutThisGuide">About the Guide</a></li>

<h2 id="aboutthisguide">AboutThisGuide</h2>

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

<p>&lt;/head&gt;</p>
<body>
<div id="wrapper">
	<div id="header-wrapper">
	<div id="header" class="container">
		<div id="logo">
			<h1><a href="#">Mountain Project API</a></h1>
		</div>
		<div id="menu">
			<ul>
				<li id="home"><a href="#" accesskey="1" title="">Home</a></li>
				<li id="start"><a href="#" accesskey="2" title="">Getting Started</a></li>
				<li id="info" class="current_page_item"><a href="#" accesskey="3" title="">Info</a></li>
				<li id="using"><a href="#" accesskey="4" title="">API Code</a></li>
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
		<div id="three-column" class="title">
			<h3>Methods</h3>
			<span class="words">There are four methods that can be used with the Mountain Project API, each one serves a specific purpose. Below are the four methods that can be used with the API. Below each method are the keys that are returned within each JSON response from the method. We will use these keys when we need to access data. This page will serve as a good reference for our future endeavors.
				<ol type="1">
					&lt;/br&gt;
					<li>
						getUsers: Gets infomation about the requested user.
						<br />
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
					&lt;/br&gt;
					<li>
						getTicks: Gets 200 most recent ticks of the user specified.
						<br />
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
					&lt;/br&gt;
					<li>
						getToDos: Gets the specified user's To Dos.
						<br />
						<span style="padding-left: 50px">Returned Properties in JSON:</span> 
						<ul style="padding-left: 100px">
						<li>toDos: This key is an array of route id for the routes that are on the users To Do list. Each element in the array corresponds to one route id.</li>
						</ul>                 
					</li>
					&lt;/br&gt;
					<li>
						getRoutes: Gets details for up to 200 routes
						<br />
						<span style="padding-left: 50px">Returned Properties in JSON:</span> 
						<ul style="padding-left: 100px">
						<li>routes: This is an array of objects where each element is an object containing infromation about the route that was queried. The amount of elements in the array is dependent on the amount of route ids that were queried. The keys within each object are:
						<ul style="padding-left: 150px">
						<li>id: The route id that was used in the request.</li>
						<li>imgMed: A medium sized image of the route.</li>
						<li>imgSmall: A small image of the route.</li>
						<li>location: An array that contains information about the route's location. The array can have a variable length but the first element is the route's state and the second element is the route's city. The other elements are additional information.</li>
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
					&lt;/br&gt;
				</ol>
				Each of these methods can be used to access various forms of data provided by Moutain Project. Additionally each of these methods takes specific arguments. However, Mountain Project provides information about each method's arguments and thus we will not repeat it here to avoid redundancy. If you have questions about an argument please refer to the Mountain Project API page <a href="https://mountainproject.com/data">here.</a>
			</span>
			&lt;/br&gt;&lt;/br&gt;
			<h3>What Returns To You When You Call A Method</h3>
			<span class="words">
				Just as a quick aside we will discuss what a method returns to you when you call it. Mountain Project API send is response in JSON. For a quick looks lets what happens when we call getRoutes for the famouse Snake Dike route on Half Dome, Snake Dike's route id is 105836362,we'll call it by simply passing the route id and our api key in to the url like this:
				&lt;/br&gt;
			<span class="words" style="color: red">
				https://www.mountainproject.com/data?action=getRoutes&amp;routeIds=105836362&amp;key=112477755-36ba8a3e0e6c4b2297518a31b679d122
			</span>
			&lt;/br&gt;
			<span class="words">
				The repsonse looks like this:
				<img height="500px" width="900px" src="responsedemo.png" />
				&lt;/br&gt;
				Our results are given to us in JSON and you can see we are provided with the location of the route, its rating, and other information.
			</span>
			&lt;/br&gt;&lt;/br&gt;
			<span id="ender3">
				Now thats all fine and dandy but we can get the information from the webpage for halfdome and it would look prettier. Additionally we're here to learn about how to use the Mountain Project API to build cool stuff with Javascript so let's get into that!
			</span>
		<ul class="actions">
			<li><a href="#" class="button" id="nexter">Next</a></li>
		</ul>

	&lt;/div&gt;
<div id="bottom">

<script src="howto.js"></script>
<script type="text/javascript">
	document.getElementById("nexter").addEventListener("click",changeCode);
	function changeCode(){
	window.location="code.html";
}
</script>
&lt;/body&gt;
&lt;/html&gt;

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
k 
			<nav class="navigation">
			<p> <b>Navigation</b> </p>
			<ul class="menu">	
				<li><a href="#top">Title</a></li>
				<li><a href="#aboutThisGuide">About the Guide</a></li>
				<li><a href="#embedVideo">Embedding a Video</a></li>
				<li><a href="#queueFunctions">Queuing Functions</a></li>
				<li><a href="#eventsPage">Event Handlers</a></li>
				<li><a href="#playbackControls">Playback Controls</a></li>
				<li><a href="#exampleVideo">Example Video</a></li>
			</ul>
		</nav>
		<div class="outer"><br />
	<div class="inner-title">
	<br />
	<center><h1>The Basics of YouTube API</h1>
	<h4><font>By: Melissa Barr </font></h4></center>
	<br />
	</div>
	</div>
		
	<br />
				<div class="outer">
			<div id="aboutThisGuide"></div>
				<div class="inner-heading">	
					<h3><br />About This Guide<br /><br /></h3>
				</div>
				<div class="inner-body">
					
			<h4>Why YouTube API?</h4>
					<p><center>I chose to research and learn about the YouTube API because it is a useful skill to have when building websites. YouTube videos are a handy tool, whether it be informational or about cats doing funny things. While this is only a basic overview of the YouTube API, more information can be found at <a href="https://developers.google.com/youtube/">https://developers.google.com/youtube/</a>. Credit given to <a href="https://developers.google.com/youtube/iframe_api_reference">https://developers.google.com/youtube/iframe_api_reference</a> for certain code excerpts.</center></p>
					
				<br /><div class="blackBar"></div><br />
				
				<h4>What is this API?</h4>
				<p><center>We will be using the IFrame Player API in order to embed videos to our own applications. The IFrame Player API posts content directly to a <code>&lt;iframe&gt;</code> tag on your page. This is different from JavaScript or Flash as they both involve embedding a Flash object, which mobile devices do not support.
					<br /><br />
					This guide will discuss the IFrame API in greater detail, such as how to embed a video, how to use JavaScript functions to control the videos, and adding event listeners for certain events.</center></p>
					
					<br /><div class="blackBar"></div><br />
					
					<h4>Requirements</h4>
					<p>In order to run the IFrame API, there are a few necessary requirements.
					<br /><br />
					These requirements are as follows:</p>
					<ul>
						<li>Your browser must be able to support the HTML5 <code>postMessage</code> feature. This feature allows for data messages to be sent between two windows/frames across domains.</li>
						<li>YouTube requires that embedded videos have a viewport of at least 200px by 200px. That size does not include the control bar at the bottom, so beware of that when embedding videos. The Google recommended size of this is 480px wide by 270px tall.</li>
						<li>The JavaScript function <code>onYouTubeIframeAPIReady</code> must be implemented on any page that runs the IFrame API. The <code>onYouTubeIframeAPIReady</code> function will be called when the page has finished downloading the JavaScript for this player API. This will allows the content within the API to be loaded.</li>
					</ul>
					
					<br />
				</div>
			</div>
		</div>	
		
		<br /><br />
		
		<div class="outer">
			<div id="embedVideo"></div>
				<div class="inner-heading">	
					<h3><br />Embedding A Video<br /><br /></h3>
				</div>
				<div class="inner-body">
				
				<table class="offset">
					<tr>
						<th>There are two ways you can embed a YouTube video on a web page.</th>
					</tr>
						<td>1. Using the <code>&lt;iframe&gt;</code> element.</td>
					&lt;/tr&gt;
					<tr>
						<td>2. Using JavaScript.</td>
					</tr>
				</table>
				
				<br /><div class="blackBar"></div><br />
				
				<h4>Using the <code>&lt;iframe&gt;</code> element.</h4>
				<p>Sample code for using the <code>&lt;iframe&gt;</code> element is:</p>
				<br />
				
				<code class="chunk">
					&lt;iframe width="420" height="315" <br /> 
					src="http://www.youtube.com/embed/XGSy3_Czz8k?autohide=1"&gt;<br />
					&lt;/iframe&gt;
				</code>
				
				<br /><br />
				
				<table class="offset" border="1">
					<tr>
						<th>Parameter</th>
						<th>Functionality</th>
					</tr>
						<td><code class="chunk">width</code></td>
						<td>refers to the width of the video player</td>
					&lt;/tr&gt;
					<tr>
						<td><code class="chunk">height</code></td>
						<td>refers to the height of the video player</td>
					</tr>
					<tr>
						<td><code class="chunk">src</code></td>
						<td>refers to the URL of the video</td>
					</tr>
				</table>
					
				<p>There are also YouTube parameters that can be passed in. An example is shown within the code, as <code>autohide=1</code>. Listed below are commonly used YouTube parameters and their accepted values.</p>
				
				<ul>
					<li>autohide
						<ul>
							<li>Value 0: video player controls always visible</li>
							<li>Value 1: controls hide automatically when video starts</li>
							<li>Value 2: If the player has 16:9 or 4:3 ratio, same as 1, otherwise same as 0</li>
						</ul>
					</li>
					<li>autoplay
						<ul>
							<li>Value 0: video will not play automatically when video loads</li>
							<li>Value 1: video will play automatically when video loads</li>
						</ul>
					</li>
					<li>controls
						<ul>
							<li>Value 0: video player controls does not display; the video loads immediately</li>
							<li>Value 1: video player controls display; the video loads immediately</li>
							<li>Value 2: video layer controls display, but the video does not load before the user initiates playback</li>
						</ul>
					</li>
					<li>loop
						<ul>
							<li>Value 0: the video will only play once</li>
							<li>Value 1: the video will loop forever</li>
						</ul>
					</li>
					<li>playlist
						<ul>
							<li>A comma separates the list of videos to play.</li>
						</ul>
					</li>
				</ul>
				
				<br /><div class="blackBar"></div><br />
				
				<h4>Using JavaScript</h4>
				
				<p>The following code excerpt shows how to set up the <code>&lt;iframe&gt;</code> through JavaScript.
				<br /><br />
				As a side note, ever since the <code>&lt;iframe&gt;</code> tag has been implemented into HTML5, the JavaScript method of embedding is not very common.
				<br /></p>
					
				<code class="chunk">
					// This code loads the IFrame Player API code asynchronously.&lt;/br&gt;
					var tag = document.createElement('script');&lt;/br&gt;
					tag.src = "https://www.youtube.com/iframe_api";&lt;/br&gt;
					var firstScriptTag = document.getElementsByTagName('script')[0];&lt;/br&gt;
					firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);&lt;/br&gt;
					&lt;/br&gt;
					// This function creates an &lt;iframe&gt; (and YouTube player)&lt;/br&gt;
					// after the API code downloads.&lt;/br&gt;
					var player;&lt;/br&gt;
					function onYouTubeIframeAPIReady() {&lt;/br&gt;
					&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;player = new YT.Player('player', {&lt;/br&gt;
					&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;height: '390',&lt;/br&gt;
					&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;width: '640',&lt;/br&gt;
					&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;videoId: 'ID of desired video',&lt;/br&gt;
					&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;events: {&lt;/br&gt;
					&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;	'onReady': onPlayerReady,&lt;/br&gt;
					&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;	'onStateChange': onPlayerStateChange&lt;/br&gt;
					&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}&lt;/br&gt;
					&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;});&lt;/br&gt;
					}
				</code>
				
				<ul>
					<li>The first segment of code loads the IFrame Player API JavaScript code. The DOM is manipulated to ensure that the code is asynchronous.</li>
					<li>The function <code>onYouTubeIframeAPIReady()</code> will load as soon as the player API code downloads. The function <code>YT.Player</code> accepts two parameters. The first parameter is the global variable <code>player</code> which refers to the video that is being embedded. The second parameter is an object that refers to the specifications of the video. The object has the following properties:
					<br /><br /><ul>
						<li><code>height</code>: refers to the height of the video</li>
						<li><code>width</code>: refers to the width of the video</li>
						<li><code>videoID</code>: refers to the ID of the video</li>
						<li><code>events</code>: refer to the Event Handlers section</li>
					</ul>
				&lt;/ul&gt;
				
				<br />
				&lt;/div&gt;
			
			&lt;/div&gt;
		&lt;/div&gt;	
		
		<br /><br />
		
		<!-- Queuing Functions -->	
		<div class="outer">
			<div id="queueFunctions"></div>
				<div class="inner-heading">	
					<h3><br />Queuing Functions<br /><br /></h3>
				</div>
				<div class="inner-body">
				
				<h4>General information about queuing</h4>
				
				<p>Before a player is able to play the video, it must be queued. The YouTube API allows for the queue of a single video, multiple videos, or search results.</p>
				<p>There are two different calling syntaxes supported by the YouTube API:</p>
				<ul>
					<li>Argument syntax</li>
					<li>Object syntax</li>
				</ul>
				<p>The different functions will be explained below, with code samples using both supported syntaxes.</p>
				
				<br /><div class="blackBar"></div><br />
				
				<h4><code class="chunk">cueVideoById</code> and <code class="chunk">loadVideoById</code></h4>
				
				<p><code>cueVideoById</code> loads the requested video's thumbnail and prepares the player to play the video. Note that the full video is not loaded until either <code>playVideo</code> or <code>seekTo</code> is called.
				<br /><br />
				<code>loadVideoById</code> loads the video, but unlike <code>cueVideoById</code>, it also plays the video.</p>
				
				<p>The following code samples depict an example of the argument and object syntax for the previously mentioned functions.</p>
				<p><b>Argument Syntax:</b>
				<br /><br />
				<code class="chunk">player.cueVideoById(videoId:String,<br />
                &nbsp;&nbsp;&nbsp;startSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;suggestedQuality:String):Void<br /><br /></code>
				<code class="chunk">player.loadVideoById(videoId:String,<br />
                &nbsp;&nbsp;&nbsp;startSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;suggestedQuality:String):Void<br /><br /><br /></code>
				
				<b>Object Syntax:</b>
				<br /><br />
				<code class="chunk">player.cueVideoById({videoId:String,<br />
                &nbsp;&nbsp;&nbsp;startSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;endSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;suggestedQuality:String}):Void<br /><br /></code>
				<code class="chunk">player.loadVideoById({videoId:String,<br />
                &nbsp;&nbsp;&nbsp;startSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;endSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;suggestedQuality:String}):Void<br /><br /></code>
				
				As shown by the examples, the object syntax allows for an extra video specification to be passed in. This is the <code>endSeconds</code> object member, which allows the programmer to put an endpoint to the video, as opposed to just a starting point.
				<br /><br />
				The other specifications are as follow:<br />
				<ul>
					<li><code>videoId</code>: This parameter specifies the ID of the requested video. It is a required parameter for both functions.</li>
					<li><code>startSeconds</code>: This parameter specifies which second the video will start at. For <code>cueVideoById</code>, this parameter tells it where to start the video in case <code>playVideo</code> is called. This parameter is optional for both functions.</li>
					<li><code>suggestedQuality</code>: This parameter specifies the suggested quality for the requested video. This parameter is optional for both functions.</li>
				</ul>
				
				<br /><div class="blackBar"></div><br />
				
				<h4><code class="chunk">cueVideoByUrl</code> and <code class="chunk">loadVideoByUrl</code></h4>
				
				<p>Much like the function mentioned above, <code>cueVideoByUrl</code> loads the requested video's thumbnail and prepares the player to play the video, only this uses the full URL of the video.
				<br /><br />
				<code>loadVideoByUrl</code> loads and plays the video, also using the full URL.</p>
				
				<p><b>Argument Syntax:</b>
				<br /><br />
				<code class="chunk">player.cueVideoByUrl(mediaContentUrl:String,<br />
                &nbsp;&nbsp;&nbsp;startSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;suggestedQuality:String):Void<br /><br /></code>
				<code class="chunk">player.loadVideoByUrl(mediaContentUrl:String,<br />
                &nbsp;&nbsp;&nbsp;startSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;suggestedQuality:String):Void<br /><br /><br /></code>
				
				<b>Object Syntax:</b>
				<br /><br />
				<code class="chunk">player.cueVideoByUrl({mediaContentUrl:String,<br />
                &nbsp;&nbsp;&nbsp;startSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;endSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;suggestedQuality:String}):Void<br /><br /></code>
				<code class="chunk">player.loadVideoByUrl({mediaContentUrl:String,<br />
                &nbsp;&nbsp;&nbsp;startSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;endSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;suggestedQuality:String}):Void<br /><br /></code>
				
				Note that there are few differences between the functions that use the URL or ID of a video. Besides the name, the main difference between the two is the <code>mediaContentUrl</code> parameter. This parameter accepts the full URL of the video, as opposed to just its ID. This parameter is required for both functions. For an explanation of the remaining parameters, please refer above.</p>
				
				
				<br /><div class="blackBar"></div><br />
				
				<h4>Playlists</h4>
				
				<p>Much like single videos, there are two functions for playlists, <code>cuePlaylist</code> and <code>loadPlaylist</code>. The main difference between playlists and single videos is that, instead of a single URL/ID, an array of URL's/ID's must be passed as an argument. The argument syntax varies slightly more than the object syntax, so they will be explained individually.</p>
				
				<p><b>Argument Syntax</b><br /><br />
				<code class="chunk">player.cuePlaylist(playlist:String|Array,<br />
                &nbsp;&nbsp;&nbsp;index:Number,<br />
                &nbsp;&nbsp;&nbsp;startSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;suggestedQuality:String):Void<br /><br /></code>
				
				<ul>
					<li><code>playlist</code>: This parameter is an array of YouTube video ID's. This parameter is required.</li>
					<li><code>index</code>: This parameter tells the player which video to play first. Much like arrays, the first index is 0, which is the default beginning of the playlist. This parameter is optional.</li>
					<li><code>startSeconds</code>: This parameter decides where the first video will begin playing from. This parameter is optional.</li>
					<li><code>suggestedQuality</code>: This parameter specifies the suggested quality the video should be played at. This parameter is optional.</li>
				</ul>
				
				To reduce redundancy, the explanation for the <code>loadPlaylist</code> argument syntax will be omitted. The only difference between the two functions is that <code>cuePlaylist</code> only queues the playlist, while <code>loadPlaylist</code> loads and plays the playlist.</p>
				
				<br />
				
				<p><b>Object Syntax</b><br /><br />
				<code class="chunk">player.cuePlaylist({listType:String,<br />
                &nbsp;&nbsp;&nbsp;list:String, <br />
                &nbsp;&nbsp;&nbsp;index:Number, <br />
                &nbsp;&nbsp;&nbsp;startSeconds:Number,<br />
                &nbsp;&nbsp;&nbsp;suggestedQuality:String}):Void<br /><br /></code>
				
				<ul>
					<li><code>listType</code>: This parameter specifies the type of results feed that are being retrieved. The accepted value are <code>playlist</code>, <code>search</code>, and <code>user_uploads</code>. The default argument of this parameter is <code>playlist</code>.</li>
					<li><code>list</code>:
					<li><code>index</code>: This parameter tells the player which video to play first. Much like arrays, the first index is 0, which is the default beginning of the playlist. This parameter is optional.</li>
					<li><code>startSeconds</code>: This parameter decides where the first video will begin playing from. This parameter is optional.</li>
					<li><code>suggestedQuality</code>: This parameter specifies the suggested quality the video should be played at. This parameter is optional.</li>
				&lt;/ul&gt;
				
				To reduce redundancy, the explanation for the <code>loadPlaylist</code> object syntax will be omitted. The only difference between the two functions is that <code>cuePlaylist</code> only queues the playlist, while <code>loadPlaylist</code> loads and plays the playlist.&lt;/p&gt;
				
				<br />
				&lt;/div&gt;
			
			&lt;/div&gt;
		&lt;/div&gt;	
		
		<br /><br />
		
		<!-- Events -->	
		<div class="outer">
			<div id="eventsPage"></div>
				<div class="inner-heading">	
					<h3><br />Event Handlers<br /><br /></h3>
				</div>
				<div class="inner-body">
				
				<h4>Introduction</h4>
				
				<p>There are certain events that are fired from the API to notify any changes made to the embedded YouTube video. These events can be added to the previously mentioned <code>YT.Player</code> object, or through <code>addEventListener</code>. Events are passed as objects, with these properties:
				<ul>
					<li><code>target</code>: This is the specified player the event is bound to.</li>
					<li><code>data</code>: This is the data passed in, associated with the event.</li>
				</ul>
				<br />
				The specific event handlers produced by the YouTube API are as follows:</p>
				<br />
				
				<table border="1">
					<tr>
						<td><code class="chunk">onReady</code></td>
						<td><code>onReady</code> is pretty much what it sounds like. This event fires whenever the player has finished loading and is ready to be manipulated. This event should be used for times when the player needs to do something as soon as it's ready, such as play when it is loaded or have information displayed about it.</td>
					</tr>
					<tr>
						<td><code class="chunk">onStateChange</code></td>
						<td>This event fires whenever the state of the player changes. Unlike <code>onReady</code>, this event has several data value associated with it. They are:
		
						<ul>
							<li>-1 (unstarted)</li>
							<li>0 (ended)</li>
							<li>1 (playing)</li>
							<li>2 (paused)</li>
							<li>3 (buffering)</li>
							<li>5 (video cued)</li>
						</ul>
						Something to note about this event is that when a played first loads the video, the value is -1, likewise, when a player cues the video, the value is 5.</td>
					</tr>
					<tr>
						<td><code class="chunk">onPlaybackQualityChange</code></td>
						<td>This event fires when the quality of the video within the specified player changes. This can be triggered by two events, user changing the quality or sending <code>suggestedQuality</code> to this function. Note that it will only fire if the quality actually changes when the <code>suggestedQuality</code> function is called. The data associated with this event are:
						<ul>
							<li>small</li>
							<li>medium</li>
							<li>large</li>
							<li>hd720</li>
							<li>hd1080</li>
							<li>highres</li>
						</ul>
						</td>
					</tr>
					<tr>
						<td><code class="chunk">onPlaybackRateChange</code></td>
						<td>This event fires if the rate of the video within the specified player changes. This is associated with the argument <code>suggestedRate</code>, and will change only if running this function with <code>suggestedRate</code> as a parameter returns a different rate than before.</td>
					</tr>
					<tr>
						<td><code class="chunk">onError</code></td>
						<td>This event fires if there is an error with the video in the specified player. The data associated with it is as follows:
						<ul>
							<li><b>2</b> - if the request contains an invalid parameter value</li>
							<li><b>5</b> - any error associated with HTML5, such as the HTML5 player not supporting the video</li>
							<li><b>100</b> - the video requested was not found</li>
							<li><b>101</b> - the owner of the video does not allow it to be played in an embedded player</li>
							<li><b>150</b> - same functionality as <b>101</b></li>
						</ul>
						</td>
					</tr>
				</table>
				
				<br />
				
				<h4>Code example</h4>
				
				<p><code class="chunk">
				function onPlayerReady(event) {<br />
				&nbsp;&nbsp;&nbsp;var embedCode = event.target.getVideoEmbedCode();<br />
				&nbsp;&nbsp;&nbsp;event.target.playVideo();<br />
				&nbsp;&nbsp;&nbsp;if (document.getElementById('embed-code')) {<br />
				&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;document.getElementById('embed-code').innerHTML = embedCode;<br />
				&nbsp;&nbsp;&nbsp;}<br />
				}
				</code><br /><br />
				
				The function takes an event object (<code>event</code>) as a parameter. The event object has a property named <code>target</code>, which points to the player itself. The <code>playVideo()</code> function is then called to begin the video. The <code>if</code> statement checks if there is an element with the <code>id</code> 'embed-code', and places the video in its spot.
				<br /><br />
				If you were to pass in <code>onReady</code> as the event, the video would play as soon as the player loaded it.</p>
				
				<br />
				</div>
	
			</div>
		&lt;/div&gt;
		
		<br /><br />
		
		<!-- Playback Controls -->	
		<div class="outer">
			<div id="playbackControls"></div>
				<div class="inner-heading">	
					<h3><br />Playback Controls<br /><br /></h3>
				</div>
				<div class="inner-body">
				
				<h4>Playing a video</h4>
				
				<p>The following functions deal with playing an embedded video.</p>
				
				<table border="1">
					<tr>
						<td><code class="chunk">player.playVideo()</code></td>
						<td>Plays the video and leaves it in a state of playing (1).</td>
					</tr>
					<tr>
						<td><code class="chunk">player.pauseVideo()</code></td>
						<td>Pauses the video and leaves it in a state of paused (2), unless the video has ended, then it will not change from ended (0).</td>
					</tr>
					<tr>
						<td><code class="chunk">player.stopVideo()</code></td>
						<td>Stops the video and prevents further loading. This should be used on rare occasions, such as only allowing the user to view one video per player. This can leave the player in any state.</td>
					</tr>
					<tr>
						<td><code class="chunk">player.seekTo()</code></td>
						<td>Seeks to a specified point in the video, unless the video is paused, in which case it will remain paused. This function has two parameters:
						<ul>
							<li><code>seconds</code>: Tells the function where to seek ahead to.</li>
							<li><code>allowSeekAhead</code>: This is a boolean that decides whether or not the video can seek to a portion that has not yet been loaded.</li>
						</ul>
						</td>
					</tr>
				</table>
				
				<h4>Some Useful Controls</h4>
				<ul>
					<li><code>player.mute()</code></li>
					<li><code>player.unMute()</code></li>
					<li><code>player.setVolume()</code></li>
					<li><code>player.setSize()</code></li>
					<li><code>player.setLoop()</code></li>
					<li><code>player.setPlaybackRate()</code></li>
					<li><code>player.setPlaybackQuality()</code></li>
				</ul>
				
				<p>Other useful controls can be found on the API developer website. The ones depicted in this guide are some that are most commonly used.</p>
				
				</div>
			
			</div>
		&lt;/div&gt;	
		
		<br /><br />

		<!-- Embedded Video -->	
		<div class="outer">
			<div id="exampleVideo"></div>
				<div class="inner-heading">	
					<h3><br />Example Video<br /><br /></h3>
				</div>
				<div class="inner-body">
				
				<center><div id="playerDiv"></div>
				
				<br /><br />
				
				<p>The implementation code of the video above is shown below. Refer to the Embedding a Video section for further explanation.</p>
				
				<br />
				
				<img src="codeImage.jpg" alt="JavaScript Code" /> </center>
					
				<br />
				</div>
			
			</div>
		&lt;/div&gt;	


</li></ul></p></p></div></div></li></ul></div></div></span></div></div></div></body>


      <footer class="site-footer">
        
          <span class="site-footer-owner"><a href="https://github.com/barrmelissa/youtubeAPI">youtubeAPI</a> is maintained by <a href="https://github.com/barrmelissa">barrmelissa</a>.</span>
        
        <span class="site-footer-credits">This page was generated by <a href="https://pages.github.com">GitHub Pages</a>.</span>
      </footer>
    </section>

    
  </body>
</html>
