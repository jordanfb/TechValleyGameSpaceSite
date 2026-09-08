---
layout: page
title: Board Meeting Minutes
permalink: /minutes/
path: minutes
---

As we migrate over to this new site layout we're working on making all our past meeting minutes availible.
Please feel free to reach out if you're looking for minutes that are not listed below.

<br>

<div id="minute_list">List Unable to Load - Please Enable Javascript or visit <a target=null href="https://github.com/TechValleyGameSpace/TechValleyGameSpace.github.io/tree/main/files/board_minutes">https://github.com/TechValleyGameSpace/TechValleyGameSpace.github.io/tree/main/files/board_minutes</a></div>


<script>
    (async () => {
    const response = await fetch('https://api.github.com/repos/TechValleyGameSpace/TechValleyGameSpace.github.io/contents/files/board_minutes/');
    const data = await response.json();
    data.reverse(); // so that it's more recent dates on the top of the page
    let htmlString = '<ul>';
    
    for (let file of data) {
        htmlString += `<li><a href="/${file.path}">${file.name}</a></li>`;
    }

    htmlString += '</ul>';
    document.getElementById('minute_list').setHTML(htmlString) || document.getElementById('minute_list').setHTMLUnsafe(htmlString);
    })()
</script>