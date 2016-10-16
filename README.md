sffoodtrucks
============
**Project Chosen**: Food Trucks


**Technical Track**: Full Stack (a trivial back-end). The back-end sets up an API endpoint, /foodtrucks, that retrieves food trucks data from https://data.sfgov.org/Permitting/Mobile-Food-Facility-Permit/rqzj-sfat and sends it back to the front-end. The back-end is trivial in the sense that it does nothing beyond handing data from somewhere else to the front-end; I could have let the front-end directly talk to DataSF's API, which could also be faster than going through a backend. However, I chose to implement a trivial back-end because it allows more opportunities of code optimization. For example, assuming DataSF's food trucks data does not change very often, I can make the back-end store a copy of DataSF's data into its own database and periodically update that data, thereby speeding up data transfer to the front-end.

**Technical Details**:

The back-end is implemented with Django 1.5. I learnt Django a year ago by using it to build a simple discussion board. Among the .py files, sffoodtrucks/views.py is written by me. I have also modified jinghaozhou/settings.py, jinghaozhou/urls.py, jinghaozhou/wsgi.py, sffoodtrucks/urls.py.

The front-end is implemented with Javascript(Jquery). The main files to look at are sffoodtrucks/static/js/index.js, sffoodtrucks/static/css/index.css, jinghaozhou/templates/index.html.


**Design Trade-offs**:
I decide to not include any title or description about the tool but make the map take up the whole page. Because this is a specific tool that does a specific task, I assume that most people who check out this tool already know what it is about. It may be good to display a set of onboarding popups for first-time visitors to learn about the tool and how to use it, but it may not be necessary to have a fixed section on the page that explains all this. A map that takes up the whole page, on the other hand, looks clean and simple. Also, the loading page helps explain the tool too.



