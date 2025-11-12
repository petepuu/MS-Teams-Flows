# Create Power Automate Flow for notifications sent by external system to Microsoft Teams channels/group chat


1. Open Power Automate portal https://make.microsoft.com/
   
   ![1-Power Automate](images/portal.png "Open make.powerautomate.com portal")

    <br>

2. Select the target environment using the environment picker (top-right).
   
   ![2-Environment picker](images/env.png "Environment picker — select target environment")

   <br>

3. Click **+ Create** and select **Instant cloud flow**
   
   ![3-Create instant flow](images/create-instant-flow.png "Create instant flow")

   <br>

4. Provide **Flow name**, scroll down and select the **When a Teams webhook request is received** trigger and then click **Create**
   
   ![4-Instant flow](images/instant-flow.png "Instant flow")

   <br>

5. Configure the trigger by selecting **When a Teams webhook request is received** and define who should be able to trigger the flow 
   - **Anyone** = Anonymous
   - **Any user in my tenant** = All users of Microsoft 365 tenant
   - **Specific users in my tenant** = User of same Microsoft 365 tenant you define. List of email addresses
  
      ![5-Configure trigger](images/conf-trigger.png "Configure trigger")

      <br>

6. Add new action by clicking **(+)** under the flow trigger
   
   ![6-Configure trigger](images/new-action.png "Configure trigger")

   <br>

7. Search and select **Post a message in a chat or channel** action
   
   ![7-Add post a message action](images/add-post-message-action.png "Post a message action")

   <br>

8. Select do you want to post a message either as **Flow bot** or **User**
   
   ![8-Post message as](images/post-msg-as.png "Select flow bot of user")

   <br>

   - If you select **Flow bot**, then message will show like below in Teams channel
  
      ![8-Flow bot](images/flowbot-sample.png "Flow bot")

      <br>
   
   - When using User option then messages are seen similarly if user posted message to channel in Microsoft Teams
  
      ![8-User](images/user-sample.png "User")

      <br>

9. Select do you want to post a message to either **Channel** or **Group chat**
    
   ![9-Post message in](images/post-msg-in.png "Select channel or group chat")

   <br>

10. Define team and channel or group chat depending which option you selected in the previous step
    
       - **Team and Channel**

          ![10-Team and channel](images/post-team-channel.png "Select team and channel")

          <br>

       - **Group chat**

          ![10-Group chat](images/post-group-chat.png "Select group chat")

          <br>

11. Type-in message and if you want you can also set subject (only available when posting as User) for the message
    
    ![11-Message and subject](images/post-msgs-message.png "Message")

    <br>

    ![11-Subject](images/post-msgs-subject.png "Subject")

    <br>

12. Publish the flow
    
    ![12-Publish flow](images/publish.png "Publish flow")

    <br>

13. Select the flow trigger and copy **HTTP URL** generated for the flow. This URL can be used to call (run) the flow e.g. from external system

    ![13-Copy trigger URL](images/copy-webhook-url.png "Publish flow")

    <br> 