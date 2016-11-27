# Jinn_Tali
@font-face {
	font-family: 'Carmela';
	src: url('../fonts/Carmela.eot?#iefix') format('embedded-opentype'),  url('../fonts/Carmela.woff') format('woff'), url('../fonts/Carmela.ttf')  format('truetype'), url('../fonts/Carmela.svg#Carmela') format('svg');
	font-weight: normal;
	font-style: normal;
}
@font-face {
	font-family: 'Carmela-Bold';
	src: url('../fonts/Carmela-Bold.eot?#iefix') format('embedded-opentype'),  url('../fonts/Carmela-Bold.woff') format('woff'), url('../fonts/Carmela-Bold.ttf')  format('truetype'), url('../fonts/Carmela-Bold.svg#Carmela-Bold') format('svg');
	font-weight: bold;
	font-style: normal;
}
body, html {
	margin: 0;
	padding: 0;
	width: 100%;
	height: 100%;
	overflow: hidden;
	color: black;
	font: normal 14px Carmela;
	background: white;
	direction: rtl;
	line-height: 1;
}
@media screen and (max-width: 768px) {
	body, html {
		overflow: auto; /* fixing various bugs, do not make hidden */
	}
}
body * {
	font-family: Carmela;	
}
dd {
	margin-left: 0;
	margin-right: 0.8em;
}
.button {
	cursor: pointer;
}
.hider {
	background: -moz-linear-gradient(left,  rgba(255,255,255,1) 0%, rgba(255,255,255,0) 100%); /* FF3.6-15 */
	background: -webkit-linear-gradient(left,  rgba(255,255,255,1) 0%,rgba(255,255,255,0) 100%); /* Chrome10-25,Safari5.1-6 */
	background: linear-gradient(to right,  rgba(255,255,255,1) 0%,rgba(255,255,255,0) 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
	filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#ffffff', endColorstr='#00ffffff',GradientType=1 ); /* IE6-9 */
	display: inline-block;	
	position: relative;
} 
a, a:hover, a:visited {
	color: #7A995D;
	text-decoration: none;
}
a.green {
	color: #7A995D !important;
}
/****************************************** main parts **********************************************/
#mainRight {
	width: 25%;	
	height: 100vh;
	background: white;
	float: right;
}
/*  iPad portrait */
@media all and (device-width: 768px) and (device-height: 1024px) and (orientation:portrait){
	#mainRight {
		height: 1024px;
	}
}
/* mobile */
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#mainRight {
		width: 0;
		overflow: hidden;
		position: absolute;
		z-index: 5;
		top: 4em;
	}
	#mainRight.open {
		width: 100%;
		-webkit-transition: width 0.3s ease-in-out;
		-moz-transition: width 0.3s ease-in-out;
		-o-transition: width 0.3s ease-in-out;
		transition: width 0.3s ease-in-out;
	}
}
#main {
	margin-right: 25%;
	background: #efefef;
	height: 100%;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#main {
		margin-right: 0;
	}
}
.tofesWrap {
	width: 100%;
}
.tofesHeaderFooterWrap {
	height: 4em;	
}
.tofesHeaderFooterWrap > div > * {
	line-height: 4em;
}
.tofesBodyWrap {
	height: calc(100vh - 8em);
}
.tofesBottomWrap {
	position: relative;
	bottom: 0;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	.tofesBottomWrap {
		display: none;
	}
}
@media screen and (max-device-width: 414px) and (-webkit-device-pixel-ratio: 2), (max-device-width: 736px) and (-webkit-device-pixel-ratio: 3) {
	.tofesBodyWrap {
		height: 81vh;
	}
	.ios .tofesBodyWrap {
		height: 70vh;
	}
	#tofesCart {
		height: 72vh !important;
	}
	.ios #tofesCart {
		height: 61vh !important;
	}
	#tofesCart ul {
		height: 50vh !important;
	}
	.ios #tofesCart ul {
		height: 39vh !important;
	}
}

#preloader {
	width: 100%;
	height: 100%;
	position: absolute;
	z-index: 6;
	display: block;
	background: white url(../images/tinyLoader.gif) no-repeat center center;
	opacity: 0.9;
	filter: alpha(90%);
}

.overlayDialog {
	display: none;
	position: absolute;
	width: 90vw;
	height: 90vh;
	z-index: 6;
	background: #F2F2F2;	
	-webkit-box-shadow: 1px 1px 15px 0 rgba(158,158,158,1);
	-moz-box-shadow: 1px 1px 15px 0 rgba(158,158,158,1);
	box-shadow: 1px 1px 15px 0 rgba(158,158,158,1);
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) { 
	.overlayDialog {
		width: 100vw;
		height: 100vh;	
		top: 0 !important; /* fix iphone bug */
	}
}
.overlayClose {
	color: inherit;
	font-size: 1.5em;
	text-decoration: none;
	display: block;
	width: 98%;
	padding: 1%;
	text-align: left;
}

input {
	background: transparent;
	border: medium none;
	padding: 1px;
	line-height: 1.1em;
	font-size: inherit;
}
textarea::-webkit-input-placeholder, input::-webkit-input-placeholder{
	color: #999;
}
textarea:-moz-placeholder, input:-moz-placeholder{
	color: #999;
} 
textarea:-ms-input-placeholder, input:-ms-input-placeholder{
	color: #999;
} 

.errorInput {
	background: #FFD4D4;
}

.result {
	font-weight: bold;
	color: #7A995D;
	font-size: 1.1em;
	display: none;
}
.result.error {
	color: #F14C4C;
}
.result span, .result i {
	font-size: 0.9em;
	margin-left: 3px;
}

.tofesSimpleTabs > ul {
	list-style-type: none;
	margin: 0;
	padding: 0;
}
.tofesSimpleTabs > ul li {
	margin: 0 5px;
	padding: 2px 0;	
	display: inline-block;
}
.tofesSimpleTabs > .tofesSimpleTabsTitle {
	border-bottom: 1px solid #ccc;
}
.tofesSimpleTabs > .tofesSimpleTabsTitle li {
	cursor: pointer;
}
.tofesSimpleTabs > .tofesSimpleTabsTitle li.active {
	color: #7A995D;
	border-bottom: 2px solid #7A995D;
}
.tofesSimpleTabs > .tofesSimpleTabsCnt > li {
	display: none;
	padding: 8px;
}
.tofesSimpleTabs > ul > li.active {
	display: inline-block;
}
.tofesSimpleTabs dt {
	margin-top: 10px;
}

/***************************************** main parts end *******************************************/
/**************************************** #toferProfilleWrap *****************************************/

#tofesProfileWrap {
	background: #9FB8C0;
}
#greeting {
	padding: 0 10px;
}
#greeting .fa-user {
	font-size: 2em;
}
#greeting .fa-user {
	font-size: 2em;
}
#greeting .fa-chevron-down {
	font-size: 1.2em;
	color: inherit;
	text-decoration: none;
	margin: 0 10px;
}
#profileMenuWrap, #mobileMenuWrap, #partnerMenuWrap {
	display: none;
}
.profileMenuTooltip {
	border-radius: 5px; 
	border: 2px solid #648C9A;
	background: white;
	color: inherit;
	font-family: inherit;
	font-size: inherit;
	line-height: 1;
}
.profileMenuTooltip .tooltipster-content {
	font-family: inherit;
	font-size: inherit;
	padding: 3px 10px 5px;
}
.profileMenu {
	list-style-type: none;
	margin: 0;
	padding: 0;
}
.profileMenu li {
	margin: 8px 5px 5px;
	padding: 5px;
	border-bottom: 1px solid gray;
}
.profileMenu li a {
	color: inherit;
	text-decoration: none;
	font-size: 1.1em;
	white-space: nowrap;
}
.profileMenu li.newSiteExpl {
	color: #7A995D;
}
.profileMenu li.logoutLink {
	border-bottom: medium none;
	padding-top: 10px;	
	margin-bottom: 0;
}
.profileMenu li.logoutLink a {
	font-size: 1em;	
}

