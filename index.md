--- 
layout: default 
--- 
{% for post in site.posts limit:site.postCount %}
<div class="post">
  <div class="post__meta">
    <div class="post__title"><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></div>
    <div class="post__text">
      {{ post.excerpt }}
    </div>
    <div class="post__postfix">
      <span class="post__date">{{ post.date | date: "%b %-d, %Y" }}</span>
      <span class="post__postfix--separator"></span>
      <a href="{{ post.url | prepend: site.baseurl | prepend: site.url }}" title="{{ post.title}}">계속 읽기...</a>
    </div>
  </div>
</div>
{% endfor %}
<div class="more_posts">
  <a href="{{ '/archive' | prepend: site.baseurl | prepend: site.url }}">모든 글 보기</a>
</div>