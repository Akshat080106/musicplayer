# musicplayer

HTML:

<script src="https://kit.fontawesome.com/68471e9dca.js" crossorigin="anonymous"></script>: Imports the Font Awesome icon library.
<div class="container">: Wraps the content in a container.
<div class="music-player">: Represents the main music player container.
<div class="circle">: Represents circular elements in the navigation.
<i class="fa-solid fa-angle-left"></i>: Displays a left-angle icon.
<i class="fa-solid fa-bars"></i>: Displays a bars icon.
<img src="media\thumbnail.jpeg.jpeg" alt="song-img" class="song-img">: Displays an image with the song thumbnail.
<h1>: Heading for the song title.
<p>: Paragraph for the song artist.
<audio id="song">: Defines an audio player with the ID "song."
<source src="media\I-Hope-You're-Happy-But-Not-Like-How-You-Were-With-Me_320(PaglaSongs).mp3" type="audio/mpeg">: Specifies the audio file source.
<input type="range" value="0" id="progress">: Represents a range input for the song progress.
<div class="controls">: Contains the playback control buttons.
<div><i class="fa-solid fa-backward"></i></div>: Represents a backward control button.
<div onclick="playPause()"><i class="fa-solid fa-play" id="ctrlIcon"></i></div>: Represents a play/pause control button with an associated function.
<div><i class="fa-solid fa-forward"></i></div>: Represents a forward control button.
<script>: Contains JavaScript code.

JAVASCRIPT:
let progress= document.getElementById("progress");: Declares a variable for the progress input element.
let song= document.getElementById("song");: Declares a variable for the audio element.
let ctrlIcon= document.getElementById("ctrlIcon");: Declares a variable for the play/pause icon element.
song.onloadedmetadata= function(){...}: Defines a function executed when the audio metadata is loaded.
function playPause(){...}: Defines a function to play/pause the audio and toggle the icon.
if(song.play()){...}: Checks if the audio is playing and updates the progress continuously.
progress.onchange= function(){...}: Defines a function executed when the progress input changes to update the audio playback position.

CSS:
*: Universal selector setting margin and padding to 0, using 'Poppins' font, and applying box-sizing:border-box to all elements.

- .container: Styles for a container div.
  - width: 100%; sets its width to 100%.
  - height: 100vh; makes its height 100% of the viewport height.
  - background: #333; sets the background color to a dark gray.
  - display: flex; enables flexbox layout.
  - align-items: center; centers items vertically.
  - justify-content: center; centers items horizontally.
  - flex-wrap: wrap; allows items to wrap to the next line if necessary.

- .music-player: Styles for the main music player container.
  - background: #ffe0e5;` sets a light pink background.
  - width: 400px; sets a fixed width.
  - padding: 25px 35px; adds padding.
  - text-align: center; centers the text.

- nav: Styles for the navigation section.
  - display: flex; enables flexbox layout.
  - justify-content: space-between; evenly distributes items horizontally.
  - margin-bottom: 30px; adds margin at the bottom.

- nav .circle: Styles for circular elements in the navigation.
  - border-radius: 50%; creates a circle.
  - width: 40px; height: 40px; sets dimensions.
  - line-height: 40px; centers content vertically.
  - background: #fff; sets a white background.
  - color: #f53192; sets text color.
  - box-shadow: 0 5px 10px rgba(255, 26, 26, 0.22); adds a subtle shadow.

- .song-img: Styles for the song image.
  - width: 220px; sets a fixed width.
  - border-radius: 50%; creates a circular shape.
  - border: 8px solid #fff; adds a white border.
  - box-shadow: 0 10px 60px rgba(255, 26, 26, 0.22); adds a shadow.

- .music-player h1: Styles for the heading within the music player.
  - font-size: 20px; sets the font size.
  - font-weight: 400; sets the font weight.
  - color: #333; sets the text color.
  - margin-top: 20px; adds margin at the top.

- .music-player p: Styles for paragraphs within the music player.
  - font-size: 14px; sets the font size.
  - color: #333; sets the text color.

- #progress: Styles for the progress input.
  - -webkit-appearance: none; removes the default styling.
  - width: 100%; spans the full width.
  - height: 6px; sets the height.
  - background: #f53192; sets the background color.
  - border-radius: 4px; adds rounded corners.
  - cursor: pointer; changes the cursor on hover.
  - margin: 40px 0; adds margin at the top and bottom.

- #progress::-webkit-slider-thumb: Styles for the slider thumb in WebKit browsers.
  - -webkit-appearance: none; removes the default styling.
  - background: #f53192; sets the background color.
  - width: 30px; height: 30px; sets dimensions.
  - border-radius: 50%; creates a circular shape.
  - border: 8px solid #fff; adds a white border.
  - box-shadow: 0 5px 5px rgba(255, 26, 26, 0.22); adds a subtle shadow.

- .controls: Styles for the playback control buttons.
  - display: flex; enables flexbox layout.
  - justify-content: center; centers items horizontally.
  - align-items: center; centers items vertically.

- .controls div: Styles for individual control buttons.
  - `width: 60px; height: 60px;` sets dimensions.
  - `margin: 20px;` adds margin.
  - `background: #fff;` sets a white background.
  - `display: inline-flex;` enables inline flexbox layout.
  - `align-items: center; justify-content: center;` centers content.
  - `border-radius: 50%;` creates a circular shape.
  - `color: #f53192;` sets text color.
  - `box-shadow: 0 10px 20px rgba(255, 26, 26, 0.22);` adds a subtle shadow.

- .controls div:nth-child(2): Styles for the play/pause control button.
  - `transform: scale(1.5); increases the size.
  - `background: #f53192; color: #fff; sets background and text color