@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape){
	#tofesProfileWrap {
		display: none;
	}
}
/************************************** #toferProfilleWrap ends **************************************/
/**************************************** #tofesCartWrap *******************************************/
#tofesCartWrap > div {
	padding: 10px;
	height: 100%;
}
#tofesCartLogo {
	padding: 2% 0 3%;
	height: 20%;
}
#tofesCartLogo img {
	display: block;
	margin: 0 auto;
	max-height: 100%;
	max-width: 100%;
}
#tofesCartLogo #beta {
	display: block;
	position: absolute;
	z-index: 1;
	width: 50px;
	height: 50px;	
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#tofesCartLogo {
		display: none;	
	}
}
#tofesCartTabs {
	white-space: nowrap;
	height: 4.8vh;
}
#tofesCartTabs > a  {
	display: inline-block;
	width: 50%;
	text-decoration: none;
	background: #9FB8C0;
	font-size: 2.2vh;
	text-align: center;
	color: inherit;
	padding: 1.3vh 0;
}
#tofesCartTabs > a.active  {
	background: #E3F0F4;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape){
	#tofesCartTabs > a{
		display: none;
	}
	#tofesCartTabs > a.active {
		display: block;
	}
	#tofesCartTabs #tofesOrdersTab {
		display: none;
	}
	#tofesCartTabs #tofesCartTab {
		width: 100%;
		font-size: 1.5em;
	}
}
#tofesCart {
	background: #E3F0F4;
	padding: 0 2% 2%;
	height: 57vh;
	display: block;
}
#tofesCartSaveWrap {
	display: block;
	padding: 1vh 0;
	text-align: center;
	text-decoration: none;
	color: inherit;
	font-size: 1.4vh;
	height: 2vh;
}
#tofesCartSaveWrap i.fa {
	margin: 0 3px;
	display: inline-block;	
	font-size: 1.4em;
}

#tofesCart ul {
	list-style-type: none;
	margin: 0;
	padding: 0;
	width: 100%;
	height: calc(43vh - 3em);
	overflow: scroll;
	overflow-x: hidden;
	visibility: hidden;
}
#tofesCart ul li, .tofesCartHeader, .userOrder {
	width: 100%;
	height: 2em;
	margin: 10px 0 5px;
	border-bottom: 1px solid black;	
	white-space: nowrap;
}
#tofesCart ul li > div, .tofesCartHeader > div, .userOrder > div {
	display: inline-block;
	margin: 0 1%;
	position: relative;
	vertical-align: middle;
	font-size: 0.9vw;
}
#tofesCart .tofesCartHeader > div, #tofesOrders .tofesCartHeader > div {
	font-weight: bold;	
	font-size: 0.9vw;
}
.tofesCartRemove {
	width: 5%;
}
.tofesCartRemove a {
	text-decoration: none;
	color: inherit;
}
.tofesCartAmount {
	width: 24%;
	text-align: center;
	padding: 0 2%;
}
.tofesCartAmountControl {
	color: inherit;
	line-height: 1em;
	font-weight: bold;
	font-size: 1.3em;
	text-align: center;
	text-decoration: none;
	padding: 0 5px;
}
.tofesCartTheAmount {
	font-weight: bold;
	font-size: 1.1em;
	text-align: center;
}
.tofesCartAmountUnit {
	text-align: center;
}
#tofesCart ul li .tofesCartName, .tofesCartHeader .tofesCartName {
	width: 31%;
	overflow: hidden;
	font-size: 1.1vw;
}
.tofesCartName .hider {
	float: left;
	width: 10px;
	height: 1em;
	background: -moz-linear-gradient(left,  rgba(227,240,244,1) 0%, rgba(227,240,244,0) 100%); /* FF3.6-15 */
	background: -webkit-linear-gradient(left,  rgba(227,240,244,1) 0%,rgba(227,240,244,0) 100%); /* Chrome10-25,Safari5.1-6 */
	background: linear-gradient(to right,  rgba(227,240,244,1) 0%,rgba(227,240,244,0) 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
	filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#e3f0f4', endColorstr='#00e3f0f4',GradientType=1 ); /* IE6-9 */	
}
.tofesCartName span {
	width: 100%;
	display: inline-block;
}
.tofesCartRemark {
	width: 8%;
	text-align: center;
}
.tofesCartRemark a {
	display: inline-block;
	width: 100%;
}
.tofesCartRemark a i.fa-file-text {
	display: none;
}
.tofesCartRemark a.hasRemark i.fa-file-text-o {
	display: none;
}
.tofesCartRemark a.hasRemark i.fa-file-text {
	display: block;
	color: #7A995D;
}
.tofesCartPrice {
	width: 18%;
	text-align: center;
}
.tofesCartThePrice {
	font-weight: bold;
	font-size: 1.1em;
}
.tofesCartCurrency {
	font-size: 0.8em;
}

#tofesCartInfo {
	padding-top: 1vh;
	height: 10.3vh;
	font-size: 1.6vh;
	visibility: hidden;
}
#tofesCartInfo > div {
	display: inline-block;
	vertical-align: top;
}
#tofesCartItemsTotalWrap {
	width: 45%;
}
#tofesCartIPriceTotalWrap {
	width: 53%;
}
#tofesCartInfo > div strong {
	font-size: 1.3vw;
}
#tofesCartItemsTotal, #tofesCartPriceTotal {
	margin-bottom: 1vh;
	white-space: nowrap;
}
#tofesCartPriceTheTotal {
	color: #BF2C30;
}
#tofesCartTotalRemarkHasFreeShipping {
	color: #7A995D;
}
#tofesCartInfo.hasFreeShipping #tofesCartTotalRemarkNoFreeShipping {
	display: none;
}
#tofesCartInfo.hasFreeShipping #tofesCartTotalRemarkHasFreeShipping {
	display: block;
	font-weight: bold;
}
#tofesCartInfo.hasFreeShipping #tofesCartPriceTheTotal {
	color: #7A995D;
}

.itemRemarkTooltip {
	border-radius: 5px; 
	border: 2px solid #7A995D;
	background: white;
	color: inherit;
	font-family: inherit;
	font-size: inherit;
	line-height: 1;
}
.itemRemarkTooltip .tooltipster-content {
	font-family: inherit;
	font-size: inherit;
	padding: 3px 10px 5px;
}
.itemRemarkTooltip .itemRemarkClose {
	display: block;
	text-align: left;
	font-size: 1.2em;
}
.itemRemarkTooltip textarea {
	resize: none;
	width: 250px;
	height: 50px;
	padding: 2px 5px;
}
.itemRemarkTooltip .itemRemarkButtons {
	padding: 8px 0 0;
	text-align: left;
}
.itemRemarkTooltip .itemRemarkSave {
	background: #7A995D;
	color: white;
	display: inline-block;
	padding: 8px 15px;
	margin-right: 20px;
}
.itemRemarkTooltip .itemRemarkClear {
	color: #999;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	.itemRemarkTooltip textarea {
		width: 100%;
	}
	.ios #tofesCart ul li .tofesCartName, .ios .tofesCartHeader .tofesCartName {
		width: 28%;
	}
}

#tofesOrders {
	background: #E3F0F4;
	padding: 0 2% 2%;
	height: 60vh;
	display: none;
}
#tofesOrders .tofesCartHeader {
	margin: 0;
	padding: 10px 0 5px;
}
#tofesOrders .tofesCartHeader > div, .userOrder > div {
	text-align: center;
}
#tofesOrders .items {
	overflow: scroll;
	overflow-x: hidden;
	height: calc(56vh - 3em - 10px);
}
.tofesOrderId {
	width: 15%;
}
.tofesOrderDate {
	width: 25%;
}
.tofesOrderCount {
	width: 17%;
	cursor: default;
}
#tofesOrders .pager ul {
	list-style-type: none;
	margin: 10px 0;
	padding: 0;
	text-align: center;
}
#tofesOrders .pager ul li {
	display: inline-block;
	margin: 0 15px;
}
#tofesOrders .pager ul li.hidden {
	visibility: hidden;
}
#tofesOrders .pager ul li a {
	font-size: 1.5em;
}

.orderItemsTooltip {
	border-radius: 5px; 
	border: 2px solid #7A995D;
	background: white;
	color: inherit;
	font-family: inherit;
	font-size: inherit;
	line-height: 1;
}
.orderItemsTooltip .tooltipster-content {
	font-family: inherit;
	font-size: inherit;
	padding: 10px 5px 0;
}

