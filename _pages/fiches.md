---
title: Fiches
layout: archive
permalink: /fiches/
entries_layout: grid
---


Des fiches explicatives

[Je suis un parent]({{ site.baseurl }}{% link _pages/parent.md %}){:  #parent .btn .btn--primary .btn--large}
[Je suis un professionnel]({{ site.baseurl }}{% link _pages/pro.md %}){: #pro .btn .btn--primary .btn--large}


<script>

let makeHandlerFor = (tag) => { 
return (event) => {
	event.preventDefault();
	fetch("https://api.countapi.xyz/hit/jallaite/" + tag)
		.then(() => {window.location.href = event.target.href;});
	}
}


let parent = document.getElementById("parent");
parent.onclick = makeHandlerFor("parent");

let pro = document.getElementById("pro");
pro.onclick = makeHandlerFor("pro");

</script>
