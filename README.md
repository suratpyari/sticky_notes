#This is a plugin for [JQuery](http://www.jquery.com) ([Github](https://github.com/suratpyari/sticky_notes))

By: [Surat Pyari]()

## Description

This plugin allows you to add sticky notes to the web page.

## Features

Add sticky notes
Moveable
Resizable
Ajaxified

## Requirement

jquery.js
jquery-ui.js

## Getting Started

Copy 'jquery-stickynotes.js' in your javascripts directory and 'stickyNote.css' in your stylesheets directory. Now add the following line in the head section of your page
	
    <script src="js/jquery-1.4.4.min.js" type="text/javascript"></script>
    <script src="js/jquery-ui-1.8.10.custom.min.js" type="text/javascript"></script>
    <script src="js/jquery-stickynotes.js" type="text/javascript"></script>
    <link href="css/ui-lightness/jquery-ui-1.8.10.custom.css" media="screen" rel="stylesheet" type="text/css" />
    <link href="css/stickyNote.css" media="screen" rel="stylesheet" type="text/css" />
    <script>
      $(function() {
        $("#sticky_notes").addStickyNotes({colors: ['#FDFB8C', '#FF99CC'], top: '120', left: '120', width: '200', height: '200'})
      })
    </script>
		
In body section you should add

    <div id="sticky_notes"></div>
	
Open your page in any browser and you can add notes, delete notes, resize the notes and even you can move the notes.

##Options

|Options    |Description                                                      |Default Value                                                                  |
|-----------|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
|colors     |Colors of sticky notes which is used as background of stick notes|['#FDFB8C', '#FF99CC', '#99FFCC', "#99CCFF"]                                   |
|color_index|Color index which will be used as background                     |0                                                                              |
|top        |Default top position of sticky note                              |0                                                                              | 
|left       |Default left position of sticky note                             |0                                                                              |
|width      |Default width of sticky note                                     |150                                                                            |
|height     |Default height of sticky note                                    |150                                                                            |
|url        |URL on which ajax request will be sent                           |'#'                                                                            | 
|method_type|GET or POST method                                               |POST                                                                           |
|save       |What fields to be send with request                              |['note', 'width', 'height', 'top', 'left', 'z-index', 'background-color', 'id']|
##Example 1

Add following code in head section

		<script>
			$(function() {
				$("#sticky_notes").addStickyNotes()
			})
		</script>

and add following code in body section if you already have some notes.

		<body>
			<div id="sticky_notes">
				<div class="stickyNote">
					<div class='note'>note 1</div>
				</div>
				<div class="stickyNote">
					<div class='note'>note 2</div>
				</div>
			</div>
		<body>	
	
##Example 2

Add following code in head section

		<script>
			$(function() {
				$("#sticky_notes").addStickyNotes({colors: ['#FDFB8C', '#FF99CC'], top: '120', left: '120', width: '200', height: '200'})
			})
		</script>

and add following code in body section if you already have some notes with options of height weight etc.

		<body>
			<div id="sticky_notes">
				<div class="stickyNote">
					<div class='note'>note 1</div>
					<div class='z_index'>1</div>
					<div class='left'>40</div>
					<div class='top'>100</div>
					<div class='color'>#FDFB8C</div>
					<div class='width'>200</div>
					<div class='height'>150</div>
					<div class='id'>1</div>
				</div>
				<div class="stickyNote">
					<div class='note'>note 2</div>
					<div class='z_index'>2</div>
					<div class='left'>60</div>
					<div class='top'>90</div>
					<div class='color'>#FF99CC</div>
					<div class='width'>100</div>
					<div class='height'>100</div>
					<div class='id'>2</div>
				</div>
			</div>
		<body>	