@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#tofesCart {
		height: 71vh;
	}
	#tofesCart ul {
		height: calc(57vh - 3em);
	}
	#tofesCartSaveWrap {
		font-size: 2.5vh;
	}
	#tofesCart .tofesCartHeader > div, #tofesOrders .tofesCartHeader > div {
		font-size: 4vw;
	}
	#tofesCart ul li > div, .tofesCartHeader > div, .userOrder > div {
		font-size: 4vw;
	}
	#tofesCart ul li .tofesCartName, .tofesCartHeader .tofesCartName {
		font-size: 5.5vw;
	}
	.ios #tofesCart ul li .tofesCartName, .ios .tofesCartHeader .tofesCartName {
		font-size: 4vw;
	}
	.tofesCartAmount {
		width: 29%;
		padding: 0;
	}
	.tofesCartAmountControl {
		line-height: 3vh;
		font-size: 5vh;
	}
	#tofesCartInfo {
		font-size: 2.6vh;
	}
	#tofesCartInfo {
		font-size: 1.9vh;
	}
	#tofesCartInfo > div strong {
		font-size: 5vw;
	}
	
	#tofesOrders {
		height: 71vh;
	}
	#tofesOrders .items {
		height: calc(68vh - 3em - 10px);
	}
}
@media screen and (device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	.tofesBodyWrap {
		height: calc(100vh - 10em);
	}
	#tofesCart .tofesCartHeader > div, #tofesOrders .tofesCartHeader > div, #tofesCart ul li > div, .tofesCartHeader > div, .userOrder > div,
	#tofesCart ul li .tofesCartName, .tofesCartHeader .tofesCartName {
		font-size: 2.5vw;
	}
	#tofesCartInfo > div strong {
		font-size: 4vw;
	}
	#tofesCartInfo > div {
		font-size: 1.7vw;
	}
	#tofesOrderBtn {
		line-height: 2.2em;
	}
}

/************************************** #tofesCartWrap ends****************************************/
/************************************** #tofesOrderBtnWrap ****************************************/

#tofesOrderBtn {
	border: medium none;
	background: #7A995D;
	font-size: 2em;
	margin: 0 auto;
	width: 95%;
	line-height: 1.8em;
	display: block;
}
#tofesOrderBtn.disabled {
	background: #F1B1A8;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#tofesOrderBtnWrap {
		display: block; /* overriding */
	}	
}

/************************************ #tofesOrderBtnWrap ends**************************************/

/************************************ #tofesMobileMenuWrap ****************************************/
#tofesMobileMenuWrap {
	display: none;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#tofesMobileMenuWrap {
		display: block;
		background: #9FB8C0;		
	}	
	#mobileMenuBtn {
		color: inherit;
		font-size: 2.5em;
		padding: 0.25em 2vw;
		display: block;
		float: right;
		width: 0.8em;
	}
	#tofesCartLogoMobile {
		display: inline-block;
		line-height: 1;
	}
	#tofesCartLogoMobile img {
		display: inline-block;
		height: 3em;
		padding: 0.4em 2vw;
	}
	#mobileTopLinks {
		float: left;
		line-height: 1;
	}
	#mobileTopLinks a {
		color: inherit;
		font-size: 2em;
		padding: 0.4em 0;
		display: inline-block;
		margin: 0 3vw;
	}
	#mobileTopLinks #mobileOrdersLink {
		display: none;
		font-size: 1.2em;
		text-decoration: underline;
	}
	#mobileTopLinks #mobileCartLink.hasItems {
		color: #7A995D;
	}
	
	.profileMenuTooltip .tooltipster-arrow-border, .profileMenuTooltip .tooltipster-arrow-bottom span {
		left: -59px;
	}
	
	#mobileMenuTop {
		background: #9EB7BF;
		padding: 0.5em;
		text-align: center;
	}
	#mobileMenuTop .overlayClose {
		text-align: right;
		font-size: 30px;		
		position: absolute;
	}
	#mobileMenuPartner {
		padding: 0.3em 0.5em;
		background: #5C8695;
		color: black;
		font-size: 1.6em;
		font-weight: bold;
	}
	#mobileMenuProfile {
		padding: 1.5em 1em;
	}
	#mobileMenuProfile > * {
		font-size: 1.5em;
	}
	#mobileMenuProfile .fa {
		font-size: 1.75em;		
	}
	#mobileMenuProfile > div.right {
		margin-left: 0.5em;
		max-width: 45%;
	}
	#mobileMenuProfileUserLinks a.big {
		background: #7A995D;
		padding: 0.3em 1em;
		color: white;
		display: block;
		text-align: center;
	}
	#mobileMenuProfileUserLinks a.logoutLink {
		background: transparent;
		padding: 0;
		margin-top: 0.5em;
		color: black;
		font-size: 0.9em; 
		display: block;
	}
	.mobileMenu {
		list-style-type: none;
		margin: 0;
		padding: 0;
	}
	.mobileMenu li {
		margin: 8px 5px 5px;
		padding: 5px;
		border-bottom: 1px solid gray;
	}
	.mobileMenu li a {
		color: inherit;
		text-decoration: none;
		font-size: 1.5em;
		white-space: nowrap;
	}
	.mobileMenu .feedbackLinkWrap {
		border: medium none;
		padding: 1em 0;
		text-align: center;
	}
	.mobileMenu .feedbackLink {
		background: white;
		border: medium none;
		font-size: 1.8em;
		padding: 0.3em 0.5em;
	}
	#mobilePartnerWrap {
		font-size: 1.2em;
	}
	#mobilePartnerWrap div {
		width: 30vw;
		height: 30vw;
		margin: 0 auto;
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center center;
	}
}

@media screen and (max-device-width: 736px) {
	#tofesCartLogoMobile img {
		height: 2.2em;
		padding: 0.8em 2vw;
	}
}

/************************************ #tofesMobileMenuWrap ends ***********************************/
/*************************************** #tofesSearchWrap *****************************************/
#tofesSearchPartnerWrap {
	background: #9FB8C0;
	white-space: nowrap;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#tofesSearchPartnerWrap {
		background: white;
	}
}
#tofesSearchPartnerWrap > div {
	position: relative;
	display: inline-block;
}
#tofesSearchWrap {
	width: 85.1%;
}
#searchInput {
	margin: 0.5em auto;
	width: 98%;
	border: medium none;
	padding: 0 1% 0 34px;
	min-height: 38px;
	line-height: 1.2em;
	background: white url(../images/search.png) no-repeat 5px center;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#tofesSearchPartnerWrap {
		display: none;		
	}
	#tofesSearchWrap {
		width: 100%;
	}
	#searchInput {
		background-color: #F2F2F2;
		display: block;
		width: 96%;
	}
	#tofesPartnerWrap {
		display: none !important;
	}
}
#searchInput.loading {
	background-image: url(../images/tinyLoader.gif);
}
#searchResults {
	width: 97%;
	padding: 0 0.5% 0.5%;
	background: #F2F2F2;
	position: absolute;
	margin-top: -5px;
	z-index: 5;
	display: none;
}
#searchResults > div {
	overflow: scroll;
	overflow-x: hidden;
}
#searchItems {
	list-style-type: none;
	margin: 0;
	padding: 0;
}
#searchResults .tofesItemDescr {
	line-height: 3vh;
}
#searchResults .searchOnly {
	display: block !important;
}
#searchNoResults {
	color: gray;
	font-size: 1.5em;
	text-align: center;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#searchResults .tofesItemDescr .searchOnly {
		display: none !important;
	}
}

#tofesPartnerWrap {
	width: 8.9%;
	margin: 0.5em 0 0.5em 2%;
	height: 38px;
	line-height: 2.6em;
	float: left;
	position: relative;
	background-size: 50px auto;
	background-repeat: no-repeat;
	background-position: right center;
	cursor: pointer;
	background-color: white;
	text-align: right;
	padding-right: 50px;	
	font-size: 1.2em;	
}
#tofesPartnerWrap > * {
	line-height: 1;
}
.partnerMenuTooltip {
	border-radius: 5px; 
	border: 2px solid #648C9A;
	background: white;
	color: inherit;
	font-family: inherit;
	font-size: inherit;
	line-height: 1;
}
.partnerMenuTooltip .tooltipster-arrow-border, .partnerMenuTooltip .tooltipster-arrow-bottom span {
	left: -145px;
}
.partnerMenuTooltip .tooltipster-content {
	font-family: inherit;
	font-size: inherit;
	padding: 3px 10px 5px;
}
.partnerMenuTooltip .partnerTabsCnt li {
	width: 200px;
}

