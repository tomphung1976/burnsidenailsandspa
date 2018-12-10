<!-- Pricing Modal -->
<div id="priceModal" class="w3-modal ">
    <div class="w3-modal-content w3-animate-zoom" style="width:50%">
        <div class="w3-container w3-padding-large">
            <span onclick="$('#priceModal').hide();" class="w3-closebtn">&times;</span>

            <div class="w3-center w3-padding-large">
                <h4> Best Deals </h4>
                <h1 style="font-size:50px; color:#5d5b5b;">Special Pricing</h1>
                <img src="{{ site.url }}/assets/images/breakline01.png" class="w3-round w3-image" width="500" height="70%">
            </div>
            <div class="w3-row border dropShadow price" >
                {% for g in site.data.price.groups %}
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
                {% endfor %}
          </div>
        </div>
    </div>
</div>
