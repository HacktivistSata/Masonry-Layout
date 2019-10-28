# Msaonry-Layout
Making a responsive Layout for gallery

Installation:-

DOWNLOAD:- colcade.js
CDN:

<script src="https://unpkg.com/colcade@0/colcade.js"></script>
npm: npm install colcade

Bower: bower install colcade

USAGE:-
 
Colcade works by moving item elements into column elements.

HTML
<div class="grid">
  <!-- columns -->
  <div class="grid-col grid-col--1"></div>
  <div class="grid-col grid-col--2"></div>
  <div class="grid-col grid-col--3"></div>
  <div class="grid-col grid-col--4"></div>
  <!-- items -->
  <div class="grid-item">...</div>
  <div class="grid-item">...</div>
  <div class="grid-item">...</div>
  ...
</div>
CSS
Sizing of the columns is handled by your own CSS. Change the number of columns by hiding or showing them.

/* Using floats */
.grid-col {
  float: left;
  width: 50%;
}

/* 2 columns by default, hide columns 2 & 3 */
.grid-col--2, .grid-col--3 { display: none }

/* 3 columns at medium size */
@media ( min-width: 768px ) {
  .grid-col { width: 33.333%; }
  .grid-col--2 { display: block; } /* show column 2 */
}

/* 4 columns at large size */
@media ( min-width: 1080px ) {
  .grid-col { width: 25%; }
  .grid-col--3 { display: block; } /* show column 3 */
}

Methods
append
Add items to end of layout.

// jQuery
$grid.colcade( 'append', items )
// vanilla JS
colc.append( items )
prepend
Add items to beginning of layout.

// jQuery
$grid.colcade( 'prepend', items )
// vanilla JS
colc.prepend( items )
destroy
Remove Colcade behavior completely.

// jQuery
$grid.colcade('destroy')
// vanilla JS
colc.destroy()

By David DeSandro
MIT License. Have at it.