/************************************* #tofesSearchWrap ends***************************************/
/*************************************** #tofesMainWrap *******************************************/
#tofesMainWrap {
	background: white;
}
#catsListWrap {
	overflow: hidden;
}
#catsList {
	list-style-type: none;
	padding: 0;
	margin: 0;
	background: white;	
	height: 5em;
	white-space: nowrap;
	position: relative;
}
#catsList li {
	margin: 0 0 0 10px;
	display: inline-block;
	padding: 0.5em 0;
}
#catsList li.active {
	background: #E5E5E5;
}
#catsList li span {
	text-decoration: none;
	color: inherit;
	display: block;
	padding: 5px 10px;
	text-align: center;
	cursor: pointer;
}
#catsList li span img {
	display: block;
	margin: 2px auto;
	width: 32px;
}
#catsListScroll {
	display: none;
	padding: 0.5em 1.5em 0;
	float: left;
	background: white;
	z-index: 1;
	position: relative;
	cursor: pointer;
}
#catsListScroll span {	
	text-decoration: none;
	color: #A0B9C1;
	display: block;
	padding: 8px 10px;
	text-align: center;
}
#catsListScroll img {
	display: block;
	border: none;
	margin: 2px auto;
}
#catsListScroll #catsListScrollPrev {
	display: none;
}
#catsListScroll.scrolled #catsListScrollPrev {
	display: block;
}
#catsListScroll.scrolled #catsListScrollNext {
	display: none;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#catsListWrap {
		overflow-x: scroll;
	}
	#catsListScroll {
		display: none !important;
	}
}

.tofesCatCnt {
	display: none;
}
.tofesCatDataWrap {
	background: #E5E5E5;
	width: 98%;
	height: calc(98vh - 13em);
	padding: 1vh 0 0;
}
.tofesCatDataWrap > div {
	padding: 0 10px;	
}
.tofesLayoutChangeWrap {
	float: left;
	position: relative;
	margin-left: 3%;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	.tofesLayoutChangeWrap {
		display: none;
	}
	.tofesCatDataWrap {
		width: 100%;
	}
}
.tofesLayoutChangeWrap span {
	display: inline-block;
	font-size: 2em;
	padding: 5px;
	cursor: pointer;
	color: gray;
}
.tofesLayoutChangeWrap span.active {
	color: inherit;
	cursor: default;
}
.tofesSubcatsList {
	min-height: 2.5em;
	color: #666;
}
span.tofesSubcatsMore {
	display: none;
}
.tofesSubcatsList ul {
	list-style-type: none;
	margin: 0;
	padding: 0;
	width: 95%;
}
.tofesSubcatsList ul li {
	display: inline-block;
	margin: 0 5px;
}
.tofesSubcatsList ul li a {
	color: inherit;
}
.tofesSubcatsList ul li.active a {
	color: #2E4A16;
	font-weight: bold;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	.tofesSubcatsList {
		overflow: hidden;
		min-height: 2em;
		padding-left: 0 !important;
	}
	.tofesSubcatsList ul {
		white-space: nowrap;
		width: 1000px;;
	}
	span.tofesSubcatsMore {
		display: block;
		color: #666;
		float: left;
		background: #E5E5E5;
		padding: 0 15px 0 10px;
		z-index: 1;
		position: relative;
	}
	.subcatsListTooltip {
		display: block;
		position: fixed;
		top: 15em;
		left: 3vw;
		width: 93vw;
		height: calc(98vh - 16em);
		background-color: white;
		-webkit-box-shadow: 3px 3px 5px -1px rgba(158,158,158,1);
		-moz-box-shadow: 3px 3px 5px -1px rgba(158,158,158,1);
		box-shadow: 3px 3px 5px -1px rgba(158,158,158,1);
		padding: 1vh 1vw;
		z-index: 100;
		overflow: scroll;
	}
	.ios .subcatsListTooltip {
		height: calc(87vh - 16em);
	}
	.subcatsListTooltip .subcatsListTooltipClose {
		display: block;
		text-align: left;
		font-size: 1.2em;
	}
	.subcatsListTooltip ul {
		list-style-type: none;
	}
	.subcatsListTooltip ul li {		
		padding: 5px;
		border-top: 1px solid #ccc;
	}
	.subcatsListTooltip ul li:first-child {
		border: medium none;
	}
	.subcatsListTooltip ul li a {
		font-size: 1.3em;
		color: inherit;
	}
}

