# JSON-Placeholder-API-Test

## Assumptions
-	Data that can be extracted from the API is in the correct format and should not accept different data types
-	Some data fields should only be able to accept data that exists in the system (e.g. a user that doesn’t exist in the system should not be able to leave comments / posts)

## Limitations of API
-	Data cannot be amended (e.g. Added, Deleted, Updated) the API just acts as if it is
	- This prevents user from manipulating data in one call and using in a second call

## Tests Executed

All Tests were desgined and implemented using Postman and can be found using the link [![Run in Postman](https://run.pstmn.io/button.svg)](https://god.postman.co/run-collection/a51bcc4da498ca0c4dd8#?env%5BPosts-User%5D=W3sia2V5IjoidXNlcmVtYWlsIiwidmFsdWUiOiIiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6InVzZXJJZCIsInZhbHVlIjoiIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJwb3N0SWQiLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoicG9zdFRpdGxlIiwidmFsdWUiOiIiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6InBvc3RCb2R5IiwidmFsdWUiOiIiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6Im51bWJlck9mUG9zdHMiLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoidXNlcklkVHlwZSIsInZhbHVlIjoiIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJudW1iZXJPZlVzZXJzIiwidmFsdWUiOiIiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6Im51bWJlck9mVXNlcnMrMSIsInZhbHVlIjoiIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJudW1iZXJPZlBvc3RzQnlVc2VyIiwidmFsdWUiOiIiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6Im51bWJlck9mQ29tbWVudHMiLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiY29tbWVudFBvc3RJZFR5cGUiLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiY29tbWVudElkVHlwZSIsInZhbHVlIjoiIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJjb21tZW50TmFtZVR5cGUiLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiY29tbWVudEVtYWlsVHlwZSIsInZhbHVlIjoiIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJjb21tZW50Qm9keVR5cGUiLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoibnVtYmVyT2ZDb21tZW50c09uUG9zdCIsInZhbHVlIjoiIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJudW1iZXJPZkNvbW1lbnRzUGx1czEiLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiY29tbWVudFBvc3RJZCIsInZhbHVlIjoiIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJjb21tZW50SWQiLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiY29tbWVudE5hbWUiLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiY29tbWVudEVtYWlsIiwidmFsdWUiOiIiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6ImNvbW1lbnRCb2R5IiwidmFsdWUiOiIiLCJlbmFibGVkIjp0cnVlfV0=)

Tests have also uploaded into the project.

### /Posts – Basic
Confirm user is able to:
-	GET data from the Posts
-	POST data to Posts
-	PUT / PATCH data to Posts
-	DELETE data from Posts
-	Filter /Posts
### /Posts – Advanced
Confirm:
-	A Specific Post in present in the full /Posts
-	Data entered into a Post is restricted
-	A newly created post has an expected post ID
### /Posts/1/comments – Basic
Confirm user is able to:
-	GET data from the Posts/1/Comments
-	POST data to /Comments
- PATCH data in a Comment
- DELETE a Comment
- Filter Comments
### /Posts/1/comments – Advanced
Confirm:
- A Newly Created Comment has expected Post ID
- The Correct number of comments are displayed on /posts/1/comments
## Findings
-	Basic functionality can be applied to /posts and posts/1/comments
- No restrictions have been implemented around data type
## Recommendations
-	Not suitable to be promoted to production due to following failures:
	-	Incorrect Data Format can be used to create Posts and Comments
	-	Users not present in the system can create posts

