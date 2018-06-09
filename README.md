<html>
<head><meta charset="utf-8" />
<title>Investigate_a_Dataset</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    color: #000 !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#login_widget {
  float: right;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: baseline;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
[dir="rtl"] #new-menu {
  text-align: right;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Project:-Investigate-a-Movie-Database">Project: Investigate a Movie Database<a class="anchor-link" href="#Project:-Investigate-a-Movie-Database">&#182;</a></h1><h2 id="Table-of-Contents">Table of Contents<a class="anchor-link" href="#Table-of-Contents">&#182;</a></h2><ul>
<li><a href="#intro">Introduction</a></li>
<li><a href="#wrangling">Data Wrangling</a></li>
<li><a href="#eda">Exploratory Data Analysis</a></li>
<li><a href="#conclusions">Conclusions</a></li>
</ul>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='intro'></a></p>
<h2 id="Introduction">Introduction<a class="anchor-link" href="#Introduction">&#182;</a></h2><blockquote><p>For Data Analysis, we have selected a database that contains information about movies.This database has details about the list of movies with the time and date they have released, Also name of the director,productuon company and the cast details.It also has the budget and revenue details for most of the movies.
Our Approach will start with Data Wrangling and cleaning where we will load the data and start cleaning the database to make the data more approprate for data analysing.Then we will perform data anaysis on the cleaned data and communicate the results through visualization
Below are the different factors are considered for this Analysis</p>
</blockquote>
<ol>
<li>Number of Movies released on each genre for the past 5 years </li>
<li>Analyze the budget,revenue,popularity and vote average based on the genres</li>
<li>Find the co-relation between budget and revenue, Does it have postive or negative or zero correlation ?</li>
<li>List of successful producion companies ?</li>
<li>Does runtime of the movie affects popularity?</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[51]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span> 
<span class="o">%</span><span class="k">matplotlib</span> inline
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='wrangling'></a></p>
<h2 id="Data-Wrangling:">Data Wrangling:<a class="anchor-link" href="#Data-Wrangling:">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[52]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Load your data and print out a few lines</span>
<span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;tmdb-movies.csv&#39;</span><span class="p">)</span>

<span class="c1">#Read the data</span>
<span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">2</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[52]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id</th>
      <th>imdb_id</th>
      <th>popularity</th>
      <th>budget</th>
      <th>revenue</th>
      <th>original_title</th>
      <th>cast</th>
      <th>homepage</th>
      <th>director</th>
      <th>tagline</th>
      <th>...</th>
      <th>overview</th>
      <th>runtime</th>
      <th>genres</th>
      <th>production_companies</th>
      <th>release_date</th>
      <th>vote_count</th>
      <th>vote_average</th>
      <th>release_year</th>
      <th>budget_adj</th>
      <th>revenue_adj</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>135397</td>
      <td>tt0369610</td>
      <td>32.985763</td>
      <td>150000000</td>
      <td>1513528810</td>
      <td>Jurassic World</td>
      <td>Chris Pratt|Bryce Dallas Howard|Irrfan Khan|Vi...</td>
      <td>http://www.jurassicworld.com/</td>
      <td>Colin Trevorrow</td>
      <td>The park is open.</td>
      <td>...</td>
      <td>Twenty-two years after the events of Jurassic ...</td>
      <td>124</td>
      <td>Action|Adventure|Science Fiction|Thriller</td>
      <td>Universal Studios|Amblin Entertainment|Legenda...</td>
      <td>6/9/15</td>
      <td>5562</td>
      <td>6.5</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>1.392446e+09</td>
    </tr>
    <tr>
      <th>1</th>
      <td>76341</td>
      <td>tt1392190</td>
      <td>28.419936</td>
      <td>150000000</td>
      <td>378436354</td>
      <td>Mad Max: Fury Road</td>
      <td>Tom Hardy|Charlize Theron|Hugh Keays-Byrne|Nic...</td>
      <td>http://www.madmaxmovie.com/</td>
      <td>George Miller</td>
      <td>What a Lovely Day.</td>
      <td>...</td>
      <td>An apocalyptic story set in the furthest reach...</td>
      <td>120</td>
      <td>Action|Adventure|Science Fiction|Thriller</td>
      <td>Village Roadshow Pictures|Kennedy Miller Produ...</td>
      <td>5/13/15</td>
      <td>6185</td>
      <td>7.1</td>
      <td>2015</td>
      <td>1.379999e+08</td>
      <td>3.481613e+08</td>
    </tr>
  </tbody>
