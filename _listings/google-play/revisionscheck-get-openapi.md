---
swagger: "2.0"
x-collection-name: Google Play
x-complete: 0
info:
  title: Google Play Check Revision
  version: 1.0.0
  description: Checks whether the games client is out of date.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /revisions/check:
    get:
      summary: Check Revision
      description: Checks whether the games client is out of date.
      operationId: games.revisions.check
      x-api-path-slug: revisionscheck-get
      parameters:
      - in: query
        name: clientRevision
        description: The revision of the client SDK used by your application
      - in: query
        name: consistencyToken
        description: The last-seen mutation timestamp
      responses:
        200:
          description: OK
      tags:
      - Revision
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---