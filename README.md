# smtp-api
The Sendinblue API makes it easy for programmers to integrate many of Sendinblue's features into other applications.

# ------------------
# Create a campaign 
# ------------------
curl -H 'api-key:YOUR_API_V3_KEY' 
-X POST -d '{ 
# Define the campaign settings 
"name":"Campaign sent via the API", 
"subject":"My subject", 
"sender": { "name": "From name", "email":"name@example.com" }, 
"type": "classic", 
# Content that will be sent 
"htmlContent": "Congratulations! You successfully sent this example campaign via the Sendinblue API.", 
# Select the recipients
"recipients": { "listIds": [2,7] }, 
# Schedule the sending in one hour
"scheduledAt": "2018-01-01 00:00:01", 
}'
'https://api.sendinblue.com/v3/emailCampaigns'
