# Setting up GraphQL in Django

This guide will walk you through setting up GraphQL in a Django project using the `graphene-django` library.

## Step 1: Set Up a Django Project

First, set up your Django project if you haven't already:

```bash
django-admin startproject myproject
cd myproject
```

## Step 2: Set Up a Django Project

Create a new app within your Django project:

```bash
django-admin startproject myproject
cd myproject
```

## Step 3: Install Graphene-Django

Install the graphene-django package:

```bash
pip install graphene-django
```

## Step 4: Add Graphene-Django to Installed Apps

Edit your settings.py file to add graphene_django to the INSTALLED_APPS list:

```python 
    INSTALLED_APPS = [
        ...
        'graphene_django',
    ]
```
## Step 5: Configure URLs for GraphQL

Edit the urls.py file inside your main Django project to include the GraphQL endpoint:

```python
# myproject/urls.py

from django.contrib import admin
from django.urls import path
from graphene_django.views import GraphQLView
from django.views.decorators.csrf import csrf_exempt

urlpatterns = [
    path('admin/', admin.site.urls),
    path('graphql/', csrf_exempt(GraphQLView.as_view(graphiql=True))),  # Change graphiql=True to graphiql=False if you do not want to use the GraphiQL API browser.
]
```

## Step 6: Define Schema Location in Settings

Specify the schema location for Graphene in your settings.py file:

```python
# settings.py

GRAPHENE = {
    "SCHEMA": "myproject.schema.schema"  # Update to match your project structure
}
```

## Step 7: Create Schema File

Create a schema.py file inside your app or project directory. Define the schema in this file:

```python
# apiapp/schema.py

import graphene

class Query(graphene.ObjectType):
    pass

schema = graphene.Schema(query=Query)
```

## Step 8: Update URLs to Use Schema

Edit your urls.py file to use the defined schema:

```python
# myproject/urls.py
from graphene_django.views import GraphQLView
from django.views.decorators.csrf import csrf_exempt
from apiapp.schema import schema  # Update to match 

urlpatterns = [
    path('admin/', admin.site.urls),
    path('graphql/', csrf_exempt(GraphQLView.as_view(graphiql=True, schema=schema))),
]
```

## Conclusion

You have successfully set up GraphQL in your Django project. You can now start defining your GraphQL queries and mutations in the schema.py file and test them using the GraphiQL interface at http://127.0.0.1:8000/graphql/.
Additional Resources

    Graphene-Django Documentation
    Django Documentation