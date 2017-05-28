<meta charset="UTF-8">
<link rel="stylesheet" type="text/css" href="style.css">
	
<script src="script.js"></script>
		
<html lang="en-us">

<head>
 <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
    <title>YouTube API Home</title>
    <meta name="heywords" content="" />
    <meta name="description" content="content1"/>
    <meta name="viewport" content="width=device-width, initial-scale=20">
    <meta name="theme-color" content="#157878">
    <link href="http://fonts.googleapis.com/css?family=Varela" rel="stylesheet" />
    <link href="default.css" rel="stylesheet" type="text/css" media="all" />
    <link href="fonts.css" rel="stylesheet" type="text/css" media="all" />
    
<html>
<head>
<style>
body {
    margin: 0;
    font-family: 'Lato', sans-serif;
}

.overlay {
    height: 100%;
    width: 0;
    position: fixed;
    z-index: 1;
    top: 0;
    left: 0;
    background-color: rgb(0,0,0);
    background-color: rgba(0,0,0, 0.9);
    overflow-x: hidden;
    transition: 0.5s;
}

.overlay-content {
    position: relative;
    top: 25%;
    width: 100%;
    text-align: center;
    margin-top: 30px;
}

.overlay a {
    padding: 8px;
    text-decoration: none;
    font-size: 36px;
    color: #818181;
    display: block;
    transition: 0.3s;
}

.overlay a:hover, .overlay a:focus {
    color: #f1f1f1;
}

.overlay .closebtn {
    position: absolute;
    top: 20px;
    right: 45px;
    font-size: 60px;
}

@media screen and (max-height: 450px) {
  .overlay a {font-size: 20px}
  .overlay .closebtn {
    font-size: 40px;
    top: 15px;
    right: 35px;
  }
}
</style>
</head>
<body>

<div id="myNav" class="overlay">
  <a href="javascript:void(0)" class="closebtn" onclick="closeNav()">&times;</a>
  <div class="overlay-content">
    <a onclick="closeNav()" href="#aboutThisGuide">Introduction</a>
    <a onclick="closeNav()" href="#embedVideo">Embedding a Video</a>
    <a onclick="closeNav()" href="#queueFunctions">Queuing Functions</a>
    <a onclick="closeNav()" href="#eventsPage">Event Handlers</a>
    <a onclick="closeNav()" href="#playbackControls">Playback Controls</a>
    <a onclick="closeNav()" href="#exampleVideo">Example Video</a>
  </div>
</div>


<span style="font-size:30px;cursor:pointer" onclick="openNav()">&#9776; Menu</span>

<script>
function openNav() {
    document.getElementById("myNav").style.width = "100%";
}

function closeNav() {
    document.getElementById("myNav").style.width = "0%";
}
</script>
     
</body>
</html>


  </head>
  <body>

   <!-- <section class="main-content">
      <h2 id="youtube-iframe-api">YouTube iFrame API</h2>
 
<!--<nav class="navigation">
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
		</nav> -->

	<div class="outer">
	<div class="inner-title">
	<center><h1>The Basics of YouTube API</h1>
	<h4><font>By: Melissa Barr </font></h4></center>
	<br />
	</div>
	</div>
	
	<html>
  <body>
    <!-- 1. The <iframe> (and video player) will replace this <div> tag. -->
    <div id="player"></div>

    <script>
      // 2. This code loads the IFrame Player API code asynchronously.
      var tag = document.createElement('script');

  tag.src = "https://www.youtube.com/iframe_api";
     var firstScriptTag = document.getElementsByTagName('script')[0];
     firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);

      // 3. This function creates an <iframe> (and YouTube player)
      //    after the API code downloads.
      var player;
      function onYouTubeIframeAPIReady() {
        player = new YT.Player('player', {
          height: '430',
          width: '700',
          videoId: '0HTexqxo1og',
          events: {
            'onReady': onPlayerReady,
            'onStateChange': onPlayerStateChange
          }
        });
      }

      // 4. The API will call this function when the video player is ready.
      function onPlayerReady(event) {
        event.target.playVideo();
      }

      // 5. The API calls this function when the player's state changes.
      //    The function indicates that when playing a video (state=1),
      //    the player should play for six seconds and then stop.
      var done = false;
      function onPlayerStateChange(event) {
        if (event.data == YT.PlayerState.PLAYING && !done) {
          setTimeout(stopVideo, 900000);
          done = true;
        }
      }
      function stopVideo() {
        player.stopVideo();
      }
    </script>
  </body>
