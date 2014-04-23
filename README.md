expressionEngineToWordpress
===========================

An xml template for expression engine to export posts/categories/tags/media to a wordpress xml format.

Based on work of Travis Smith (http://www.hopstudios.com/blog/exporting_from_expressionengine_into_wordpress). However:

- I needed a way to export all categories
- My articles had a little different field names 
- I use a tags addon (Tag: http://www.solspace.com/software/detail/tag/) and I wanted my tags to be transfered too
- My articles had cover images attached to them, and I wanted wordpress to import them and handle them as featured photos


So, here's how it works:

1. In expression engine, set up a template group called “Export” (or whatever you like) and a tamplate file (mine is index). 
2. Set the template to be XML, allow PHP and set it to run in output stage. 
3. Paste my xml file in the editor
4. Edit it to handle your own fields and urls
5. View it, download it and use it as a wordpress import file to get all your content.


Field names:
- My featured image is: {main_hd_image}
- {article_description} is the short description (used as excerpt in wordpress)
- {article_body} is the actual article


Notes:
Due to boredom (:p), I don't handle the dates of images in media files import, so all of them take a default "Sun, 23 Mar 2014 23:48:28 +0000". Same goes for xml pubDate (Tue, 22 Apr 2014 11:12:48 +0000). I don't think that's important, but if you need the actual dates, the modification would be easy.