</table>
<p>2 rows × 21 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Data-Cleaning:">Data Cleaning:<a class="anchor-link" href="#Data-Cleaning:">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#change the datatype of genre from float to string</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">astype</span><span class="p">(</span><span class="nb">str</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Considering only the first genre as the genre of the film</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;genres&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">x</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;|&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">])</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#dropping the rows which has no genre listed.</span>
<span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">df</span><span class="o">.</span><span class="n">query</span><span class="p">(</span><span class="s1">&#39;genres == &quot;nan&quot;&#39;</span><span class="p">)</span><span class="o">.</span><span class="n">index</span><span class="p">,</span><span class="n">axis</span><span class="o">=</span><span class="mi">0</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#confirm changes</span>
<span class="n">df</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>&lt;class &#39;pandas.core.frame.DataFrame&#39;&gt;
Int64Index: 10843 entries, 0 to 10865
Data columns (total 21 columns):
id                      10843 non-null int64
imdb_id                 10835 non-null object
popularity              10843 non-null float64
budget                  10843 non-null int64
revenue                 10843 non-null int64
original_title          10843 non-null object
cast                    10768 non-null object
homepage                2931 non-null object
director                10801 non-null object
tagline                 8037 non-null object
keywords                9368 non-null object
overview                10840 non-null object
runtime                 10843 non-null int64
genres                  10843 non-null object
production_companies    9827 non-null object
release_date            10843 non-null object
vote_count              10843 non-null int64
vote_average            10843 non-null float64
release_year            10843 non-null int64
budget_adj              10843 non-null float64
revenue_adj             10843 non-null float64
dtypes: float64(4), int64(6), object(11)
memory usage: 1.8+ MB
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#dropping few unwanted columns</span>
<span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">&#39;tagline&#39;</span><span class="p">,</span><span class="s1">&#39;imdb_id&#39;</span><span class="p">,</span><span class="s1">&#39;homepage&#39;</span><span class="p">,</span><span class="s1">&#39;keywords&#39;</span><span class="p">,</span><span class="s1">&#39;overview&#39;</span><span class="p">,</span><span class="s1">&#39;director&#39;</span><span class="p">,</span><span class="s1">&#39;production_companies&#39;</span><span class="p">],</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#confirm changes</span>
<span class="n">df</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>&lt;class &#39;pandas.core.frame.DataFrame&#39;&gt;
Int64Index: 10843 entries, 0 to 10865
Data columns (total 14 columns):
id                10843 non-null int64
popularity        10843 non-null float64
budget            10843 non-null int64
revenue           10843 non-null int64
original_title    10843 non-null object
cast              10768 non-null object
runtime           10843 non-null int64
genres            10843 non-null object
release_date      10843 non-null object
vote_count        10843 non-null int64
vote_average      10843 non-null float64
release_year      10843 non-null int64
budget_adj        10843 non-null float64
revenue_adj       10843 non-null float64
dtypes: float64(4), int64(6), object(4)
memory usage: 1.2+ MB
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='eda'></a></p>
<h2 id="Exploratory-Data-Analysis">Exploratory Data Analysis<a class="anchor-link" href="#Exploratory-Data-Analysis">&#182;</a></h2><h3 id="1.-Number-of-Movies-released-on-each-genre-for-the-past-5-years">1. Number of Movies released on each genre for the past 5 years<a class="anchor-link" href="#1.-Number-of-Movies-released-on-each-genre-for-the-past-5-years">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#1 Number of Movies released on each genre for the past 5 years</span>

<span class="n">df_5</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;release_year&#39;</span><span class="p">]</span> <span class="o">&gt;</span> <span class="mi">2010</span><span class="p">]</span>
<span class="n">gen_ct</span> <span class="o">=</span> <span class="n">df_5</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;genres&#39;</span><span class="p">])[</span><span class="s1">&#39;id&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">count</span><span class="p">()</span>


