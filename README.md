/* CSS Document - Header (with right slide navigation) code-clip */


/********************************************
		Header
*********************************************/

/* NOTE: JS used with the following functions:
		 
		 //  Hide menu and apply click event to show/hide
		 //  Move headerText div outside the carousel on listing pages and appeal pages
		 //  Apply page class if carousel contains an image
		 //  Apply page class if carousel contains a carouselSlideSummary (optional)
		 //  Move the admin menu into the main menu
		 //  Move main call to action donate button to after the alt menu button so that float right gives correct layout
		 //  Convert the page-header to be fixed when scrolled down
		 //  Adjust the stored padding sizes when the window size changes
		 //  Function to reduce calls from event handlers i.e. resize event
		 
		 */
		 
		 
/* Removes elements that shouldn't be displayed */		 
.headerFollowContainer { display: none; }		 
		 
		 
/* General */
.pageHeader {
	position: fixed;
	z-index: 500;
	top: 0;
	left: 0;
	right: 0;
	padding: 30px 20px 26px;
}
.page-has-banner .pageHeader {
	background: #323638;
	background: rgba(50, 54, 56, 0.9) none repeat scroll 0 0;
}
.page-no-banner .pageHeader {
	background: #323638;
	background: rgba(50, 54, 56, 0.9);
	position: fixed;
}
.pageHeader .headerContent {
	width: auto;
	max-width: none;
}
.pageHeader .headerContent:after {
	clear: none;
}
.mainLogo {
	background:url("http://placehold.it/250x39/ffffff/666666/&text=Any+size+logo");
	margin: 0;
	height: 39px;
	width: 250px;
}

/*  - Search button magnifier  */
.menuMain > form { clear: right; }
.searchContainer { position: relative; margin-top: 5px; }
#siteSearch { font-size: 14px; font-size: 1.4rem; height: 38px; width: 100%; padding-left: 17px; padding-right: 40px; background: #000000; color: #ffffff; -webkit-border-radius: 38px; -moz-border-radius: 38px; border-radius: 38px; border: 0; margin-top: 0; }
::-webkit-input-placeholder,
:-moz-placeholder, /** Firefox 18- */
::-moz-placeholder,  /** Firefox 19+ */
:-ms-input-placeholder { color: #000; }
.menuMain .searchContainer button:before { font-family: 'Genericons'; content: '\f400'; color: #d6085f; font-size: 24px; font-size: 2.4rem; }
.menuMain .searchContainer button { background-color: transparent; height: 22px; position: absolute; right: 2px; top: 4px; width: 22px; padding: 0; margin: 4px 15px; overflow: hidden; }
.menuMain .searchContainer button:hover,
.menuMain .searchContainer button:focus { background-color: transparent; }

/* Navigation */
.menuMainAlt:link,
.menuMainAlt:visited,
.menuMainAlt:active {
	display: block;
	margin-top: 5px;
	margin-left: 15px;
	color: #fff;
	font-size: 16px;
	font-size: 1.6rem;
}
.menuMainAlt:hover,
.menuMainAlt:focus {
	text-decoration: none;
}
.menuMainAlt:after {
	content: "\f419";
    font-family: "Genericons";
    font-size: 35px;
    line-height: 0;
    padding: 2px 5px 2px 15px;
    vertical-align: middle;
}
#menuMain.menuMain .menuMainCloseBtn {
	position: absolute;
	top: 10px;
	right: 10px;
	width: 21px;
	height: 20px;
	overflow: hidden;
	color: #ffffff;
	display: none;
}
.menuMainCloseBtn:before {
	display: block;
	width: 20px;
	height: 20px;
	font-family: "Genericons";
	content: "\f406";
	font-size: 20px;
	line-height: 1;
	padding: 1px 0 0;
}
.menuMain {
	background: #000;
    background-color: rgba(0, 0, 0, 0.85);
    float: right;
    width: 400px;
	position: fixed;
	top: 0;
	right: 0;
	z-index: 99999;
	overflow: hidden;
	padding: 60px 53px 0;
	height:100%;
	overflow:scroll;
}
.menuMain.open {
	transition: padding ease .3s, width ease .3s;
}
#menuMain.menuMain > * {
	width: 294px;
}
.menuMain .searchContainer {
	float: none;
}
.menuMain .menuAdminContainer {
	height: auto;
	background: transparent;
}
.menuMain .topLevel,
.menuMain ul#menuAdmin {
	margin: 60px auto;
	width: auto;
}
.menuMain .topLevel li,
.menuMain ul#menuAdmin li {
	display: block;
}
.menuMain .topLevel li.menuAdminAltItems {
	display:none;
}
.menuMain ul li a {
	color: #fff;
    font-size: 21px;
	font-size: 2.1rem;
    height: auto;
    padding: 11px 0;
}
.menuMain li.hasSubmenu > a:after {
    content: "+";
    display: block;
    font-size: 1.5em;
    padding: 0 0.5em;
    position: absolute;
    right: 0;
    top: 0;
}
.menuMain li.hasSubmenu > a.active:after {
	content: "-";
}
.subMenu {
	background-color: transparent;
	border: none;
	box-shadow: none;
	min-width: inherit;
	position: relative;
}
.menuMain .subMenu.active {
   display: block;
}
.subMenu ul { left: auto; top: auto; }
.menuMain ul.subMenu li > a { font-size: 18px; font-size: 1.8rem; padding: 0 10px 8px; }
.menuMain ul.subMenu ul li > a { padding-left: 30px; }
.menuMain ul.submenu ul ul li > a { padding-left: 50px; }
.menuMain ul ul > li a,
.menuMain ul ul > li a:hover { background: transparent; }
.menuMain ul#menuAdmin li a {
	border: 0;
	color: #bbb;
    padding: 8px 0;
}
.menuMain ul#menuAdmin li a:hover {
	background: transparent;
}

.menuMain .adminBar,
.menuMain .adminBarEdit {
	background: transparent;
	box-shadow: none;
}
.menuMain .adminBar .adminName {
	display: block;
}
.menuMain .editPostDetails {
	width: 100%;
}
.menuMain .adminBarEdit fieldset {
	width: 55%;
	float:right;
	margin-top: 15px;
	padding-bottom: 10px;
}


/* Media Queries */
@media screen and (max-width: 945px){
.menuMainAlt:link,
.menuMainAlt:visited,
.menuMainAlt:active {
	margin-right: 0 !important;
}
#menuMain.menuMain .menuMainCloseBtn {
	display: block;
}
}

@media screen and (max-width: 768px){
a.menuMainAlt { background-color: transparent; width: auto; }
a.menuMainAlt:before { content: ""; display: none; }
.menuMain ul { display: block; }
.menuMain > ul { border: 0; }
.menuMain,
.menuMain.active { max-height: none; }
.menuMain > ul ul,
.menuMain > ul ul.active { background: transparent; }
.menuMain ul li a { text-align: left; border: 0; }
.menuAdminContainer { display: block; }
}

@media screen and (max-width: 420px){
.page-has-banner .pageHeader { background: #222222; background: rgba(34, 34, 34, 0.9); }
.pageHeader { padding: 30px 20px 26px; }
.pageWrapper,
.homepage .contentContainer { padding-top: 69px; }
body.page-no-banner .pageWrapper { padding-top: 0; }

.mainLogo { background-size: contain; width: 53%; }

.menuMainAlt:link,
.menuMainAlt:visited,
.menuMainAlt:active {
	margin-top: 0;
	display: block;
}
.menuMain {
	width: 320px;
	padding: 40px 20px 0;
}
}

/****** End Header ******/
