# How to create a static website using jekyll

## Installing jekyll and launching a project

1. Install Jekyll in your terminal window
```
gem install jekyll
```
2. Go to the directory where the site materials will be stored. Use "new" to create a jekyll site folder.
```
cd ~/Documents
jekyll new yourwebsitename
cd yourwebsitename
```
3. Scaffolding jekyll website on a local host, use "-w" to watch for any file changes
```
jekyll serve -w --baseurl ""
```
4. A few things to mention about Jekyll site structures:
* All contents will get converted to the **_site** folder - it serves as the final version of the website
* **_layouts** folder is a Jekyll-specific folder that contains the site layout which will be the same for every page
* Use the {% ... %} structure to refer to a specific html file, e.g.:
```{html}
{% include default.html %}
```
5. To make a second page for the website:
* Create a new file "careers.html" and use yml front matter to specify the design template
```{html}
---
layout: default
<h1>Career</h1>
---
```
* Go back to **_layouts** folder and add navigation bar to the "default.html" file to connect the 2 pages together. Use "{{site.baseurl}}/" to append separate pages to the main site url.
```{html}
<header>
  <h1>Site Header</h1>
  <nav>
    <ul>
      <li><a href="{{site.baseurl}}/index.html">Home</a></li>
      <li><a href="{{site.baseurl}}/careers.html">Careers</a></li>
    </ul>
  </nav>
</header>
```
6. To utilize the includes functionality of Jekyll, take the navigation code snippet and put it into a new file under **_includes** folder, call it "nav.html"
```{html}
<nav>
    <ul>
      <li><a href="{{site.baseurl}}/index.html">Home</a></li>
      <li><a href="{{site.baseurl}}/careers.html">Careers</a></li>
    </ul>
  </nav>
```
7. Go back to the "default.html" under **_layouts** folder and use Jekyll tag to include the navigation snippet
```{html}
{% include nav.html %}
```
...and this will prompt Jekyll to look for a file called "nav.html" in the **_includes** folder and call it




