## Step #5

### Handling migrations
We want to store passwords more securely, but for that we need to change the database. To handle these changes we use a process called 'migrations'. Flask allows to do this using a module called flask-migrate.
- Change db.init to drop the database and create it (needs to be in control from start) and run it
- Add flask-migrate to requirements.txt and install it
- Add migrate commands to manage.py and __init__.py
- Initialize using ```python manage.py db init```. This will add a migrations folder to your application.
- You can then generate an initial migration:
```python manage.py db migrate```
- And then apply the changes to the database using:
```python manage.py db upgrade```.
  - Each time the database models change repeat the migrate and upgrade commands
  - To sync the database in another system, jut run the upgrade command.
- Take out the blog checking part of the /admin and run /setup directly
