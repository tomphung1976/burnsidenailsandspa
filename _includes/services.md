<!-- Services Section -->
<div class="w3-row w3-padding-32 " id="services">
    <div class="w3-left w3-third">
        <h2>Our Services</h2>
    </div>
    <div class="w3-row w3-center w3-margin-xlarge">
        <div class="w3-half w3-padding-large w3-opacity-min w3-hover-opacity-off" onclick="showModal('#Acrylic')">
            <div class="w3-card-2">
                <img src="{{ site.url }}/assets/images/services/nails01.png" class="w3-round w3-image" alt="Service" width="500" height="750">
                <h4>Acrylic</h4>
            </div>
        </div>
        <div class="w3-half w3-padding-large w3-opacity-min w3-hover-opacity-off" onclick="showModal('#Gelnails')">
            <div class="w3-card-2">
                <img src="{{ site.url }}/assets/images/services/nails02.png" class="w3-round w3-image" alt="Service" width="500" height="750">
                <h4>Gel Nails</h4>
            </div>
        </div>
        <!--2nd row-->
        <div class="w3-third w3-padding-large w3-opacity-min w3-hover-opacity-off" onclick="showModal('#Shellac')">
            <div class="w3-card-2">
                <img src="{{ site.url }}/assets/images/services/nails05.png" class="w3-round w3-image" alt="Service" width="500" height="750">
                <h4>Shellac</h4>
            </div>
        </div>
        <div class="w3-third  w3-padding-large w3-opacity-min w3-hover-opacity-off" onclick="showModal('#Waxing')">
            <div class="w3-card-2">
                <img src="{{ site.url }}/assets/images/services/waxing.png" class="w3-round w3-image" alt="Service" width="300" height="750">
                <h4>Waxing</h4>
            </div>
        </div>
        <div class="w3-third w3-padding-large w3-opacity-min w3-hover-opacity-off" onclick="showModal('#Tint')">
            <div class="w3-card-2">
                <img src="{{ site.url }}/assets/images/services/nails06.png" class="w3-round w3-image" alt="Service" width="500" height="750">
                <h4>Tint</h4>
            </div>
        </div>
        <!-- 3rd row-->
        <div class="w3-half w3-padding-large  w3-opacity-min w3-hover-opacity-off" onclick="showModal('#Manicure')">
            <div class="w3-card-2">
                <img src="{{ site.url }}/assets/images/services/nails03.png" class="w3-round w3-image" alt="Service" width="500" height="750">
                <h4>Manicure</h4>
            </div>
        </div>
        <div class="w3-half w3-padding-large  w3-opacity-min w3-hover-opacity-off" onclick="showModal('#Pedicure')">
            <div class="w3-card-2">
                <img src="{{ site.url }}/assets/images/services/nails04.png" class="w3-round w3-image" alt="Service" width="500" height="750">
                <h4>Pedicure</h4>
            </div>
        </div>
    </div>
</div>

<!-- Services Modal -->
<div id="servicesModal" class="w3-modal ">
    <div class="w3-modal-content w3-animate-zoom" style="width:50%">
        <div class="w3-container">
            <span onclick="$('#servicesModal').hide();" class="w3-closebtn">&times;</span>
            <div id="serviceDetails" style="margin:5%">
              {% for service in site.data.services %}
              <div id="{{service.id}}" style="display:none;">
                  <h1 class="w3-center" style="font-size:50px; color:#5d5b5b;">{{service.name}}</h1>

                  <div class="w3-center"><img src="{{ site.url }}{{service.image}}" class="w3-round w3-image" alt="Service" width="80%" height="100%"></div>
                  {{service.description}}
              </div>
              {% endfor %}                
            </div>
        </div>
    </div>
</div>

<script>
function showModal(id){
  $(id).show();
  $(id).siblings('div').hide();
  $('#servicesModal').show();
}
</script>
