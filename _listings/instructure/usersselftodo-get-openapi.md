---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Users API List the TODO items
  description: List the todo items.
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /courses/{course_id}/todo:
    get:
      summary: Course TODO items
      description: Course todo items.
      operationId: course-todo-items
      x-api-path-slug: coursescourse-idtodo-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Todo
  /users/self/todo:
    get:
      summary: List the TODO items
      description: List the todo items.
      operationId: list-the-todo-items
      x-api-path-slug: usersselftodo-get
      responses:
        200:
          description: OK
      tags:
      - Users
      - Self
      - Todo
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