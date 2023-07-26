---
layout: home
---

<style type="text/css">
.float-container {
    /* border: 3px solid #fff; */
    padding: 20px;
}

.float-child {
    width: 40%;
    float: left;
    padding: 20px;
    /* border: 2px solid red; */
}

.proof-of-membership {
  color:#8c0e0e;
}
</style>


<p>Please check the websites of the museums you plan to visit prior to your arrival for hours and admission information. To receive admissions discounts listed, please purchase your tickets at the door.</p>


<h2 class="proof-of-membership">Show Proof Of Membership At Any Of Our Museums For Discounts When You Visit</h2>

{% for museum in site.museums %}
<!-- {{ museum.name }} -->
<div class="float-container">

  <div class="float-child"><div><img width="{{museum.img_width}}" height="{{museum.img_height}}" src="{{museum.img}}"></div></div><!-- float-child -->

  <div class="float-child"><div>
  <blockquote>
    <p><strong>{{ museum.name }}</strong></p>
    <p>{{ museum.address }}</p>
    <p><a href="{{ museum.url }}">{{ museum.url }}</a></p>
    <p>{{ museum.phone }}</p>
    <p>{{ museum.discount }}</p>
  </blockquote>
  </div></div><!-- float-child -->

</div><!-- float-container -->
<div style="clear:both" />
{% endfor %}


