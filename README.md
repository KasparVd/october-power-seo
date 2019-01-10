Power SEO an OctoberCMS Plugin
=============

_First please note that this plugin was originally created by AnandPatel, however after 2 years of no support and many 
issues with the plugin, I have taken over the plugin development and maintain it under a new repository. This new 
version fixes the server errors in the old plugin._

###Inject SEO fields to CMS Pages, Static Pages and Blog.

This plugin add SEO fields to CMS Pages, Static Pages and Blog, and for using it you simply need to drop component on layout/page.

Current fields:
* Meta Title
* Meta Description
* Meta Keywords
* Canonical URL
* Meta Redirect to other URL
* Robot Index & Follow

__*for more fields, please open an issue and request this on the git repository__

####Features
* Open Graph(og) Tags added for better social sharing
* Settings added in backend to configure meta and Open Graph tags

####Future Development
* Integration of SEO optimizer to optimize pages

####Like this plugin?
If you like this plugin, plese give it a star on GitHub

#Documentation

##Installation
To install this plugin you have to click on __add to project__ or need to type __SureSoftware.SeoExtension__ in Backend *System > updates > intall plugin*

The plugin currently includes three components:
* SEO CMS Page
* SEO Blog Post
* SEO Static Page

####**SEO CMS Page**
Put the component in the CMS Layout

``````````````````
    <html>
        <head>
            {% component 'SeoCmsPage' %}
        </head>
        <body>
           {% page %}
        </body>
    </html>
``````````````````


####**SEO Blog Post**
Put the component in the page with the blogPost component and pass the post as a parameter

``````````````````
    {% component 'blogPost' %}
    {% component 'SeoBlogPost' data=post %}
``````````````````

> You must place also SeoCMSPage component on layout

#####**SEO Static Page**
Put the component in the head of the Static Pages Layout

``````````````````
    <html>
        <head>
            {% component 'SeoStaticPage' %}
        </head>
        <body>
            {% component 'staticMenu' %}
            {% component 'staticBreadcrumbs' %}
            {% page %}
        </body>
    </html>
``````````````````

####Configuration
To configure this Plugin goto Backend *System* then find *My Settings* in left side bar, then click on *SEO Extension*