.tofesItemsWrap {
	overflow: scroll;
	overflow-x: hidden;
	height: calc(98vh - 15.5em);
	background: #E5E5E5;
	padding: 0 !important;	
}
.tofesItemsSubcatWrap {
	padding-bottom: 1vh;
	position: relative;
}
.tofesItemsControl {
	display: block;
	position: absolute;
	height: 100%;
	width: 3vw;
	font-size: 2vw;
	cursor: pointer;
	z-index: 1;
	background-color: #E5E5E5;
	background-repeat: no-repeat;
	background-position: center center;
}
.tofesItemsControl.list {
	display: none !important;
}
.tofesItemsControl > div {
	height: 100%;
	width: 0.5vw;
}
.tofesItemsControlFwd {
	left: -1px;
}
.tofesItemsControlFwd > div {
	float: right;
	margin-right: -0.5vw;
}
.tofesItemsControlFwd.active {
	background-image: url(../images/nextGray.png);	
}
.tofesItemsControlFwd.active > div {
	background: -moz-linear-gradient(left,  rgba(229,229,229,1) 0%, rgba(125,185,232,0) 100%); /* FF3.6-15 */
	background: -webkit-linear-gradient(left,  rgba(229,229,229,1) 0%,rgba(125,185,232,0) 100%); /* Chrome10-25,Safari5.1-6 */
	background: linear-gradient(to right,  rgba(229,229,229,1) 0%,rgba(125,185,232,0) 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
	filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#e5e5e5', endColorstr='#007db9e8',GradientType=1 ); /* IE6-9 */
}
.tofesItemsControlBack {
	right: 0;
}
.tofesItemsControlBack > div {
	float: left;
	margin-left: -0.5vw;
}
.tofesItemsControlBack.active {
	background-image: url(../images/prevGray.png);
}
.tofesItemsControlBack.active > div {
	background: -moz-linear-gradient(left,  rgba(229,229,229,0) 0%, rgba(229,229,229,1) 100%); /* FF3.6-15 */
	background: -webkit-linear-gradient(left,  rgba(229,229,229,0) 0%,rgba(229,229,229,1) 100%); /* Chrome10-25,Safari5.1-6 */
	background: linear-gradient(to right,  rgba(229,229,229,0) 0%,rgba(229,229,229,1) 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
	filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#00e5e5e5', endColorstr='#e5e5e5',GradientType=1 ); /* IE6-9 */
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	.tofesItemsWrap {
		height: calc(100vh - 11em);
	}
	
	.tofesItemsControl {
		width: 6vw;
	}
}

.tofesItemsSubcat {
	margin: 0 3vw;
}
.tofesItemsSubcatName {
	margin: 0 10px;
	font-size: 1.3em;
}
.tofesItemsSubcatWrap ul {
	list-style-type: none;
	margin: 0;
	padding: 0;
	white-space: nowrap;
}
.tofesItemsSubcatWrap ul.list {
	white-space: normal;
	margin-right: 0 !important;
}
.tofesItemWrap {
	display: inline-block;
	margin: 10px;
	width: 230px;
	height: 230px;
	overflow: hidden;
	position: relative;
	
	box-shadow: none;
	background: transparent;
	border: medium none;
}
.tofesItemWrap.koed {
	border-bottom: 3px solid white;
	background-color: white;
	-webkit-box-shadow: 3px 3px 5px -1px rgba(158,158,158,1);
	-moz-box-shadow: 3px 3px 5px -1px rgba(158,158,158,1);
	box-shadow: 3px 3px 5px -1px rgba(158,158,158,1);	
}
.tofesItemWrap.list {
	display: block;
	width: 99.5%;
	height: 58px;
	margin: 0 0 2px;	
}
.tofesItemWrap.koed.list {
	-webkit-box-shadow: none;
	-moz-box-shadow: none;
	box-shadow: none;
	border-bottom: medium none;
	border-left: 3px solid white;
}
.tofesSaleTag {
	position: absolute;
	z-index: 1;
	top: 10px;
	right: 10px;
}
.list .tofesSaleTag {
	top: 1px;
	right: 0;
}
.tofesItemImg {
	width: 100%;
	height: 66%;
	background-repeat: no-repeat;
	background-size: contain;
	background-position: center center;
}
.list .tofesItemImg {
	width: 4vw;
	height: 100%;
	float: right;
}
.tofesItemImg.loading {
	background-size: auto;
}
.tofesItemData {
	height: 32%;
	padding: 1% 2%;
	overflow: hidden;
}
.list .tofesItemData {
	height: 100%;
	padding: 0;
	position: relative;
}
.list .tofesItemData > div {
	display: inline-block;
	vertical-align: middle;
	margin-right: 1.5vw;
	/*height: 100%;*/
	padding-top: 0;
	padding-bottom: 0;
	line-height: 1;
}
.tofesItemData .long {
	white-space: nowrap;
	width: 100%;
	overflow: hidden;
}
.tofesItemData .long > span {
	display: block;
	width: 100%;
	height: 100%;
}
.tofesItemProvider {
	height: 1em;
	font-size: 0.8em;
}
.list .tofesItemProvider {
	position: absolute;
	line-height: 1 !important;
	top: 4.5vh;
}
.tofesItemName {
	height: 1em;
	font-size: 1.2em;
	font-weight: bold;
	padding: 4px 0;
}
.list .tofesItemName {
	width: 15vw;
}
.tofesItemDescr {
	height: 1em;
}
.searchOnly {
	display: none !important;
}
.list .tofesItemDescr {
	width: 8vw;
}
.tofesItemRemark {
	display: block;
	position: absolute;
	top: 57%;
}
.tofesItemRemark.hasRemark i.fa-file-text-o {
	display: none;
}
.tofesItemRemark.hasRemark i.fa-file-text {
	display: inline-block;
	color: #7A995D;
}
.tofesItemRemark i.fa-file-text {
	display: none;
}
.list .tofesItemRemark {
	width: 3vw;
	display: inline-block;
	top: auto;
	white-space: nowrap;
	cursor: pointer;
	position: relative;
}

.tofesItemDataBottom {
	padding-top: 4px;
}
.list .tofesItemDataBottom {
	padding-top: 0;
}
.list .tofesItemDataBottom > div {
	display: inline-block;
	margin-right: 2vw;
}
.tofesItemPrice {
	float: right;	
}
.list .tofesItemPrice {
	float: none;
	width: 4vw;
	white-space: nowrap;
	line-height: 1;
	padding-top: 5px;
	margin-right: 1.5vw;
}
.tofesItemPrice .theprice {
	font-weight: bold;
}
.tofesItemUnitChoice {
	float: left;
	color: #666;
}
.tofesItemUnitChoice i {
	font-style: normal;
}
.list .tofesItemUnitChoice {
	float: none;
}
.tofesItemUnitChoice > span {
	cursor: pointer;
}
.tofesItemUnitChoice > span:hover {
	text-decoration: underline;
}
.tofesItemUnitChoice > span.selected {
	font-weight: bold;
	color: #7A995D;
	text-decoration: underline;
}
.tofesItemAmountWrap {
	position: absolute;
	top: 4%;
	left: 5%;
	text-align: center;
	display: none;
}
.list .tofesItemData > div.tofesItemAmountWrap {
	left: 3.5vw;
	top: 0;
	display: none;
}
@media screen and (min-width: 1024px) {
	.list .tofesItemData > div.tofesItemAmountWrap {
		left: 1vw;
		z-index: 2;
	}
}
.partlyAmount {
	display: block;
/*	text-align: right;
	color: #7A995D;*/
	cursor: pointer;
	/*font-size: 1.8em;*/
	width: 25px;
	left: 3.2vw;
	position: absolute;
	z-index: 1;
	top: 0;
}
.list .partlyAmount {
	left: 3vw;
}
.tofesItemAmount {
	background: #7A995D;
	border-radius: 50%;
	font-size: 2em;
	color: white;
	margin-bottom: 3px;
	font-weight: bold;
	width: 3vw;
	height: 3vw;
	display: table-cell;
	text-align: center;
	vertical-align: middle;
}
.list .tofesItemAmountUnit {
	color: #7A995D;
	display: block;
	position: absolute;
	top: 2vh;
	left: -1vw;
}
.partlyAmountTooltip {
	border-radius: 5px; 
	border: 2px solid #7A995D;
	background: white;
	color: inherit;
	font-family: inherit;
	font-size: inherit;
	line-height: 1;
}
.partlyAmountTooltip .tooltipster-content {
	font-family: inherit;
	font-size: inherit;
	padding: 3px 10px 5px;
}
.partlyAmountTooltip span.close {
	display: block;
	text-align: left;
	font-size: 1.2em;
}
.partlyAmountTooltip input {
	resize: none;
	width: 250px;
	height: 1.4em;
	padding: 0.1em 5px;
	font-size: 1.2em;
	margin-top: 5px;
	direction: ltr;
	text-align: left;
	border: 1px solid #aaa;
}
.partlyAmountTooltip span.save {
	background: #7A995D;
	color: white;
	display: block;
	padding: 8px 15px;
	margin: 8px 0 0;
	float: left;
}
@media screen and (max-height: 768px) {
	#searchResults .list .tofesItemName {
		line-height: 3vh;
	}
	#searchResults .tofesItemDescr {
		line-height: 2vh;
		color: red;
	}
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	.partlyAmountTooltip input {
		width: 100%;
	}
}

.tofesItemControls {
	position: absolute;
	top: 55%;
	left: 5%;
	white-space: nowrap;
}
.list .tofesItemControls {
	top: 0;
	left: 1vw;
	z-index: 1;
}
.tofesItemControls > a {
	background: #7A995D;
	border-radius: 50%;
	color: white;
	display: inline-block;	
	text-decoration: none;
	font-weight: bold;
}
.list .tofesItemControls > a {
	display: inline-block;
	margin-top: 7px;
	line-height: 1;
}
.tofesItemControls .tofesItemAdd {
	padding: 5px 16px;
}
.tofesItemControls .tofesItemRemove {
	padding: 0 10px;
}
.tofesItemControls .tofesItemAdd {
	font-size: 2em;
	padding: 8px 16px;
}
.tofesItemControls .tofesItemRemove {
	font-size: 2em;
	padding: 3px 10px;
	margin-left: 10px;
	display: none;
}
.list .tofesItemControls .tofesItemRemove {
	margin-left: 5.6vw;
}
@media screen and (min-width: 1024px) {
	.list .tofesItemWrap:not(.mobile) .tofesItemControls > a {
		font-size: 2em;
		padding: 0;
		font-weight: bold;
		width: 2.5vw;
		height: 2.5vw;
		line-height: 2.5vw;
		text-align: center;
		vertical-align: middle;
		margin-bottom: 4px;
	}	
	.list .tofesItemWrap:not(.mobile) .tofesItemControls > a.tofesItemRemove {
		width: 2vw;
		height: 2vw;
		line-height: 2vw;
		margin-left: 2vw;
	}
}

.tofesItemWrap.incart {
	border-bottom: 3px solid #7A995D;
}
.tofesItemWrap.incart.list {
	border-bottom: medium none;
	border-left: 3px solid #7A995D;
}
.tofesItemWrap.incart .tofesItemImg {
	opacity: 0.4;
	filter: alpha(4%);
}
/*.tofesItemWrap.incart.list .tofesItemImg {
	opacity: 1;
	filter: alpha(100%);
}*/
.tofesItemWrap.incart .tofesItemAmountWrap, .list.incart .tofesItemData > div.tofesItemAmountWrap {
	display: block;
}

