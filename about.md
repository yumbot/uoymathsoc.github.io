---
layout: page
title: Meet the Committee
permalink: /about/
---

We are a society aimed at everyone with an interest in mathematics. With social and academic motives we organise public lectures delivered by globally renowned external speakers who are leaders in their field, study groups aimed at ensuring you are fully supported with your exam preparation, as well as a diverse array of social events; including a few trips away in the forthcoming year.

## Our current committee consists of:

<div>
{% for member in site.data.committee.members %}
    
    {% if member.itsUsername == null %}
        {% break %}
    {% endif %}
    
    <h3> {{ member.name }} - {{ member.position }} </h3>
    <img style="float: left;" hspace="20" src="{{ site.url }}/images/portrait_{{member.itsUsername}}.jpg" onError="src='{{ site.url }}/images/portrait_.jpg'">
    
    <p>
        {% assign bio = site.data.committee.bios.[member.itsUsername] %}
        {% if bio == null %}
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut at tincidunt magna, nec tempor nulla. Integer quis fermentum diam. Sed tempus massa eu elit dignissim consectetur. Nunc pretium congue nisi, at ullamcorper quam euismod et. Nullam non semper urna. Donec vestibulum felis vitae nisi rutrum.
        {% else %}
          {{ bio }}
        {% endif %}
    </p>
    
    <a href="mailto:{{ member.handle | split:'_' | first }}@yums.org.uk">{{ member.handle | split:'_' | first }}@yums.org.uk</a>

{% endfor %}
</div>

<!---

### Jack Davidson - President
<img style="float: left;" hspace="20" src="{{ site.url }}/images/portrait_jwd508.jpg">

Jack is a 2nd year MMath student with an interest in Programming and Statistics, he aims in the future to sell out and work in a investment banking firm. In his spare time he enjoys playing video games, going to the gym, and playing guitar.

[president@yums.org.uk](mailto:president@yums.org.uk)

### Jack Patrick - Secretary
<img style="float: left;" hspace="20" src="{{ site.url }}/images/portrait_placeholder.jpg">

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut at tincidunt magna, nec tempor nulla. Integer quis fermentum diam. Sed tempus massa eu elit dignissim consectetur. Nunc pretium congue nisi, at ullamcorper quam euismod et. Nullam non semper urna. Donec vestibulum felis vitae nisi rutrum.

[secretary@yums.org.uk](mailto:secretary@yums.org.uk)

### Nathan Plumb - Treasurer
<img style="float: left;" hspace="20" src="{{ site.url }}/images/portrait_np816.jpg">

Nathan studies Actuarial Science and as such is mainly interested in Statistical Mathematics. In his free time he is an accomplished musician, playing in two orchestras and having achieved three grade 8’s. In what little spare time he worries about how little time he has left to do homework in.

[treasurer@yums.org.uk](mailto:treasurer@yums.org.uk)

### Keziah Clarke - Academic Officer
<img style="float: left;" hspace="20" src="{{ site.url }}/images/portrait_kc1035.jpg">

She studies Mathematics and Statistics, her particular interest is in Stochastic analysis. Other than sleeping and having fun processing data on R-studio, she also enjoys going to see plays at the theatre and to local heavy metal gigs, doing pole exercise and playing darts!

[academic@yums.org.uk](mailto:academic@yums.org.uk)

--->
