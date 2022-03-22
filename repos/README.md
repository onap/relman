# repos.yaml

Contains an entry for every ONAP project and related repositories, regardless
if the (sub)project is maintained, unmaintained, read-only or writeable.
Includes authorative information about repo state and release partizipation.

## Example entry:

```
vnfsdk:

  - repository:   'vnfsdk/compliance'
    unmaintained: 'false'
    read_only:    'true'
    included_in:  '[9,9M1,10]'

```

## Explanations:

`vnfsdk:` *project name*

`repository: 'vnfsdk/compliance'` *(sub)project/repository name*

`unmaintained: 'false'` *is the (sub)project unmaintained? (true|false)*

`read_only: 'true'` *is the (sub)project read-only in gerrit? (true|false)*

`included_in:  '[9,9M1,10]'` *list of (main|maintenance) releases which include the (sub)project (currently under discussion; not yet used!)*

# repos-schema.yaml

repos.yaml is complemented by a schema file named `repos-schema.yaml`. It can
be used to validate `repos.yaml`. Read more about yaml linting and validation
[here](https://docs.releng.linuxfoundation.org/en/latest/committer-management.html).

In particular, after downloading the `yaml-verify-schema.py` program, you can
run the following command to verify `repos.yaml` against the schema:

```shell
yaml-verify-schema.py --schema repos-schema.yaml --yaml repos.yaml
```
