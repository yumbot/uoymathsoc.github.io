---
layout: page
title: Meet the Committee
permalink: /about/
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

<head>
<style>
.card {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    max-width: 256px;
    margin: auto;
    text-align: center;
}

.container {
    padding: 0 16px;
}

.title {
    color: grey;
    font-size: 18px;
}

button {
    border: none;
    outline: 0;
    display: inline-block;
    padding: 8px;
    color: white;
    background-color: #000;
    text-align: center;
    cursor: pointer;
    width: 100%;
    font-size: 18px;
}

a {
    text-decoration: none;
    font-size: 22px;
    color: black;
}

button:hover, a:hover {
    opacity: 0.7;
}
</style>
</head>

We are a society aimed at everyone with an interest in mathematics. With social and academic motives we organise public lectures delivered by globally renowned external speakers who are leaders in their field, study groups aimed at ensuring you are fully supported with your exam preparation, as well as a diverse array of social events; including a few trips away in the forthcoming year.

## Our current committee consists of:

<div>
{% for member in site.data.committee.members %}
    
    {% if member.itsUsername == null %}
        {% continue %}
    {% endif %}    

    <div class="card" id="{{ member.itsUsername }}">
        <img src="{{ site.url }}/images/portrait_{{member.itsUsername}}.jpg" alt="{{ member.name }}" style="width:100%" onError="src='{{ site.url }}/images/portrait_.jpg'">
        <div class="container">
            <h1>{{ member.name }}</h1>
            <p class="title">{{ member.position }}</p>
            <p class="bio">
                {% assign bio = site.data.committee.bios.[member.itsUsername] %}
                {% if bio == null %}
                    <!--Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut at tincidunt magna, nec tempor nulla. Integer quis fermentum diam. Sed tempus massa eu elit dignissim consectetur. Nunc pretium congue nisi, at ullamcorper quam euismod et. Nullam non semper urna. Donec vestibulum felis vitae nisi rutrum.-->
                {% else %}
                    {{ bio }}
                {% endif %}
            </p>
            <a href="#"><i class="fa fa-twitter"></i></a> 
            <a href="#"><i class="fa fa-linkedin"></i></a> 
            <p><button>Contact</button></p>
            
            <!--<a href="mailto:{{ member.handle | split:'_' | first }}@yums.org.uk">{{ member.handle | split:'_' | first }}@yums.org.uk</a>-->
        </div>
    </div>

{% endfor %}
</div>

{% comment %}

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

{% endcomment %}
