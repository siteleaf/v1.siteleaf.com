---
title: Developer friendly
date: 2015-03-31 21:44:00 Z
graphic_html: |-
  ```liquid
  <html>
    <head>
      <title>{{ title }} - {{ site.title }}</title>
    </head>
    <body>
      <nav>
        {% for page in site.pages %}
          <a href="{{ page.url }}">{{ page.title }}</a>
        {% endfor %}
      </nav>

      <h1>{{ title }}</h1>
      <div class="page-description">{{ body }}</div>

      {% for post in posts %}
        <article>
          <h2>{{ post.title }}</h2>
          {{ post.body }}
        </article>
      {% endfor %}

      <footer>Copyright {{ site.date | date: "%Y" }}</footer>
  </body>
  </html>
  ```

  ```ruby
  $ siteleaf config example.com
  => "Site configured with Pow, open `http://example.dev` to test site locally."

  $ siteleaf push theme
  => "20 assets uploaded"
  ```
---

