# jupyter-jsc-custom-share-template
Template repository for custom JupyterHub templates and static files.

To use this template, click **Use this template** above the file list and select **Include all branches** when creating your repository.

Reference templates and static files used by the Jupyter-JSC JupyterHub can be found [in this repository](https://github.com/FZJ-JSC/jupyter-jsc-share).

## Templates

This branch contains any templates and static files that should be changed on the production JupyterHub instance. Templates are written in [Jinja](https://jinja.palletsprojects.com/en/3.1.x/). For more information, refer to the [official JupyterHub documentation](https://jupyterhub.readthedocs.io/en/stable/reference/templates.html).

### Suggested changes for a custom JupyterHub

* Change header and footer as desired. Any logos should be placed in the `static/images` directory. 

* You may want to update the meta data in `page.html`.

* You may want to change the login text in `<div id="upper-login-div">` and carousel texts of the `templates/login.html` file as well as the carousel backgrounds in `static/css/login.css`.

* If you want to link to different or additional pages, update `links.html`.

* The privacy policy may be updated in `dps.html`.

## Available variables

Some variables are passed from JupyterHub and available as Jinja variables in the templates. The following variables are available in all templates:

```python
base_url  # hub.base_url
prefix  # base_url
user  
login_url
login_service
logout_url
static_url  # url location of static files
version_hash  # e.g. datetime.now().strftime("%Y%m%d%H%M%S")
services  # list of services returned by `get_accessible_services(user)`
parsed_scopes  # scopes for a user
expanded_scopes  

# and any variables defined in under `template_vars` in the JupyterHub config file
```