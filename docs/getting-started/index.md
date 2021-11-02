
# Getting Started

Doc index.md

<h1>test html</h1>
<button id="demo" onclick="myFunction()">Click me.</button>
<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "YOU CLICKED ME!";
}
</script>



<h2>Using the XMLHttpRequest Object</h2>

<div id="demo2">
<button type="button" onclick="loadXMLDoc()">Change Content</button>
</div>

<script>
function loadXMLDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
      document.getElementById("demo").innerHTML =
      this.responseText;
    }
  };
  xhttp.open("GET", "https://www.w3schools.com/xml/xmlhttp_info.txt", true);
  xhttp.send();
}
</script>