<!doctype html>
<html lang="en">
<head>

<title>{{ page.title }}</title>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="{{ site.url }}/assets/w3.css">
<link rel="stylesheet" href="{{ site.url }}/assets/custom.css">
<link rel="stylesheet" href="{{ site.url }}/assets/font-awesome/css/font-awesome.min.css">
<script src="{{ site.url }}/assets/jquery-3.1.1.min.js"></script>
</head>

<body>

<!-- Navigation bar -->
<div>
  <div class="w3-top">
  <ul class="w3-navbar w3-white w3-wide w3-padding-8 w3-card-2">
    <li>
      <h4 class="w3-margin-left">{{ page.title }}</h4>
    </li>
    <!-- Right-sided navbar links. Hide them on small screens -->
    <li class="w3-right w3-hide-small">
      <a href="#" class="w3-left"><i class="fa fa-home" aria-hidden="true"></i></a>
      <a href="#about" class="w3-left">About us</a>
      <a href="#services" class="w3-left">Services</a>
      <a href="#specials" class="w3-left">Specials</a>
      <a href="#priceList" class="w3-left" onclick="$('#priceModal').show();">Price list</a>
      <a href="#contact" class="w3-left w3-margin-right">Contact</a>
    </li>
    </ul>
  </div>
  <div class="w3-padding-small w3-hide-small">
    <img src="{{ site.url }}/assets/images/banner_large04.png" class="w3-round" alt="main" width="100%" height="400px">
  </div>
</div>

<!-- Header -->
<header class="w3-display-container w3-content w3-wide" style="max-width:1600px;min-width:500px" id="home">
  <!-- About Section -->
 <div class="w3-row" id="header">
   <div class="w3-center w3-display-center w3-padding-small w3-opacity">
     <h1 class="w3-xxlarge">{{ page.title }}</h1>
   </div>
 </div>
 <hr>
</header>


<!-- Page content -->
{{ content }}

<!-- Footer -->
<footer class="w3-center w3-light-grey w3-padding-12">
  <p><i class="fa fa-copyright" aria-hidden="true"></i> Burnside nails and spa beauty salon - South Australia</p>
  <p>Shop 5, 384-390 Greenhill Road, Glenside, SA, 5065</p>
</footer>
  {% include {{ page.pricing }} %}

</body>

</html>