.list .tofesItemWrap.incart .tofesItemAmountWrap {
	display: table-cell;
}
.tofesItemWrap.incart .tofesItemRemove {
	display: inline-block;
}

#tofesCatLoader {
	position: absolute;
	background: #E5E5E5 url(../images/tinyLoader.gif) no-repeat center center;
	z-index: 2;
}
#tofesCatLoader span {
	color: #7A995D;
	font-size: 2em;
	margin-top: 25vh;
	display: block;
	text-align: center;
}

@media screen and (max-width: 1024px) {
	.list .tofesItemRemark {
		text-align: left;
	}
	.list .tofesItemRemark span {
		display: none;
	}
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {	
	.tofesItemWrap.list {
		height: 65px;
		background: white;
	}	
	.tofesItemRight {
		float: right;		
		width: 11.4vh;
		position: relative;
		background: #E2EEF4;
	}
	.list .tofesItemImg {
		float: none;
		width: 100%;
		height: 70%;
	}	
	.list .tofesSaleTag {
		right: 1px;
	}
	.list .tofesItemPrice {
		width: 100%;
		line-height: 1.5em;
		white-space: normal;
		text-align: center;
		padding-top: 0;
	}
	.list .tofesItemData {
		/*overflow: visible;*/
		margin-right: 11.4vh;
		width: 40vw;
	}
	.tofesItemAmount {
		width: 18vw;
		height: 18vw;
	}
	.list .tofesItemAmount {
		font-size: 1.5em;
		width: 12vw;
		height: 12vw;
	}
	.tofesItemAmountWrap .partlyAmount {
		left: 19vw;
	}
	.list .tofesItemAmountWrap .partlyAmount {
		right: -7vw;
		left: auto;
	}
	.partlyAmountTooltip textarea {
		width: 100%;
	}
	.list .tofesItemData > div.tofesItemName, .list .tofesItemData > div.tofesItemDescr {
		display: block;
		height: auto;		
		line-height: 1;
		width: 98%;
		padding: 1vh 1%;
		white-space: normal;
	}
	.list .tofesItemData > div.tofesItemDescr {
		padding: 0;
		line-height: 5vh;
	}
	.list .tofesItemControls {
		position: relative;
		top: auto;
		left: auto;
		float: left;
		width: 30vw;
		height: 100%;
	}
	.list .tofesItemControls > a {
		margin-top: 2.2vh;
	}
	.list .tofesItemControls .tofesItemRemove {
		padding: 4px 10px;
		line-height: 1;
		margin-left: 4vw;
	}	
	.list .tofesItemControls .tofesItemAdd {
		font-size: 2em;
		width: 42px;
		line-height: 40px;
		padding: 0;
		text-align: center;
	}
	.list .tofesItemControls .tofesItemAdd.nonempty {
		font-size: 1.7em;
	}
	.list .tofesItemControls .partlyAmount {
		width: 4vh;		
		left: 12vw;
	}
	
	.mobileProductData {
		position: fixed;
		right: 1vh;
		background: white;
		-webkit-box-shadow: 3px 3px 5px -1px rgba(158,158,158,1);
		-moz-box-shadow: 3px 3px 5px -1px rgba(158,158,158,1);
		box-shadow: 3px 3px 5px -1px rgba(158,158,158,1);
		padding: 3vh;
		z-index: 100;
		border: 2px solid #7A995D;
		border-radius: 3px;
		width: 51vw;
		font-size: 1.2em;
	}
	.mobileProductDataClose {
		display: block;
		text-align: left;
		font-size: 1.1em;
		margin-bottom: 2vh;
	}
	.dataSaleTag {
		float: left;
		margin-right: 1vw;
	}
	.dataItemName {
		font-size: 1.1em;
		font-weight: bold;
		margin: 1vh 0;
	}
	.mobileProductData .tofesItemUnitChoice {
		float: none;
	}
	.dataItemRemark textarea {
		resize: none;
		width: 100%;
		height: 50px;
		padding: 2px 5px;
		border: 1px solid #7A995D;
	}
}

.subcatLoader {
	background: url(../images/tinyLoader.gif) no-repeat right center;
	display: none;
	margin: 0 10px 0 0;
	width: 32px;
	height: 1em;
	vertical-align: top;
}

.tofesItemsSubcat.loading .subcatLoader {
	display: inline-block;
}


/************************************** #tofesMainWrap ends****************************************/
/*************************************** #tofesFooterWrap ******************************************/
#tofesFooterWrap {
	background: white;
	z-index: 1;
	position: relative;
}
#tofesFooterWrap ul {
	list-style-type: none;
	padding: 0;
}
#tofesFooterWrap ul li {
	margin: 0 10px;
	display: inline-block;
}
#tofesFooterWrap ul li a {
	text-decoration: none;
	color: inherit;
}
#tofesFooterWrap .centered a {
	color: inherit;
	text-decoration: none;
}
.feedbackLink {
	color: #7A995D !important;
	font-weight: bold;
	border: 1px solid #7A995D;
	display: inline-block;
	padding: 0 10px;
	line-height: 1.5em !important;
}
#facebook {
	border-radius: 50%;
	color: white !important;
	text-decoration: none;
	padding: 9px 11px 3px;
	background: #0071BB;
	font-weight: bold;
	font-size: 1.2em;
}
/************************************* #tofesFooterWrap ends***************************************/
/******************************************* order wrap  *********************************************/
#orderUnderlayWrap {
	display: none;
	position: absolute;
	width: 100%;
	height: 100%;
	left: 0;
	top: 4em;
	background: white;
	opacity: 0.6;
	filter: alpha(60%);
	z-index: 5;
}
#orderWrap {
}

#orderTabs {
	list-style-type: none;
	margin: 0;
	padding: 0;
	width: 100%;
	border-bottom: 1px solid #9FB8C0;
}
#orderTabs li {
	display: inline-block;
	border-right: 1px solid #9FB8C0;
	width: 33.255%;
	text-align: center;
}
#orderTabs li:first-child {
	border-right: medium none;
}
#orderTabs li.active {
	background: #9FB8C0;
}
#orderTabs li a {
	color: inherit;
	text-decoration: none;
	line-height: 4em;
	font-weight: bold;
}
#orderTabs li a .orderTabNum {
	border: 1px solid black;
	border-radius: 50%;
	padding: 2px 5px;
	margin-left: 20px;
	display: inline-block;
	line-height: 1;
}
#orderTabs li a .orderTabNum i {
	display: none;
}
#orderTabs li.visited a .orderTabNum {
	border-color: #7A995D;
	background: #7A995D;
	color: white;	
	padding: 4px;
}
#orderTabs li.visited a .orderTabNum i {
	display: inline-block;
	font-size: 0.8em;
}
#orderTabs li.visited a .orderTabNum span {
	display: none;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#orderTabs li {
		width: 33%;
	}
	#orderTabs li a .orderTabNum {
		margin: 1vh 0;
	}
	.orderTabTitle {
		display: none;
	}
}

#orderMain {
	height: 60vh;
}
@media screen and (max-height: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#orderMain {
		height: 53vh;
	}
}
#orderMain > div {
	padding: 3% 3% 0 3%;
}
@media screen and (max-height: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#orderMain > div {
		padding: 0 3%;
	}
}

#orderBottom {
	height: 15vh;
	clear: both;
}
#orderBottomLinks > span {
	display: block;
	text-align: center;
	font-size: 1.2vw;
}
#orderBottomBack {
	display: block;
	position: absolute;
	right: 5%;
	bottom: 5%;
	color: #9B9B9B;
	font-weight: bold;
	text-decoration: none;
	font-size: 1.2em;
}

#orderNextBtn {
	background: #7A995D;
	line-height: 2.8em;
	text-align: center;
	font-weight: bold;
	font-size: 1.4em;
}
#orderNextBtn.disabled {
	background: #F1B1A8;
}
#orderNextBtn.doshow{
	display: block !important;
}

/****************************************** order wrap ends  *****************************************/
/********************************************* order tab 1 ********************************************/

