---
layout: posts
category: project-organization
title:  "Kickoff meeting"
author: "Erik Tjong Kim Sang"
Date: 2021-09-28
comment_id: 2
---
On Tuesday 28 September 2021, the kickoff meeting was held for the project [Navigating Stories in Times of Transition](https://navigating-stories.github.io/notebooks/). Three people attended the meeting: principal investigator professor [Gerben Westerhof](https://people.utwente.nl/g.j.westerhof) of the University of Twente and program manager [Jisk Attema](https://www.esciencecenter.nl/team/dr-jisk-attema/) and research software engineer [Erik Tjong Kim Sang](https://www.esciencecenter.nl/team/dr-erik-tjong-kim-sang/), both from the Netherlands eScience Center. Also in the project is assistant professor [Anneke Sools](https://people.utwente.nl/a.m.sools) from the University of Twente and researcher [Stefan Bastholm Andrade](https://www.vive.dk/da/medarbejdere/stefan-bastholm-andrade-1634/). Still missing is the postdoc of the University of Twente. The university is recruiting now and we hope the postdoc will start in January.

The most important decision of the meeting was to start the project on 1 November 2021. Erik Tjong Kim Sang and Stefan Bastholm Andrade will perform the initial work.
	
The project will last for three years.

![Photo by Clay Banks on Unsplash](/assets/images/clay-banks-TRGRf4LvMdQ-unsplash.jpg)

<small>Photo by [Clay Banks](https://unsplash.com/@claybanks?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/research?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)</small>

<div id="comments">
  <script type="text/javascript">
  var writeToComment = function(element, html) {
    var element = document.createElement(element)
    element.innerHTML = html
    document.getElementById("comments").appendChild(element)
  }

  var loadComments = function(data) {
    writeToComment("h2", "Comments")

    for (var i = 0; i < data.length; i++) {
      var commentHTML = [...]
      writeToComment("div", commentHTML)
    }

    var callToAction = [...]
    writeToComment("div", callToAction)
  }

  var writeFirstComment = function() {
    var callToAction = [...]
    writeToComment("div", callToAction)
  }

  // This is mostly there now: http://caniuse.com/#feat=fetch
  if (window.fetch) {
    var url =
      "https://github-blog-comments.herokuapp.com/repos/navigating-stories/navigating-stories.github.io/issues/{{ page.comment_id }}/comments"

    window
      .fetch(url, { Accept: "application/vnd.github.v3.html+json" })
      .then(function(response) {
        return response.json()
      })
      .then(function(json) {
        if(json.length) {
          loadComments(json)
        } else {
          writeFirstComment()
        }
      })
  }
  </script>
  <h2>Comments</h2>
  {% if page.comment_id %}
    <article class='post'>
      {% include gh_comments.html %}
    </article>
  {% endif %}
  <div id="header">
    Want to leave a comment? Visit <a href="https://github.com/navigating-stories/navigating-stories.github.io/issues/{{page.comment_id}}"> this post's issue page on GitHub</a> (you'll need a GitHub account).
  </div>
</div>