<span class="n">Action</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Action&#39;</span><span class="p">]</span>
<span class="n">Adventure</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Adventure&#39;</span><span class="p">]</span>
<span class="n">Animation</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Animation&#39;</span><span class="p">]</span>
<span class="n">Comedy</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Comedy&#39;</span><span class="p">]</span>
<span class="n">Crime</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Crime&#39;</span><span class="p">]</span>
<span class="n">Documentary</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Documentary&#39;</span><span class="p">]</span>
<span class="n">Drama</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Drama&#39;</span><span class="p">]</span>
<span class="n">Family</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Family&#39;</span><span class="p">]</span>
<span class="n">Fantasy</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Fantasy&#39;</span><span class="p">]</span>
<span class="n">Foreign</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Foreign&#39;</span><span class="p">]</span>
<span class="n">History</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;History&#39;</span><span class="p">]</span>
<span class="n">Horror</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Horror&#39;</span><span class="p">]</span>
<span class="n">Music</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Music&#39;</span><span class="p">]</span>
<span class="n">Mystery</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Mystery&#39;</span><span class="p">]</span>
<span class="n">Romance</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Romance&#39;</span><span class="p">]</span>
<span class="n">Science_Fiction</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Science Fiction&#39;</span><span class="p">]</span>
<span class="n">TV_Movie</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;TV Movie&#39;</span><span class="p">]</span>
<span class="n">Thriller</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Thriller&#39;</span><span class="p">]</span>
<span class="n">War</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;War&#39;</span><span class="p">]</span>
<span class="n">Western</span> <span class="o">=</span> <span class="n">gen_ct</span><span class="p">[</span><span class="s1">&#39;Western&#39;</span><span class="p">]</span>

<span class="c1">#Visualization</span>

<span class="n">N</span><span class="o">=</span><span class="mi">19</span>
<span class="n">locations</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">N</span><span class="p">)</span>
<span class="n">gens</span> <span class="o">=</span> <span class="p">[</span><span class="n">Action</span><span class="p">,</span><span class="n">Adventure</span><span class="p">,</span><span class="n">Comedy</span><span class="p">,</span><span class="n">Crime</span><span class="p">,</span><span class="n">Documentary</span><span class="p">,</span><span class="n">Drama</span><span class="p">,</span><span class="n">Family</span><span class="p">,</span><span class="n">Fantasy</span><span class="p">,</span><span class="n">Foreign</span><span class="p">,</span><span class="n">History</span><span class="p">,</span><span class="n">Horror</span><span class="p">,</span><span class="n">Music</span><span class="p">,</span><span class="n">Mystery</span><span class="p">,</span><span class="n">Romance</span><span class="p">,</span><span class="n">Science_Fiction</span><span class="p">,</span><span class="n">TV_Movie</span><span class="p">,</span><span class="n">Thriller</span><span class="p">,</span><span class="n">War</span><span class="p">,</span><span class="n">Western</span><span class="p">]</span>
<span class="n">labels</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Action&#39;</span><span class="p">,</span><span class="s1">&#39;Adventure&#39;</span><span class="p">,</span><span class="s1">&#39;Comedy&#39;</span><span class="p">,</span><span class="s1">&#39;Crime&#39;</span><span class="p">,</span><span class="s1">&#39;Documentary&#39;</span><span class="p">,</span><span class="s1">&#39;Drama&#39;</span><span class="p">,</span><span class="s1">&#39;Family&#39;</span><span class="p">,</span><span class="s1">&#39;Fantasy&#39;</span><span class="p">,</span><span class="s1">&#39;Foreign&#39;</span><span class="p">,</span><span class="s1">&#39;History&#39;</span><span class="p">,</span><span class="s1">&#39;Horror&#39;</span><span class="p">,</span><span class="s1">&#39;Music&#39;</span><span class="p">,</span><span class="s1">&#39;Mystery&#39;</span><span class="p">,</span><span class="s1">&#39;Romance&#39;</span><span class="p">,</span><span class="s1">&#39;Science_Fiction&#39;</span><span class="p">,</span><span class="s1">&#39;TV_Movie&#39;</span><span class="p">,</span><span class="s1">&#39;Thriller&#39;</span><span class="p">,</span><span class="s1">&#39;War&#39;</span><span class="p">,</span><span class="s1">&#39;Western&#39;</span><span class="p">]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">locations</span><span class="p">,</span><span class="n">gens</span><span class="p">,</span><span class="n">tick_label</span><span class="o">=</span><span class="n">labels</span><span class="p">),</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">locations</span><span class="p">,</span><span class="n">rotation</span><span class="o">=</span><span class="mi">90</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;No.of Movies by genres&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;genres&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;No.of Movies&#39;</span><span class="p">)</span>


<span class="c1">#COMMUNICATION - In the Last 5 years, Drama genre tops the list with more number of movies followed by comedy genre.</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[9]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0,0.5,&#39;No.of Movies&#39;)</pre>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[32]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[32]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id</th>
      <th>popularity</th>
      <th>budget</th>
      <th>revenue</th>
      <th>runtime</th>
      <th>vote_count</th>
      <th>vote_average</th>
      <th>release_year</th>
      <th>budget_adj</th>
      <th>revenue_adj</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>10843.000000</td>
      <td>10843.000000</td>
      <td>1.084300e+04</td>
      <td>1.084300e+04</td>
      <td>10843.000000</td>
      <td>10843.000000</td>
      <td>10843.000000</td>
      <td>10843.000000</td>
      <td>1.084300e+04</td>
      <td>1.084300e+04</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>65868.491930</td>
      <td>0.647456</td>
      <td>1.465672e+07</td>
      <td>3.990779e+07</td>
      <td>102.137508</td>
      <td>217.813705</td>
      <td>5.973974</td>
      <td>2001.315595</td>
      <td>1.758827e+07</td>
      <td>5.147332e+07</td>
    </tr>
    <tr>
      <th>std</th>
      <td>91977.394803</td>
      <td>1.000986</td>
      <td>3.093864e+07</td>
      <td>1.171131e+08</td>
      <td>31.293320</td>
      <td>576.155351</td>
      <td>0.934260</td>
      <td>12.813298</td>
      <td>3.433299e+07</td>
      <td>1.447664e+08</td>
    </tr>
    <tr>
      <th>min</th>
      <td>5.000000</td>
      <td>0.000065</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
      <td>0.000000</td>
      <td>10.000000</td>
      <td>1.500000</td>
      <td>1960.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>10589.500000</td>
      <td>0.208253</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
      <td>90.000000</td>
      <td>17.000000</td>
      <td>5.400000</td>
      <td>1995.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>20558.000000</td>
      <td>0.384555</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
      <td>99.000000</td>
      <td>38.000000</td>
      <td>6.000000</td>
      <td>2006.000000</td>
      <td>0.000000e+00</td>
      <td>0.000000e+00</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>75182.000000</td>
      <td>0.715349</td>
      <td>1.500000e+07</td>
      <td>2.413675e+07</td>
      <td>111.000000</td>
      <td>146.000000</td>
      <td>6.600000</td>
      <td>2011.000000</td>
      <td>2.093530e+07</td>
      <td>3.387655e+07</td>
    </tr>
    <tr>
      <th>max</th>
      <td>417859.000000</td>
      <td>32.985763</td>
      <td>4.250000e+08</td>
      <td>2.781506e+09</td>
      <td>900.000000</td>
      <td>9767.000000</td>
      <td>9.200000</td>
      <td>2015.000000</td>
      <td>4.250000e+08</td>
      <td>2.827124e+09</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="2.-Genre-vs-Revenue_adj">2. Genre vs Revenue_adj<a class="anchor-link" href="#2.-Genre-vs-Revenue_adj">&#182;</a></h3><h3 id="3.-Genre-vs-Budjet_adj">3. Genre vs Budjet_adj<a class="anchor-link" href="#3.-Genre-vs-Budjet_adj">&#182;</a></h3><h3 id="4.-Genre-vs-Popularity">4. Genre vs Popularity<a class="anchor-link" href="#4.-Genre-vs-Popularity">&#182;</a></h3><h3 id="5.-Genre-vs-Vote_Avg">5. Genre vs Vote_Avg<a class="anchor-link" href="#5.-Genre-vs-Vote_Avg">&#182;</a></h3><h3 id="6.-Co-relation-between-Budjet_adj-and-Revenue_adj">6. Co-relation between Budjet_adj and Revenue_adj<a class="anchor-link" href="#6.-Co-relation-between-Budjet_adj-and-Revenue_adj">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[27]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#2 - Genre Vs Revenue_adj</span>

<span class="n">df_r</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;genres&#39;</span><span class="p">])[</span><span class="s1">&#39;revenue_adj&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>

<span class="n">Action</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Action&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Adventure</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Adventure&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Animation</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Animation&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Comedy</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Comedy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Crime</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Crime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Documentary</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Documentary&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Drama</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Drama&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Family</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Family&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Fantasy</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Fantasy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="c1">#Foreign = df_r[&#39;Foreign&#39;].round()</span>
<span class="n">History</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;History&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Horror</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Horror&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Music</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Music&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Mystery</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Mystery&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Romance</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Romance&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Science_Fiction</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Science Fiction&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">TV_Movie</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;TV Movie&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Thriller</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Thriller&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">War</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;War&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Western</span> <span class="o">=</span> <span class="n">df_r</span><span class="p">[</span><span class="s1">&#39;Western&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>

<span class="c1">#Visualization</span>

<span class="n">N</span><span class="o">=</span><span class="mi">18</span>
<span class="n">locations</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">N</span><span class="p">)</span>
<span class="n">gens</span> <span class="o">=</span> <span class="p">[</span><span class="n">Action</span><span class="p">,</span><span class="n">Adventure</span><span class="p">,</span><span class="n">Comedy</span><span class="p">,</span><span class="n">Crime</span><span class="p">,</span><span class="n">Documentary</span><span class="p">,</span><span class="n">Drama</span><span class="p">,</span><span class="n">Family</span><span class="p">,</span><span class="n">Fantasy</span><span class="p">,</span><span class="n">History</span><span class="p">,</span><span class="n">Horror</span><span class="p">,</span><span class="n">Music</span><span class="p">,</span><span class="n">Mystery</span><span class="p">,</span><span class="n">Romance</span><span class="p">,</span><span class="n">Science_Fiction</span><span class="p">,</span><span class="n">TV_Movie</span><span class="p">,</span><span class="n">Thriller</span><span class="p">,</span><span class="n">War</span><span class="p">,</span><span class="n">Western</span><span class="p">]</span>
<span class="n">labels</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Action&#39;</span><span class="p">,</span><span class="s1">&#39;Adventure&#39;</span><span class="p">,</span><span class="s1">&#39;Comedy&#39;</span><span class="p">,</span><span class="s1">&#39;Crime&#39;</span><span class="p">,</span><span class="s1">&#39;Documentary&#39;</span><span class="p">,</span><span class="s1">&#39;Drama&#39;</span><span class="p">,</span><span class="s1">&#39;Family&#39;</span><span class="p">,</span><span class="s1">&#39;Fantasy&#39;</span><span class="p">,</span><span class="s1">&#39;History&#39;</span><span class="p">,</span><span class="s1">&#39;Horror&#39;</span><span class="p">,</span><span class="s1">&#39;Music&#39;</span><span class="p">,</span><span class="s1">&#39;Mystery&#39;</span><span class="p">,</span><span class="s1">&#39;Romance&#39;</span><span class="p">,</span><span class="s1">&#39;Science_Fiction&#39;</span><span class="p">,</span><span class="s1">&#39;TV_Movie&#39;</span><span class="p">,</span><span class="s1">&#39;Thriller&#39;</span><span class="p">,</span><span class="s1">&#39;War&#39;</span><span class="p">,</span><span class="s1">&#39;Western&#39;</span><span class="p">]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">locations</span><span class="p">,</span><span class="n">gens</span><span class="p">,</span><span class="n">tick_label</span><span class="o">=</span><span class="n">labels</span><span class="p">),</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">locations</span><span class="p">,</span><span class="n">rotation</span><span class="o">=</span><span class="mi">90</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Genre Vs Revenue_adj&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Genres&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Revenue_adj&#39;</span><span class="p">)</span>


<span class="c1"># COMMUNICATION - Adventure movies produced more revenue when compared to all other genres, Also science_fiction movies</span>
<span class="c1"># as well produced good amount of revenue.</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[27]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0,0.5,&#39;Revenue_adj&#39;)</pre>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[28]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#3 - Genre Vs Budjet_adj</span>

<span class="n">df_b</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;genres&#39;</span><span class="p">])[</span><span class="s1">&#39;budget_adj&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span> 

<span class="n">Action</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Action&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Adventure</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Adventure&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Animation</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Animation&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Comedy</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Comedy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Crime</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Crime&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Documentary</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Documentary&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Drama</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Drama&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Family</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Family&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Fantasy</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Fantasy&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="c1">#Foreign = df_b[&#39;Foreign&#39;].round()</span>
<span class="n">History</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;History&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Horror</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Horror&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Music</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Music&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Mystery</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Mystery&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Romance</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Romance&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Science_Fiction</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Science Fiction&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">TV_Movie</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;TV Movie&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Thriller</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Thriller&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">War</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;War&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>
<span class="n">Western</span> <span class="o">=</span> <span class="n">df_b</span><span class="p">[</span><span class="s1">&#39;Western&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">round</span><span class="p">()</span>

<span class="c1">#Visualization</span>

<span class="n">N</span><span class="o">=</span><span class="mi">18</span>
<span class="n">locations</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">N</span><span class="p">)</span>
<span class="n">gens</span> <span class="o">=</span> <span class="p">[</span><span class="n">Action</span><span class="p">,</span><span class="n">Adventure</span><span class="p">,</span><span class="n">Comedy</span><span class="p">,</span><span class="n">Crime</span><span class="p">,</span><span class="n">Documentary</span><span class="p">,</span><span class="n">Drama</span><span class="p">,</span><span class="n">Family</span><span class="p">,</span><span class="n">Fantasy</span><span class="p">,</span><span class="n">History</span><span class="p">,</span><span class="n">Horror</span><span class="p">,</span><span class="n">Music</span><span class="p">,</span><span class="n">Mystery</span><span class="p">,</span><span class="n">Romance</span><span class="p">,</span><span class="n">Science_Fiction</span><span class="p">,</span><span class="n">TV_Movie</span><span class="p">,</span><span class="n">Thriller</span><span class="p">,</span><span class="n">War</span><span class="p">,</span><span class="n">Western</span><span class="p">]</span>
<span class="n">labels</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Action&#39;</span><span class="p">,</span><span class="s1">&#39;Adventure&#39;</span><span class="p">,</span><span class="s1">&#39;Comedy&#39;</span><span class="p">,</span><span class="s1">&#39;Crime&#39;</span><span class="p">,</span><span class="s1">&#39;Documentary&#39;</span><span class="p">,</span><span class="s1">&#39;Drama&#39;</span><span class="p">,</span><span class="s1">&#39;Family&#39;</span><span class="p">,</span><span class="s1">&#39;Fantasy&#39;</span><span class="p">,</span><span class="s1">&#39;History&#39;</span><span class="p">,</span><span class="s1">&#39;Horror&#39;</span><span class="p">,</span><span class="s1">&#39;Music&#39;</span><span class="p">,</span><span class="s1">&#39;Mystery&#39;</span><span class="p">,</span><span class="s1">&#39;Romance&#39;</span><span class="p">,</span><span class="s1">&#39;Science_Fiction&#39;</span><span class="p">,</span><span class="s1">&#39;TV_Movie&#39;</span><span class="p">,</span><span class="s1">&#39;Thriller&#39;</span><span class="p">,</span><span class="s1">&#39;War&#39;</span><span class="p">,</span><span class="s1">&#39;Western&#39;</span><span class="p">]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">locations</span><span class="p">,</span><span class="n">gens</span><span class="p">,</span><span class="n">tick_label</span><span class="o">=</span><span class="n">labels</span><span class="p">),</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">locations</span><span class="p">,</span><span class="n">rotation</span><span class="o">=</span><span class="mi">90</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Genre Vs Budget_adj&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Genres&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Budget_adj&#39;</span><span class="p">)</span>


<span class="c1"># COMMUNICATION - Adventure genre movies are made with huge budget than any other genres </span>
<span class="c1"># also they are producing more revenue. Suprisingly Action movies are made with more budjet but producing less revenue.</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[28]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0,0.5,&#39;Budget_adj&#39;)</pre>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[30]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#4 - Genre Vs Popularity</span>

<span class="n">df_p</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;genres&#39;</span><span class="p">])[</span><span class="s1">&#39;popularity&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span> 

<span class="n">Action</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Action&#39;</span><span class="p">]</span>
<span class="n">Adventure</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Adventure&#39;</span><span class="p">]</span>
<span class="n">Animation</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Animation&#39;</span><span class="p">]</span>
<span class="n">Comedy</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Comedy&#39;</span><span class="p">]</span>
<span class="n">Crime</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Crime&#39;</span><span class="p">]</span>
<span class="n">Documentary</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Documentary&#39;</span><span class="p">]</span>
<span class="n">Drama</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Drama&#39;</span><span class="p">]</span>
<span class="n">Family</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Family&#39;</span><span class="p">]</span>
<span class="n">Fantasy</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Fantasy&#39;</span><span class="p">]</span>
<span class="c1">#Foreign = df_b[&#39;Foreign&#39;].round()</span>
<span class="n">History</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;History&#39;</span><span class="p">]</span>
<span class="n">Horror</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Horror&#39;</span><span class="p">]</span>
<span class="n">Music</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Music&#39;</span><span class="p">]</span>
<span class="n">Mystery</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Mystery&#39;</span><span class="p">]</span>
<span class="n">Romance</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Romance&#39;</span><span class="p">]</span>
<span class="n">Science_Fiction</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Science Fiction&#39;</span><span class="p">]</span>
<span class="n">TV_Movie</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;TV Movie&#39;</span><span class="p">]</span>
<span class="n">Thriller</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Thriller&#39;</span><span class="p">]</span>
<span class="n">War</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;War&#39;</span><span class="p">]</span>
<span class="n">Western</span> <span class="o">=</span> <span class="n">df_p</span><span class="p">[</span><span class="s1">&#39;Western&#39;</span><span class="p">]</span>

<span class="c1">#Visualization</span>

<span class="n">N</span><span class="o">=</span><span class="mi">18</span>
<span class="n">locations</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">N</span><span class="p">)</span>
<span class="n">gens</span> <span class="o">=</span> <span class="p">[</span><span class="n">Action</span><span class="p">,</span><span class="n">Adventure</span><span class="p">,</span><span class="n">Comedy</span><span class="p">,</span><span class="n">Crime</span><span class="p">,</span><span class="n">Documentary</span><span class="p">,</span><span class="n">Drama</span><span class="p">,</span><span class="n">Family</span><span class="p">,</span><span class="n">Fantasy</span><span class="p">,</span><span class="n">History</span><span class="p">,</span><span class="n">Horror</span><span class="p">,</span><span class="n">Music</span><span class="p">,</span><span class="n">Mystery</span><span class="p">,</span><span class="n">Romance</span><span class="p">,</span><span class="n">Science_Fiction</span><span class="p">,</span><span class="n">TV_Movie</span><span class="p">,</span><span class="n">Thriller</span><span class="p">,</span><span class="n">War</span><span class="p">,</span><span class="n">Western</span><span class="p">]</span>
<span class="n">labels</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Action&#39;</span><span class="p">,</span><span class="s1">&#39;Adventure&#39;</span><span class="p">,</span><span class="s1">&#39;Comedy&#39;</span><span class="p">,</span><span class="s1">&#39;Crime&#39;</span><span class="p">,</span><span class="s1">&#39;Documentary&#39;</span><span class="p">,</span><span class="s1">&#39;Drama&#39;</span><span class="p">,</span><span class="s1">&#39;Family&#39;</span><span class="p">,</span><span class="s1">&#39;Fantasy&#39;</span><span class="p">,</span><span class="s1">&#39;History&#39;</span><span class="p">,</span><span class="s1">&#39;Horror&#39;</span><span class="p">,</span><span class="s1">&#39;Music&#39;</span><span class="p">,</span><span class="s1">&#39;Mystery&#39;</span><span class="p">,</span><span class="s1">&#39;Romance&#39;</span><span class="p">,</span><span class="s1">&#39;Science_Fiction&#39;</span><span class="p">,</span><span class="s1">&#39;TV_Movie&#39;</span><span class="p">,</span><span class="s1">&#39;Thriller&#39;</span><span class="p">,</span><span class="s1">&#39;War&#39;</span><span class="p">,</span><span class="s1">&#39;Western&#39;</span><span class="p">]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">locations</span><span class="p">,</span><span class="n">gens</span><span class="p">,</span><span class="n">tick_label</span><span class="o">=</span><span class="n">labels</span><span class="p">),</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">locations</span><span class="p">,</span><span class="n">rotation</span><span class="o">=</span><span class="mi">90</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Genre Vs Popularity&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Genres&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Popularity&#39;</span><span class="p">)</span>


<span class="c1">#Communication - Adventure and Science Fiction are more popular among the people and Documentry gets least poplularity.</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[30]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0,0.5,&#39;Popularity&#39;)</pre>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[49]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#5 Genre vs Vote_Avg</span>

<span class="n">df_v</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;genres&#39;</span><span class="p">])[</span><span class="s1">&#39;vote_average&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span> 


<span class="n">Action</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Action&#39;</span><span class="p">]</span>
<span class="n">Adventure</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Adventure&#39;</span><span class="p">]</span>
<span class="n">Animation</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Animation&#39;</span><span class="p">]</span>
<span class="n">Comedy</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Comedy&#39;</span><span class="p">]</span>
<span class="n">Crime</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Crime&#39;</span><span class="p">]</span>
<span class="n">Documentary</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Documentary&#39;</span><span class="p">]</span>
<span class="n">Drama</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Drama&#39;</span><span class="p">]</span>
<span class="n">Family</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Family&#39;</span><span class="p">]</span>
<span class="n">Fantasy</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Fantasy&#39;</span><span class="p">]</span>
<span class="c1">#Foreign = df_b[&#39;Foreign&#39;].round()</span>
<span class="n">History</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;History&#39;</span><span class="p">]</span>
<span class="n">Horror</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Horror&#39;</span><span class="p">]</span>
<span class="n">Music</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Music&#39;</span><span class="p">]</span>
<span class="n">Mystery</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Mystery&#39;</span><span class="p">]</span>
<span class="n">Romance</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Romance&#39;</span><span class="p">]</span>
<span class="n">Science_Fiction</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Science Fiction&#39;</span><span class="p">]</span>
<span class="n">TV_Movie</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;TV Movie&#39;</span><span class="p">]</span>
<span class="n">Thriller</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Thriller&#39;</span><span class="p">]</span>
<span class="n">War</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;War&#39;</span><span class="p">]</span>
<span class="n">Western</span> <span class="o">=</span> <span class="n">df_v</span><span class="p">[</span><span class="s1">&#39;Western&#39;</span><span class="p">]</span>

<span class="c1">#Visualization</span>

<span class="n">N</span><span class="o">=</span><span class="mi">18</span>
<span class="n">locations</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">N</span><span class="p">)</span>
<span class="n">gens</span> <span class="o">=</span> <span class="p">[</span><span class="n">Action</span><span class="p">,</span><span class="n">Adventure</span><span class="p">,</span><span class="n">Comedy</span><span class="p">,</span><span class="n">Crime</span><span class="p">,</span><span class="n">Documentary</span><span class="p">,</span><span class="n">Drama</span><span class="p">,</span><span class="n">Family</span><span class="p">,</span><span class="n">Fantasy</span><span class="p">,</span><span class="n">History</span><span class="p">,</span><span class="n">Horror</span><span class="p">,</span><span class="n">Music</span><span class="p">,</span><span class="n">Mystery</span><span class="p">,</span><span class="n">Romance</span><span class="p">,</span><span class="n">Science_Fiction</span><span class="p">,</span><span class="n">TV_Movie</span><span class="p">,</span><span class="n">Thriller</span><span class="p">,</span><span class="n">War</span><span class="p">,</span><span class="n">Western</span><span class="p">]</span>
<span class="n">labels</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Action&#39;</span><span class="p">,</span><span class="s1">&#39;Adventure&#39;</span><span class="p">,</span><span class="s1">&#39;Comedy&#39;</span><span class="p">,</span><span class="s1">&#39;Crime&#39;</span><span class="p">,</span><span class="s1">&#39;Documentary&#39;</span><span class="p">,</span><span class="s1">&#39;Drama&#39;</span><span class="p">,</span><span class="s1">&#39;Family&#39;</span><span class="p">,</span><span class="s1">&#39;Fantasy&#39;</span><span class="p">,</span><span class="s1">&#39;History&#39;</span><span class="p">,</span><span class="s1">&#39;Horror&#39;</span><span class="p">,</span><span class="s1">&#39;Music&#39;</span><span class="p">,</span><span class="s1">&#39;Mystery&#39;</span><span class="p">,</span><span class="s1">&#39;Romance&#39;</span><span class="p">,</span><span class="s1">&#39;Science_Fiction&#39;</span><span class="p">,</span><span class="s1">&#39;TV_Movie&#39;</span><span class="p">,</span><span class="s1">&#39;Thriller&#39;</span><span class="p">,</span><span class="s1">&#39;War&#39;</span><span class="p">,</span><span class="s1">&#39;Western&#39;</span><span class="p">]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">locations</span><span class="p">,</span><span class="n">gens</span><span class="p">,</span><span class="n">tick_label</span><span class="o">=</span><span class="n">labels</span><span class="p">),</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">locations</span><span class="p">,</span><span class="n">rotation</span><span class="o">=</span><span class="mi">90</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Genre Vs vote_average&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Genres&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;vote_average&#39;</span><span class="p">)</span>

<span class="c1">#Communication: Documentry tops the list with highest voting Average than any other genres.</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[49]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0,0.5,&#39;vote_average&#39;)</pre>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[50]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#6 Budjet_adj vs Revenue_adj</span>

<span class="n">df_r</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;genres&#39;</span><span class="p">])[</span><span class="s1">&#39;revenue_adj&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="n">df_b</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">([</span><span class="s1">&#39;genres&#39;</span><span class="p">])[</span><span class="s1">&#39;budget_adj&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>



<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">df_r</span><span class="p">,</span><span class="n">df_b</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Budget_adj Vs Revenue_adj&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Revenue_adj&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Budget_adj&#39;</span><span class="p">)</span>


<span class="c1">#Communication: Budget and Revenue shows a good postive co-relation.</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[50]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0,0.5,&#39;Budget_adj&#39;)</pre>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Conclusions:</span>
 <span class="c1"># Able to analyze the movie dataset by considering genre as a main factor.</span>
 <span class="c1"># Able to predict which could be possibly be the genre that people like or dislike most     </span>
 <span class="c1"># Able to predict the relation between budget and revenue factors</span>
 <span class="c1"># we can further investigate this dataset by taking other factors like production companies,cast list,runtime etc.</span>

    
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[53]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">subprocess</span> <span class="k">import</span> <span class="n">call</span>
<span class="n">call</span><span class="p">([</span><span class="s1">&#39;python&#39;</span><span class="p">,</span> <span class="s1">&#39;-m&#39;</span><span class="p">,</span> <span class="s1">&#39;nbconvert&#39;</span><span class="p">,</span> <span class="s1">&#39;Investigate_a_Dataset.ipynb&#39;</span><span class="p">])</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[53]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0</pre>
</div>

</div>

</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>

