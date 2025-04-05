# OpenWise
Project OpenWise
<h1>OpenWise test</h1>
<p>Blah blah blah</p>
<p>Blah blah blah</p>
<p>Blah blah blah</p>
<p>See Daniel?</p>
<!-- The text field -->
<input type="text" value="Hello Child" id="myInput">

<!-- The button used to copy the text -->
<button onclick="myFunction()">Copy text</button>
function myFunction() {
  // Get the text field
  var copyText = document.getElementById("myInput");

  // Select the text field
  copyText.select();
  copyText.setSelectionRange(0, 99999); // For mobile devices

   // Copy the text inside the text field
  navigator.clipboard.writeText(copyText.value);

  // Alert the copied text
  alert("Copied the text: " + copyText.value);
}
