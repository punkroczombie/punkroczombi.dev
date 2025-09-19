---
layout: base.njk
permalink: index.html
title: Zombie's Website
description: Welcome to my page
---

<section class="half">
    <h1>Welcome to my homepage!</h1>
    <h2>You are visitor # <span id="hitcount"></span></h2>
    <p>Thanks for checking out my website, its currently under construction as I relearn how to use HTML and CSS.</p>
</section>

<section class="small">
    <h2>Blog Posts</h2>
    <ul class="none">
        {% assign top_posts = collections.posts | reverse %}
        {%- for post in top_posts -%}
          <li><a href="{{ post.data.permalink }}">{{ post.data.date | readableDate }} » {{ post.data.title }}</a></li>
        {% endfor %}
    </ul>
</section>

<section class="half">
    <h2>Button Wall</h2>
    <img src="https://www.88x31.nl/gifs/discord2.gif" alt="discord2.gif"  height="31" width="88">
    <img src="https://www.88x31.nl/gifs/christnow (2).gif" alt="christnow (2).gif"  height="31" width="88">
    <img src="https://www.88x31.nl/gifs/delete_twitter.gif" alt="delete_twitter.gif"  height="31" width="88">
    <img src="https://www.88x31.nl/gifs/internetprivacy.gif" alt="internetprivacy.gif"  height="31" width="88">
    <img src="https://www.88x31.nl/gifs/internetarchive.gif" alt="internetarchive.gif"  height="31" width="88">
    <img src="https://www.88x31.nl/gifs/tumblr_ou69s0gvdZ1wvu485o9_100.gif" alt="tumblr_ou69s0gvdZ1wvu485o9_100.gif"  height="31" width="88">
    <img src="https://pixelsafari.neocities.org/buttons/1guestbook3.gif" alt="1guestbook3.gif"  height="31" width="88">
    <img src="https://pixelsafari.neocities.org/buttons/1linux2.gif" alt="1linux2.gif"  height="31" width="88">
    <img src="https://pixelsafari.neocities.org/buttons/1notepad.png" alt="1notepad.png"  height="31" width="88">
    <img src="https://cyber.dabamos.de/88x31/cssdif.gif" alt="cssdif.gif"  height="31" width="88">
    <img src="https://cyber.dabamos.de/88x31/ipv6.gif" alt="ipv6.gif"  height="31" width="88">
    <img src="https://cyber.dabamos.de/88x31/jellyfin.gif" alt="jellyfin.gif"  height="31" width="88">
    <img src="https://cyber.dabamos.de/88x31/valid-bad.gif" alt="valid-bad.gif"  height="31" width="88">
    <img src="https://anlucas.neocities.org/piracy.gif" alt="piracy.gif"  height="31" width="88">
    <img src="https://skye.sh/media/content/88x31/monero-now.gif" alt="monero-now.gif"  height="31" width="88">
    <img src="https://88x31.nl/gifs/websitering.gif" alt="websitering.gif"  height="31" width="88">
</section>

<section class="half">
    <h2>My other sites:</h2>
    <ul>
        <li><a href="https://thekrew.network/">thekrew.network</a></li>
    </ul>
</section>

<section class="half">
    <div id="letterboxd-embed-wrapper-tc">Loading...</div>
    <script>
    fetch('https://lb-embed-content.bokonon.dev?username=punkroczombi')
    .then(response => response.text())
    .then(data => {
    document.getElementById('letterboxd-embed-wrapper-tc').innerHTML = data;
    });
    </script>
</section>

<section class="half">

</section>

<section class="full">
    <div style="max-width: fit-content;margin-left: auto;margin-right: auto;">
        <img src="http://www.snazzyspace.com/generators/viewer-counter/counter.php/fid=1758033921/style=5/counter.png" border="0">
    </div>
</section>


<div id="oneko">
    <script src="/scripts/widgets/oneko/oneko.js"></script>
</div>

<script>
    var xhttp = new XMLHttpRequest();
    xhttp.onreadystatechange = function () {
        if (this.readyState === 4 && this.status === 200) {
            var site_data = JSON.parse(this.responseText);
            var num_arr = site_data.info.views.toString().split("");
            var num_str = "";
            for (i = 0; i < num_arr.length; i++) {
                num_str += num_arr[i];
                if ((num_arr.length - 1 - i) % 3 === 0 && num_arr.length - 1 - i !== 0) {
                    num_str += ",";
                }
            }
            document.getElementById("hitcount").innerHTML = num_str;
        }
    };
    xhttp.open(
        "GET",
        "https://weirdscifi.ratiosemper.com/neocities.php?sitename=punkroczombi",
        true,
    );
    xhttp.send();
</script>