#orderContentsHeader {
	line-height: 1em;
}
#orderContentsHeader a {
	float: left;
	text-decoration: none;
	color: inherit;
}
#orderContents ul {
	list-style-type: none;
	margin: 0;
	padding: 0;
	width: 100%;
	height: 40vh;
	overflow: scroll;
	overflow-x: hidden;
}
#orderContents ul li {
	width: 100%;
	height: 2em;
	margin: 10px 0 5px;
	border-bottom: 1px solid black;	
	white-space: nowrap;
}
#orderContents ul li > div {
	display: inline-block;
	margin: 0 1%;
	position: relative;
	vertical-align: middle;
	font-size: 0.9vw;
}
#orderContents .tofesCartHeader > div {
	font-weight: bold;	
	font-size: 0.9vw;
}
#orderContents ul li .tofesCartName {
	width: 31%;
	overflow: hidden;
	font-size: 1.3vw;
}
#orderBottomLeft {
	width: 30%;
	display: block;
	float: left;
	margin-left: 3%;
	padding-bottom: 2vh;
}
#orderCartTotal > div {
	display: inline-block;
	vertical-align: top;
}
#orderCartItemsTotalWrap {
	width: 45%;
}
#orderCartIPriceTotalWrap {
	width: 53%;
}
#orderCartTotal > div strong {
	font-size: 1.2vw;
}
#orderCartItemsTotal, #tofesCartPriceTotal {
	white-space: nowrap;
}
#orderCartTotalRemark {
	font-size: 1.2em;
	line-height: 2.5em;
	text-align: center;
}
#orderCartTotalRemark .withShipping {
	color: #BF2C30;
}
#orderCartTotalRemark .withoutShipping {
	color: #7A995D;
}

.orderBordered {
	border-bottom: 1px solid #bbb;
	padding-bottom: 5px;
}
.vElt {
	border-radius: 50%;
	margin-left: 20px;
	display: inline-block;
	line-height: 1;
	border: 1px solid #999;	
	padding: 4px;
	cursor: pointer;
}
.vElt i {
	visibility: hidden;
}
.vElt.active {
	background: #7A995D;
	border-color: #7A995D;
}
.vElt.active i {
	visibility: visible;
	color: white;
}
.circleElt {
	border-radius: 50%;
	border: 1px solid #999;
	width: 1em;
	height: 1em;
	padding: 2px;
	display: inline-block;
	vertical-align: bottom;
	margin-left: 1%;
	cursor: pointer;
}
.circleElt.active {
	border-color: #7A995D;
}
.circleElt.active div {
	border-radius: 50%;
	border-color: #7A995D;
	background: #7A995D;
	width: 1em;
	height: 1em;	
}

/*#orderWrap textarea::-webkit-input-placeholder, #orderWrap textarea::-webkit-input-placeholder{
	color: #999;
}
#orderWrap textarea:-moz-placeholder, #orderWrap textarea:-moz-placeholder{
	color: #999;
} 
#orderWrap textarea:-ms-input-placeholder, #orderWrap textarea:-ms-input-placeholder{
	color: #999;
} */

.orderDataTabs > div {
	display: inline-block;
	margin-left: 10px;
	white-space: nowrap;
}
.orderDataTabs > div.inactive {
	color: #999;
}

.orderDataTitle {
	font-size: 1.2em;
	font-weight: bold;
}

@media screen and (max-width: 1024px) and (min-width: 769px){ /* small desktop; ipads will be overrided by the next query */
	#orderContents .tofesCartHeader > div, #orderContents ul li > div, #orderContents ul li .tofesCartName,
	#orderBottomLinks > span, #orderCartTotal > div strong {
		font-size: 1.7vw;
	}
	#orderMain {
		height: 60vh;
	}
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#orderMain {
		height: 69vh;
	}
	.ios #orderMain {
		height: 58vh;
	}
	#orderContents ul {
		height: 59vh;
	}	
	.ios #orderContents ul {
		height: 47vh;
	}
	#orderContents .tofesCartHeader > div, #orderContents ul li > div {
		font-size: 4vw;
	}
	#orderContents ul li .tofesCartName {
		font-size: 100%;
	}
	#orderBottom {
		font-size: 1.9vh;
	}
	#orderBottomLeft {
		float: none;
		width: 100%;
		margin: 0;
	}
	#orderCartTotal {
		padding: 2%;
	}
	#orderCartTotal > div strong {
		font-size: 3vh;	
	}
	#orderCartTotalRemark {
		line-height: 3vh;
		font-size: 2.5vh;	
	}
	#orderBottomLinks {
		position: absolute;
		width: 100%;
		bottom: 1vh;
	}
	.ios #orderBottomLinks {
		bottom: 12vh;
	}
	#orderBottomLinks > span {
		font-size: 2vh;
		line-height: 1vh;
	}
	#orderNextBtn {
		margin: 0 2vw;
	}
}
@media screen and (device-width: 1024px) and (device-height: 768px) and (orientation:landscape) { /* ipads only */
	#orderContents .tofesCartHeader > div, #orderContents ul li > div, #orderContents ul li .tofesCartName,
	#orderBottomLinks > span, #orderCartTotal > div strong {
		font-size: 2.5vw;
	}
	#orderMain {
		height: 62vh;
	}
	#orderBottom {
		height: 12vh;
	}
	#orderBottomLinks {
		bottom: 2vh;
	}
}

/****************************************** order tab 1 ends******************************************/
/********************************************* order tab 2 ********************************************/
#orderTabShipping {
	height: 100%;
	overflow: scroll;
	overflow-x: hidden;
}
#orderRemarkWrap {
	float: left;
	width: 30%;
	height: 100%;
}
#orderRemarkWrap i {
	font-style: normal;
}
#orderRemark {
	margin-top: 0.5em;
	resize: none;
	border: 1px solid #bbb;
	padding:8px;
	width: 100%;
	height: 50%;
	background: transparent;
}

#orderShippingWrap {
	float: right;
	width: 65%;
	height: 60%;
}
#orderShippingWrap .profilePassword {
	display: none;
}
#orderShippingDetails {
	padding: 2% 0;
}
#orderShippingDetails ul {
	list-style-type: none;
	margin: 0;
	padding: 0;
}
#orderShippingDetails ul li {
	margin: 0.8em 0;
}

#orderTimeWrap {
	float: right;
	width: 30%;
}
#orderTime {
	padding: 2% 0;
	list-style-type: none;
	margin: 0;
}
#orderTime li {
	margin: 0.8em 0;
}
#orderTime li > span {
	color: #999;
}
#orderTime li .active {
	color: inherit;
}
#orderOnmissingWrap {
	float: right;
	width: 30%;
}
#orderOnmissing {
	padding: 2% 0;
	list-style-type: none;
	margin: 0;
}
#orderOnmissing li {
	margin: 0.8em 0;
}
#orderOnmissing li span {
	color: #999;
}
#orderOnmissing li .active {
	color: inherit;
}

@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	.orderBordered {
		padding-bottom: 0;
	}
	
	.orderDataTabs > div {
		margin-left: 0;
		margin-bottom: 3px;
	}
	#orderRemarkWrap {
		height: auto;
	}
	#orderRemarkWrap i {
		display: none;
	}
	#orderRemark {
		height: 25vh;
	}
	#orderShippingWrap {
		height: auto;
	}
	#orderTimeWrap {
		clear: both;
		float: none;
		width: 100%;
		margin: 0;
	}
	#orderTime li {
		margin: 1vh 0;
	}
	#orderOnmissingWrap {
		clear: both;
		float: none;
		width: 100%;
	}
	.ios #orderOnmissing {
		padding: 1% 0;
	}
	#orderOnmissing li {
		margin: 1vh 0;
	}
}

/****************************************** order tab 2 ends ******************************************/
/********************************************* order tab 3 ********************************************/
.orderPreviewWrap {
	float: right;
	width: 50%;	
}
.orderPreview {
	padding: 2% 0;
	list-style-type: none;
	margin: 0;
}
@media screen and (max-height: 720px) {
	.orderPreview {
		padding: 0;
	}
}
.orderPreview li {
	margin: 0.8em 0;
}
.orderPreview li.small {
	font-size: 0.9em;
	font-weight: normal;
}

