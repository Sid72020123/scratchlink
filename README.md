# ScratchLink v1.0.1

## Introduction

ScratchLink is a simple Python Library to get the data of Scratch using the Scratch API. This library is simple to use.
This library need no login!

## Installation

To use this library you must need to install the Python Programming Language. If you have already installed Python then
type the following in the Terminal (Command Prompt):

```bash
pip install scratchlink
```

## Import

To import scratchlink, use the following code:

```python
import scratchlink  # Import Library

scratch = scratchlink.ScratchLink()  # Create an object of the ScratchLink class
```

## Getting The Data

### Front Page Data

To get the front page data of Scratch Website, run the following Program:

```python
import scratchlink

scratch = scratchlink.ScratchLink()
front_page = scratch.link_frontpage()  # Connect the front page

front_page.health()  # Get the health of the website
front_page.news()  # Get the news of the website
front_page.front_page_projects()  # Get the front page projects of the website
front_page.explore_projects(mode="trending", query="*")  # Explore the projects
front_page.explore_studios(mode="trending", query="*")  # Explore the studios
front_page.search_projects(mode="trending", search="*")  # Search the projects
front_page.search_studios(mode="trending", search="*")  # Search the studios
```

### User Data

To get the user data, run the following Program:

```python
import scratchlink

scratch = scratchlink.ScratchLink()
user = scratch.link_user(username="Sid72020123")  # Connect a Scratch User

user.id()  # Returns the ID of the user
user.thumbnail_url()  # Returns the thumbnail URL of a user
user.messages_count()  # Returns the messages count of the user
user.work()  # Returns the 'What I am working on' of a Scratch profile
user.bio()  # Returns the 'About me' of a Scratch profile
user.status()  # Returns the status(Scratcher or New Scratcher) of a Scratch profile
user.joined_date()  # Returns the joined date of a Scratch profile
user.country()  # Returns the country of a Scratch profile
user.featured_data()  # Returns the featured project data of the Scratch profile
user.projects()  # Returns the list of shared projects of a user
user.followers_count()  # Returns the follower count of a user
user.following_count()  # Returns the following count of a user
user.total_views_count()  # Returns the total views count of all the shared projects of a user
user.total_loves_count()  # Returns the total loves count of all the shared projects of a user
user.total_favourites_count()  # Returns the total favourites count of all the shared projects of a user
user.following()  # Returns the list of the user following
user.followers()  # Returns the list of the user followers
user.favourites()  # Returns the list of the user favourites
user.user_follower_history()  # Return the follower history of the user
user.all_data()  # Returns all the data of the user
user.comments(limit=5, page=1)  # Get comments of the profile of the user
user.pretty_print_user_data()  # Pretty print the user data
##########################################################################
# IMPORTANT NOTE: To always get the updated data use the update_data() function
##########################################################################
user.update_data()  # Update the data
```

### Studio Data

To get the studio data, run the following Program:

```python
import scratchlink

scratch = scratchlink.ScratchLink()
studio = scratch.link_studio(studio_id=1)  # Connect a Scratch Studio

studio.id()  # Returns the studio ID
studio.title()  # Returns the studio title
studio.host_id()  # Returns the studio owner/host ID
studio.description()  # Returns the studio description
studio.visibility()  # Returns the studio visibility
studio.is_public()  # Returns whether a studio is public
studio.is_open_to_all()  # Returns whether a studio is open to all
studio.are_comments_allowed()  # Returns whether a studio has comments allowed
studio.history()  # Returns the history of the studio
studio.stats()  # Returns the stats of the studio
studio.thumbnail_url()  # Returns the thumbnail URL of the studio
studio.projects(all=False, limit=40, offset=0)  # Get the projects of the studio
studio.comments(all=False, limit=40, offset=0)  # Get the comments of the studio
studio.curators(all=False, limit=40, offset=0)  # Get the curators of the studio
studio.managers(all=False, limit=40, offset=0)  # Get the managers of the studio
studio.activity(all=False, limit=40, offset=0)  # Get the activity of the studio
studio.pretty_print_studio_data()  # Pretty print the Studio Data
##########################################################################
# IMPORTANT NOTE: To always get the updated data use the update_data() function
##########################################################################
studio.update_data()  # Update the data
```

