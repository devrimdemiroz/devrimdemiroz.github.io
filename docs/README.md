{% for post in site.posts %}
{% if post.category =="home"%}
## {{ post.title }}
{{ post.content }}
{% endif %}
{% endfor %}


Next: [{{ site.posts.first.title }}]({{ site.posts.first.url }})


 