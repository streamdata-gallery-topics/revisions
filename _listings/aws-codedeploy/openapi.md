swagger: "2.0"
x-collection-name: AWS CodeDeploy
x-complete: 1
info:
  title: AWS CodeDeploy API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=BatchGetApplicationRevisions:
    get:
      summary: Batch Get Application Revisions
      description: Gets information about one or more application revisions.
      operationId: batchGetApplicationRevisions
      x-api-path-slug: actionbatchgetapplicationrevisions-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application about which to get
          revision            information
        type: string
      - in: query
        name: revisions
        description: Information to get about the application revisions, including
          type and            location
        type: string
      responses:
        200:
          description: OK
      tags:
      - Application Revisions
  /?Action=ListApplicationRevisions:
    get:
      summary: List Application Revisions
      description: Lists information about revisions for an application.
      operationId: listApplicationRevisions
      x-api-path-slug: actionlistapplicationrevisions-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      - in: query
        name: deployed
        description: 'Whether to list revisions based on whether the revision is the
          target revision of            an deployment group:'
        type: string
      - in: query
        name: nextToken
        description: An identifier returned from the previous list application revisions
          call
        type: string
      - in: query
        name: s3Bucket
        description: An Amazon S3 bucket name to limit the search for revisions
        type: string
      - in: query
        name: s3KeyPrefix
        description: A key prefix for the set of Amazon S3 objects to limit the search
          for            revisions
        type: string
      - in: query
        name: sortBy
        description: 'The column name to use to sort the list results:'
        type: string
      - in: query
        name: sortOrder
        description: 'The order in which to sort the list results:'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Application Revisions
  /?Action=GetApplicationRevision:
    get:
      summary: Get Application Revision
      description: Gets information about an application revision.
      operationId: getApplicationRevision
      x-api-path-slug: actiongetapplicationrevision-get
      parameters:
      - in: query
        name: applicationName
        description: The name of the application that corresponds to the revision
        type: string
      - in: query
        name: revision
        description: Information about the application revision to get, including
          type and            location
        type: string
      responses:
        200:
          description: OK
      tags:
      - Application Revisions
  /?Action=RegisterApplicationRevision:
    get:
      summary: Register Application Revision
      description: Registers with AWS CodeDeploy a revision for the specified application.
      operationId: registerApplicationRevision
      x-api-path-slug: actionregisterapplicationrevision-get
      parameters:
      - in: query
        name: applicationName
        description: The name of an AWS CodeDeploy application associated with the
          applicable IAM user            or AWS account
        type: string
      - in: query
        name: description
        description: A comment about the revision
        type: string
      - in: query
        name: revision
        description: Information about the application revision to register, including
          type and            location
        type: string
      responses:
        200:
          description: OK
      tags:
      - Application Revisions