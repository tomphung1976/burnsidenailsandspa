---
layout: master
title: Burnside Nails and Spa Beauty Salon
services: services.md
pricing: price.md
---
<!-- Page content -->
<div class="w3-content" style="max-width:1100px">

  <!-- About Section -->
  <div class="w3-row" id="about">
    <div class="w3-col l6">
      <div class="w3-col m6">
      <img src="/assets/images/aboutus01.png" class="w3-round w3-image w3-right" alt="about us" width="200" height="200">
      </div>
      <div class="w3-col m6">
      <img src="/assets/images/aboutus03.png" class="w3-round w3-image" alt="about us" width="200" height="200">
      </div>
      <div class="w3-col m6">
      <img src="/assets/images/aboutus04.png" class="w3-round w3-image w3-right" alt="about us" width="200" height="200">
      </div>
      <div class="w3-col m6">
      <img src="/assets/images/aboutus02.png" class="w3-round w3-image" alt="about us" width="200" height="200">
      </div>
    </div>
    <div class="w3-col l1" style="padding-left:10px;" >
    <div class="vertical-text">
      <h2>ABOUT US</h2>
    </div>
    </div>
    <div class="w3-col l5">
    <span style="font-size:20px; text-align:justify">
    Our spa treatments are designed for specific needs on your hands and feet. We are eco-friendly and health-conscious salon. Every single element inside Nail Service has been carefully tested for glowing result before bringing to you. Our goal is to provide the healthiest and longest lasting result at affordable price. We have gone as far as using certified organic ingredients for our lotion and scrubs. Natural ingredients of herbs, citruses and essential oils are commonly used in our salon. All services are attentive and include thorough massage.
    </span>
    </div>
  </div>

  <hr>
  <!-- Services -->
  {% include {{ page.services }} %}
  <hr>

  <!-- Price -->
  <div class="w3-row w3-padding-32" id="priceList">
    <div class="w3-center w3-padding-large">
        <h4> Best Deals </h4>
        <h1 style="font-size:50px; color:#5d5b5b;">Special Pricing</h1>
        <img src="/assets/images/breakline01.png" class="w3-round w3-image" width="500" height="70%">
    </div>
    <div class="w3-row price border dropShadow">
          {% for g in site.data.price.groups %}
          {% if g.description == "Shellac" or g.description == "Manicure & Pedicure" %}
          <div class="w3-half">
            <h2>{{g.description}}</h2> {% for title in g.subTitles %}
            <h6>{{title.name}}</h6> {% endfor %}
            <ul>
                <!--each item-->
                {% for item in g.items %} {% assign price = {{item.price}}|lstrip %}
                <li class="w3-padding-large">{{item.name}} <span class="w3-right priceTag">{% if price != '' %}  {{price}} {% endif %} </span>
                <br>
                <span style="font-size:18px;">{{item.description}}</span>
                </li>
                {% endfor %}
            </ul>
          </div>
          {% endif %}
          {% endfor %}
          <div class="w3-center w3-padding-xlarge">      
            <h4>... and More</h4>
            <a href="#priceList" class="w3-btn-floating-large w3-teal" onclick="$('#priceModal').show();">+</a>      
          </div>  
    </div>

  </div>
  <hr>

  <!-- specials -->
  <div class="w3-row w3-padding-32" id="specials">
    <div class="w3-col w3-right  w3-padding-large">
      <h2 class="w3-right">Packages & Specials </h2>
    </div>
    <div class="w3-col l6">
    <img src="/assets/images/specials04.png" class="w3-round w3-image" alt="Menu" width="600" height="500">
   </div>

   <div class="w3-col l6">
    <!-- Specials deals-->
    <div class="w3-row w3-center dropShadow" height="500">
      <div class="w3-col m6 w3-padding-large specialItems borderRight">
      <h4>Special 1</h4>
      </div>
      <div class="w3-col m6  w3-padding-large specialItems">
        <h4>Special 1</h4>
      </div>
      <div class="w3-col m6  w3-padding-large specialItems borderRight">
      <h4>Special 1</h4>
      </div>
      <div class="w3-col m6  w3-padding-large specialItems">
        <h4>Special 1</h4>
      </div>
    </div>

   </div>

  </div>

   <hr style="font-weight:bold">
   <!--Reviews-->
   <div class="w3-row w3-padding-32" id="reviews">
   <div class="w3-col l12">
    <h1 class="w3-center">Feature in CliqueMag</h1><br>
   <img src="/assets/images/clique.png" class="w3-round w3-image" alt="Menu" width="auto" height="750">
   </div>
    <div class="w3-col l12">
	 <h1 class="w3-center">Reviews</h1><br>
    <img src="/assets/images/yelp.png" class="w3-round w3-image w3-right dropShadow" alt="Menu" width="auto" height="750">
   </div>

  </div>

  <hr>

  <!-- Contact Section -->
  <div class="w3-container w3-padding-32" id="contact">
  <div class="w3-col l6 w3-padding-large">
   <h1 class="w3-center">Contact us</h1><br>  
	<ul class="w3-ul w3-card-4">
    <li><h4>OPENING HOURS</h4></li>            
            <li>
            Monday - Friday: 9am - 5:30pm <br>
            Thursday: 9am - 9pm <br>
            Saturday: 9am - 5pm <br>
            Sunday : 11am - 9pm
            </li>            
            <li>Shop 5, 384-390 Greenhill Road, Glenside, SA, 5065</li>
            <li>Phone:  (08) 8338 6616 </li>
            <li>After hours: 0488896868 </li>
            <li>Email: contactus@burnsidenailsandspa.com</li>
	</ul>
  </div>

<div class="w3-col l6 w3-padding-large">
<iframe
  width="500"
  height="450"
 src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3270.6807033849914!2d138.63965131617968!3d-34.939543980374005!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6ab0cc03d6f8be51%3A0x894fea0e6a9342d!2sBurnside+Nails+And+Spa!5e0!3m2!1sen!2sau!4v1487130580377" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>

</div>  

<!-- End page content -->
</div>
