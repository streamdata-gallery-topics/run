---
swagger: "2.0"
x-collection-name: AWS Device Farm
x-complete: 0
info:
  title: AWS Device Farm API List Runs
  version: 1.0.0
  description: Gets information about runs, given an AWS Device Farm project ARN.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DeleteRun:
    get:
      summary: Delete Run
      description: Deletes the run, given the run ARN.
      operationId: deleteRun
      x-api-path-slug: actiondeleterun-get
      parameters:
      - in: query
        name: arn
        description: The Amazon Resource Name (ARN) for the run you wish to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Runs
  /?Action=GetRun:
    get:
      summary: Get Run
      description: Gets information about a run.
      operationId: getRun
      x-api-path-slug: actiongetrun-get
      parameters:
      - in: query
        name: arn
        description: The runs ARN
        type: string
      responses:
        200:
          description: OK
      tags:
      - Runs
  /?Action=ListRuns:
    get:
      summary: List Runs
      description: Gets information about runs, given an AWS Device Farm project ARN.
      operationId: listRuns
      x-api-path-slug: actionlistruns-get
      parameters:
      - in: query
        name: arn
        description: The Amazon Resource Name (ARN) of the project for which you want
          to list runs
        type: string
      - in: query
        name: nextToken
        description: An identifier that was returned from the previous call to this
          operation, which can be used to return the next set of items in the list
        type: string
      responses:
        200:
          description: OK
      tags:
      - Runs
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