#orderPaymentDetailsWrap {
	float: right;
	width: 50%;
	clear: right;
}
#orderPayment {
	padding: 2% 0;
	list-style-type: none;
	margin: 0;
}
@media screen and (max-height: 720px) {
	#orderPayment {
		padding: 0;
	}
}
#orderPayment li {
	margin: 0.8em 0;
}
#orderPayment li span {
	color: #999;
}
#orderPayment li .active {
	color: inherit;
}

#ccardPaymentDialog {
	display: none;
	position: absolute;
	width: 700px;
	height: 80vh;
	border: 2px solid #7A995D;
	-webkit-box-shadow: 3px 3px 5px -1px rgba(158,158,158,1);
	-moz-box-shadow: 3px 3px 5px -1px rgba(158,158,158,1);
	box-shadow: 3px 3px 5px -1px rgba(158,158,158,1);
	padding: 1vh 1vw;
	z-index: 7;
	background: white url(../images/sslIcon.png) no-repeat 98% 2%;
}
#ccardPaymentWrap {
	padding: 20px 20px 0;
}
#ccardPaymentWrap.loading {
	background: white url(../images/tinyLoader.gif) no-repeat center center;	
}
#ccardPayment {
	width: 370px;
	height: 410px;
	margin: 0 auto;
}
#credirCardsImg {
	display: block;
	margin: 1vh auto;
	max-width: 90%;
}
#ccardPaymentDialog h2 {
	text-align: center;
	margin-bottom: 0;
}

@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#ccardPaymentDialog {
		width: 95vw;
		height: 95vh;
	}	
	.ios #ccardPaymentDialog {
		height: 85vh;
	}
	#ccardPaymentWrap {
		padding-top: 0;
	}
	#ccardPayment {
		width: 100%;
	}
	#ccardPaymentDialog h2 {
		width: 55%;
		margin: 0 auto;
	}
	
	#orderPaymentDetailsWrap {
		float: none;
		width: 100%;
	}
}

/****************************************** order tab 3 ends ******************************************/
/*********************************************** invoice **********************************************/

#invoiceWrap.loading {
	background: white url(../images/tinyLoader.gif) no-repeat center center;	
}
#invoiceWrap.loading #invoice {
	display: none;
}
#invoice {
	padding: 5%;
	font-size: 1.25em;
}
#invoice .orderDataWrap.left {
	width: 30%;
}
#invoice .orderDataWrap.right {
	width: 60%;
}
#invoice .orderDataWrap .orderDataTabs {
	margin-bottom: 3vh;
}
#invoice .orderPreview li {
	margin-top: 0;
	margin-bottom: 1em;
}
#trackerWrap {
	margin-top: 15vh;
	line-height: 1.3em;
}
#trackerTruck {
	float: left;
}
#trackerLine {
	width: 65%;
	height: 1px;
	border-top: 1px solid #999;
	margin-top: 117px;
	z-index: 1;
}
#trackerActions {
	list-style-type: none;
	margin: -16px 0 0;
	padding: 0;
	z-index: 2;
}
#trackerActions li {
	display: inline-block;
	width: 8%;
	margin: 0 5%;
	text-align: center;
	vertical-align: top;
}
#trackerActions li:first-child {
	margin-right: 0;
}
#trackerActions li .vElt {
	background: #F2F2F2;
	margin: 0;
}
#trackerActions li .vElt.active {
	background: #7A995D;
}
#trackerActions li .trackerAction {
	display: block;
}

#invoiceReloadBtn {
	background: #7A995D;
	line-height: 2.3em;
	text-align: center;
	font-weight: bold;
	font-size: 1.4em;
	color: white;
	position: absolute;
	left: 5%;
	bottom: 5%;
	display: block;
	width: 30%;
	z-index: 1;
}

@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {	
	#trackerTruck {
		margin-top: 34px;
	}
	#trackerLine {
		width: 100%;
		height: 150px;
		border-top: medium none;
		border-right: 1px solid #999;
		margin-top: 10px;
	}	
	#trackerActions {
		list-style-type: none;
		margin: -150px -14px 0 0;
	}
	#trackerActions li {
		display: block;
		width: 100%;
		margin: 0 0 15px 0;
		text-align: right;
	}
	#trackerActions li .trackerAction {
		display: inline-block;
		margin-right: 10px;
	}
}
@media screen and (max-width: 768px) {
	#trackerWrap {
		margin-top: 10vh;
	}
	#invoice .trackerTxt br {
		display: none;
	}
	#invoice .orderDataWrap.left {
		display: none;
	}
	#invoice .orderDataWrap.right {
		float: none;
		width: 100%;
	}
	#trackerTruck {
		width: 95px;
		margin-top: 60px;
	}
	#invoiceReloadBtn {
		float: none;
		width: 90%;
	}
	.ios #invoiceReloadBtn {
		bottom: 13vh;
	}
}
@media screen and (device-width: 768px) and (device-height: 1024px) and (orientation:portrait) {	
	#invoice {
		font-size: 2em;
	}
	#invoice .trackerTxt {
		font-size: 1.2em;
	}
	#trackerWrap {
		margin-top: 21vh;
	}
	#trackerTruck {
		width: auto;
		margin-top: 34px;
	}
}
/******************************************** invoice ends ********************************************/
/*********************************************** profile ***********************************************/
#profile {
	padding: 5vw 10vw;
}
#profileDetailsWrap {
	margin-bottom: 5vh;
	padding-bottom: 5vh;
	border-bottom: 1px solid #bbb;
}
#profile strong {
	font-size: 1.2em;
	margin-bottom: 15px;
}
.profileList {
	font-size: 1.1em;
	list-style-type: none;
	margin: 0;
	padding: 0;
}
.profileList li {
	margin: 1vh 0;
}
.profileList .labelWrap {
	float: right;
	width: auto;
	padding: 2px;
	margin-left: 5px;
}
.profileList .inputWrap {
	width: auto;
	overflow: hidden;
	border-bottom: 1px solid #bbb;
}
.profileList .inputWrap input{
	width: 100%;
}
.profileList .inputWrap select {
	width: 100%;
	padding: 0 5px;
	background: transparent;
	border: medium none;
}

#profile button {
	background: #7A995D;
	padding: 10px 30px;
	border: medium none;
	font-size: 1.1em;
	font-weight: bold;
	margin: 1vh 0 1vh 15px;;
}
#profilePasswordWrap {
	margin-top: 5vh;
}
/********************************************* profile ends ********************************************/
/********************************************* notifications ********************************************/
#notifs {
	padding: 10vw;
	text-align: center;
}
#notifs strong {
	font-size: 1.2em;
	margin-bottom: 15px;
}
#notifs ul {
	font-size: 1.1em;
	list-style-type: none;
	margin: 0;
	padding: 0;
}
#notifs ul li {
	margin: 1vh 0;
}
#notifs ul li label {
	width: 55px;
	display: inline-block;
}
#notifs button {
	background: #7A995D;
	padding: 10px 30px;
	border: medium none;
	font-size: 1.1em;
	font-weight: bold;
	margin: 1vh 0 1vh 15px;;
}
/****************************************** notifications ends *****************************************/
/********************************************* feedback **********************************************/
#feedback {
	padding: 10vw;
	text-align: center;
}
#feedbackCnt {
	padding: 1% 5vh;
}
#feedback strong {
	font-size: 1.5em;
	margin-bottom: 15px;
	display: block;
}
#feedback ul {
	font-size: 1.1em;
	list-style-type: none;
	margin: 0;
	padding: 0 15vw;
}
#feedback ul li {
	margin: 1vh 0;
}
#feedback ul li label {
	width: 55px;
	display: inline-block;
}
#feedback textarea {
	resize: none;
	width: 100%;
	height: 20vh;
	background: transparent;
	border-bottom: medium none;
}
#feedback button {
	background: #7A995D;
	padding: 10px 30px;
	border: medium none;
	font-size: 1.1em;
	font-weight: bold;
	margin: 1vh 0 1vh 15vw;
	float: left;
}
#feedbackSendResult {
	font-size: 2em;
}
@media screen and (max-width: 768px),(device-width: 1024px) and (device-height: 768px) and (orientation:landscape) {
	#feedback {
		padding: 5vw;
		text-align: right;
	}
	#feedback ul {
		padding: 0;
	}
}