</html>	
	<div class="outer">
	<div id="aboutThisGuide"></div>
			<div class="inner-heading">	
				<h2>Introduction</h2>
			</div>
			<div class="inner-body">
					
		<h5>What is the YouTube IFrame API?</h5>
		<p><left>The Iframe player API is a program that lets you embed a YouTube video player into your website and lets you program it to your specifications using JavaScript. There are many ways to personalize it. </left></p>
		<table class="offset">
				<tr>
					<th>For example you can:</th>
				</tr>
					<td>1. Play</td>
				<tr>
					<td>2. Pause</td>
				</tr>
					<td>3. Stop</td>
				<tr>
					<td>4. Adjust player volume</td>
				</tr>
					<td>5. Retrieve information about the video</td>
				<tr>
					<td>6. Add event listeners</td>
				</tr>
		</table>
				
		<p><left>I choose to do this program because it is a useful tool that can be added to any website either to support information, explain ideas, or just for fun!</left></p>
		<p><left>Here is where you can find the software and existing documentation for the YouTube IFrame API. Credit is given for code experts. 
		<a href="https://developers.google.com/youtube/iframe_api_reference">https://developers.google.com/youtube/iframe_api_reference</a></left></p>	
		<br /><div class="blackBar"></div><br />		
			<h2>Getting Started: How do you set it up?</h2>
			<h4>Requirements</h4>
			<p><left>There are a few requirements that you need:
					<li>A browser that supports the HTML5 postMessage feature (most browsers do but keep in mind that Internet Explorer 7 does not support this)</li>
					<li>The player must have an area at least 200px by 200px to play the video and if you decide to include controls then it must have room for that as well</li>
					<li>Must use the <code>onYouTubeIframeAPIReady</code> function - we will explain more on this later</li>
					<br /><br />Here is a sample HTML code that creates an embedded player that will load a video. Code explained below.</left></p>
					
	<img src="HTMLexampleYouTubeAPI.png" alt="YouTubeAPI" style="width:650px;height:800px;">
	
	<p><left>So lets talk about what’s going on here. 
	<br/><br/>Starting at the top at #1, the <code>&lt;div&gt;</code> tag is used to get the location on the page of where the video player will be placed. This is identified by the id to make sure that the <code>&lt;iframe&gt;</code> places it in the correct location.
	<br/><br/>Continuing on to #2, this is the part of the code that actually loads the Iframe Player API JavaScript code. The <code>&lt;script&gt;</code> part is needed to asynchronously download the code. It is important to keep in mind that this is not yet supported in all modern browsers.
	<br/><br/>Remember when we mentioned the <code>onYouTubeAPIReady</code> function before? This is where it comes into play. It is used to execute the code as soon as the player downloads. What is is actually doing is contracting a video player object but to phrase that in easier to understand terms it is defining the terms of the player and getting ready to play the video. There are a few ways to personalize this which we will go into detail in a bit but as shown you can specify the height, width, and when it plays.
	<br/><br/>While the previous function gets the video ready to play, the <code>onPlayerReady</code> function plays the video when it is ready. Again, this depends on the settings you have programmed it to.
	<br/><br/>Lastly #5 is all about changing the state of the player. The <code>onPlayerStateChange</code> function is for when the state of the player changes. This includes any of the 6 ways to personalize the video player shown in the introduction as well as more!
	<br/><br/>In this example specifically, you can see the number 6000. This means that the video will start playing and after 6 seconds the video will call the function <code>stopVideo()</code> and the player will stop it. As you can see from the video playing at the top of the website, it does not have this restriction on it because it is able to play throughout the whole video.</left></p>
				<br /><div class="blackBar"></div><br />		
		<br /><br />
		
		<div class="outer">
			<div id="embedVideo"></div>
				<div class="inner-heading">	
					<h3><br />Loading a Video<br /><br /></h3>
				</div>
				<p><left>Now that we have the basics down we can make adjustments to personalize the video player even more! Here is the code shown in #3 above but posted again to make it easier to follow.</left></p>

				<div class="inner-body">
				
				<table class="offset">
					<tr>
						<th>There are two parameters to consider here:</th>
					</tr>
					<td>1. The first parameter specifies either the DOM element of the <code>id</code> of the HTML element</td>
					&lt;/tr&gt;
					<tr>
						<td>2. The second parameter specifies the player options
</td>
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