### Project Data

To get the project data, run the following Program:

```python
import scratchlink

scratch = scratchlink.ScratchLink()
project = scratch.link_project(project_id=1)  # Connect a Scratch Project

project.author()  # Returns the author of the project
project.title()  # Returns the title of the project
project.notes()  # Returns the notes(Notes or Credits) of the project
project.instruction()  # Returns the instructions of the project
project.are_comments_allowed()  # Returns whether the comments are allowed in a project
project.stats()  # Returns the stats of a project
project.history()  # Returns the history of a project
project.remix_data()  # Returns the remix data of a project
project.visibility()  # Returns whether the project is visible
project.is_public()  # Returns whether the project is public
project.is_published()  # Returns whether the project is published
project.thumbnail_url()  # Returns the thumbnail url of a project
project.assets_info()  # Returns the Assets info of a project
project.scripts()  # Returns the scripts of a project
project.comments(all=False, limit=40, offset=0, comment_id=None)  # Returns the list of comments of a project
project.remixes(all=False, limit=20, offset=0)  # Returns the list of remixes of a project
project.pretty_print_project_data()  # Pretty print the project data
##########################################################################
# IMPORTANT NOTE: To always get the updated data use the update_data() function
##########################################################################
project.update_data()  # Update the data
```

### Cloud Data

To get the cloud data of a project, run the following Program:

```python
import scratchlink

scratch = scratchlink.ScratchLink()
project = scratch.link_project(project_id=1)  # Connect a Scratch Project

cloud = project.link_cloud()  # Connect the Cloud Variables of a project
cloud.get_variable_data(limit=100, offset=0)  # Get the variable data
cloud.get_cloud_variable_value(variable_name="Name",
                               limit=100)  # Get the variable value. This will return a list containing many values. The first item in the list is the current value
cloud.pretty_print_cloud_data()  # Pretty print the cloud data
```

### Forum Topic Data

To get the forum topic data, run the following Program:

```python
import scratchlink

scratch = scratchlink.ScratchLink()
forum = scratch.link_forum(topic_id=1)  # Connect a Scratch Forum Topic

forum.id()  # Returns the id of the forum
forum.title()  # Returns the title of the forum
forum.category()  # Returns the category of the forum
forum.is_closed()  # Returns whether the forum is closed or not
forum.is_deleted()  # Returns whether the forum is deleted or not
forum.time()  # Returns the activity of the forum
forum.post_count()  # Returns the total post count of the forum
forum.posts(page=1)  # Get the post in Forum Topic of a specified page. Images and some other stuff will not appear!
forum.pretty_print_topic_data()  # Pretty print the topic data
##########################################################################
# IMPORTANT NOTE: To always get the updated data use the update_data() function
##########################################################################
forum.update_data()  # Update the data
```

## Bug Reporting

All Bugs to be reported on my [Scratch Profile](https://scratch.mit.edu/users/Sid72020123/)
or [Github](https://github.com/Sid72020123/scratchlink/issues)

## Data Providers

Data is taken from the [Scratch API](https://github.com/LLK/scratch-rest-api) by the Scratch Team
and [Scratch DB](https://scratchdb.lefty.one/) by [@DatOneLefty](https://scratch.mit.edu/users/DatOneLefty/) on Scratch

## Credits

This Library is made by [@Sid72020123](https://scratch.mit.edu/users/Sid72020123/) on Scratch

## Change Log

* 11/12/2021(v0.5) - First Started Making This Library.
* 12/12/2021(v1.0) - Updated and First Release!
* 27/01/2022(v1.0.1) - Updated Comments API

## Thank You!