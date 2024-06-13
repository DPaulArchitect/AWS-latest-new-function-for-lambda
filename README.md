Description: |
  This microservice does two things, fetches the most recent 10 Blog posts, using Amazon EventBridge on a daily schedule, from the 'AWS Latest News' RSS feed and
  adds then into a DynamoDB table. The second aspect of this microservice populates your web page with the 10 most recently added 
  blog posts from DynamoDB using Lambda fronted by a function URL which sits on your application servers 

  - Dynamodb table for stories and links
  - Lambda function which grabs stories from the RSS feed
  - Eventbridge rule which runs daily triggering the function
  - Lambda function which is triggered by a function URL whenever your page is refreshed, grabbing the latest stories and displaying them on your webpage.
