

<SECTION>
<style>


.adminsquares > * {
  border: 1px solid #c9ff23;
  border-radius: 5px;
  padding: 0px;
  flex-grow:1;
  overflow: hidden;
   transition: all 300ms ease-in-out;
  
  &:hover {
    flex-grow: 2;
    
  }
 
  
}

.adminsquares {
  display: flex;
  flex-flow: row wrap; 
  
  padding: 15px;
  gap: 5px;
  height: auto;
}


.adminsquares img {
  width: 100%;
}

</style>    
<div class="adminsquares">
{% for post in site.posts %}
    
<ARTICLE itemprop="blogPosts" itemscope itemtype="https://schema.org/BlogPosting" >
  <a href="{{ site.github.url }}{{ post.url }}">
    <div class="featured-post" {% if post.image %}style="background-image:url({{ site.github.url }}/assets/img/{{ post.image }})"{% endif %}>
      <h2 itemprop="headline"><span>{{ post.title }}</span></h2>
    </div>
  </a>
</ARTICLE>

{% endfor %}
</div>



</SECTiON>
</MAIN>