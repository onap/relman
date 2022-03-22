repos.yaml

Contains an entry for every ONAP project and related repositories, regardless
if the (sub)project is maintained, unmaintained, read-only or writeable.
Includes authorative information about repo state and release partizipation.

Example entry:

vnfsdk:                                 -project name

  - repository:   'vnfsdk/compliance'   -(sub)project/repository name
    unmaintained: 'false'               -maintenance state (true|false)
    read_only:    'true'                -gerrit state (true|false)
    included_in:  '[]'                  -list of (main|maintenance) releases
                                         which include the (sub)project,
                                         e.g. '[9,9M1,10]' (proposal!)

repos.yaml is complemented by a schema file named 'repos-schema.yaml'. It can
be used to validate 'repos.yaml'. Read more about yaml linting and validation
in https://docs.releng.linuxfoundation.org/en/latest/committer-management.html.
