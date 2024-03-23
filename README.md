# Elastic SIEM Lab
#### [Made by Jamian Worrell with Scribe](https://scribehow.com/shared/Elastic_SIEM_Lab__PhIU-Tz8R0ScpwqTlL4AJA)


1\. 1. Navigate to the Elastic web portal at [https://cloud.elastic.co/.](https://cloud.elastic.co/)
2. Click on the menu icon on the top-left, then under “Add Integrations,”\
   Click "Add Elastic Defend"\
   Click "Install Elastic Agent"\
   Click "Copied"

![](https://colony-recorder.s3.amazonaws.com/files/2024-03-23/508c4f58-e36f-439d-8ade-2261958b2d34/stack_animation.webp)


2\. Navigate to our Kali VM and copy the Agent installation 

![](https://colony-recorder.s3.amazonaws.com/files/2024-03-23/ff8a21a5-dc74-4efb-b675-87e33a383cc8/stack_animation.webp)


3\. Agent will begin to install

![](https://colony-recorder.s3.amazonaws.com/files/2024-03-23/d1d3d3fb-aee5-4ea4-9669-adba0bba123b/stack_animation.webp)

# Endpoint Alerts
1\. Now that the agent is installed we will make some alerts on our Kali VM

We our going to scan our localhost

Using "nmap -p- localhost"

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2024-03-23/29802a7e-9cee-4929-90bc-0e2a0918f2b7/ascreenshot.jpeg?tl_px=14,432&br_px=874,913&force_format=png&width=860&wat_scale=76&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=402,212)


2\. We will now check our logs on Elastic.\
\
Inside your Elastic Deployment, click on the menu icon at the top-left with the three horizontal lines and then click on the “Logs” tab under “Observability” to view the logs from the Kali VM.

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2024-03-23/ffd9e45b-334c-448d-8302-7120178b423a/ascreenshot.jpeg?tl_px=0,0&br_px=859,480&force_format=png&width=860&wat_scale=76&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=3,40)


3\. Click here on Logs

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2024-03-23/b77ead5d-e99e-4e67-a7d3-61ecea124520/ascreenshot.jpeg?tl_px=0,599&br_px=859,1080&force_format=png&width=860&wat_scale=76&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=4,315)


4\. In the search bar, enter a search query to filter the logs. For example, to search for all logs related to Nmap scans, enter the query: event.action: “nmap_scan” or process.args: “sudo”.

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2024-03-23/809252f2-bfdb-4e87-a917-e509140f7473/ascreenshot.jpeg?tl_px=387,0&br_px=1247,480&force_format=png&width=860&wat_scale=76&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=402,193)


5\. We will click on view details and scroll and see our nmap scan is there.

![](https://colony-recorder.s3.amazonaws.com/files/2024-03-23/349f483c-b127-40fa-952b-c6c2b183f56a/stack_animation.webp)
#### [Made with Scribe](https://scribehow.com/shared/Navigate_using_clicks_searches_filters_and_key_presses__BoUNWnp4RcWWJn-_cAYp5w)

# Creating SIEM Dashboard
1\. We will now be creating a dashboard to better visualize the information being sent our endpoint VM.


2\. 1. Navigate to the Elastic web portal at [https://cloud.elastic.co/.](https://cloud.elastic.co/)
2. Click on the menu icon on the top-left, then under “Analytics,” click on “Dashboards.”
3. Then create Dashboard

![](https://colony-recorder.s3.amazonaws.com/files/2024-03-23/4298b58c-af59-4d68-9698-37f3171a8cd9/stack_animation.webp)


3\. Click "Bar vertical stacked"\
Click here and search for Area.

![](https://colony-recorder.s3.amazonaws.com/files/2024-03-23/8d17e2fa-99c9-4013-ab58-ba18d4e2a586/stack_animation.webp)


4\. Click "Add or drag-and-drop a field to Horizontal axis"

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2024-03-23/1a3486fc-1c8b-4dcc-a4dd-fda1265e8bd0/ascreenshot.jpeg?tl_px=1060,97&br_px=1920,578&force_format=png&width=860&wat_scale=76&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=480,212)


5\. Click here and select timestamp

![](https://colony-recorder.s3.amazonaws.com/files/2024-03-23/22bb98b3-9218-4308-8a5f-78511d1b4154/stack_animation.webp)


6\. Click here

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2024-03-23/4f7d181e-c3eb-4f18-9573-635b70d24776/ascreenshot.jpeg?tl_px=1060,0&br_px=1920,480&force_format=png&width=860&wat_scale=76&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=806,160)


7\. Click "Add or drag-and-drop a field to Vertical axis"

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2024-03-23/e934b803-b484-45ca-80ce-0704cb64b1b7/ascreenshot.jpeg?tl_px=1060,186&br_px=1920,667&force_format=png&width=860&wat_scale=76&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=554,212)


8\. Click "Count"

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2024-03-23/79dcc6d5-c9d7-4856-927f-fafe32cf9417/ascreenshot.jpeg?tl_px=1060,153&br_px=1920,634&force_format=png&width=860&wat_scale=76&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=448,212)


9\. Click here

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2024-03-23/902cf6b8-ed26-4307-a3b6-8d7fabc51891/ascreenshot.jpeg?tl_px=1060,599&br_px=1920,1080&force_format=png&width=860&wat_scale=76&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=458,430)


10\. Click here to save our newly created Dashboard.

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2024-03-23/6d855d69-facf-42f4-85a9-7a8f56f09958/ascreenshot.jpeg?tl_px=1060,0&br_px=1920,480&force_format=png&width=860&wat_scale=76&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=715,47)


11\. We our going to do another scan on our endpoint

nmap -sS localhost

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2024-03-23/49b9d8b2-ca94-448f-80eb-bb44ccaec810/ascreenshot.jpeg?tl_px=157,443&br_px=1016,924&force_format=png&width=860&wat_scale=76&wat=1&wat_opacity=0.7&wat_gravity=northwest&wat_url=https://colony-recorder.s3.us-west-1.amazonaws.com/images/watermarks/FB923C_standard.png&wat_pad=402,212)


12\. This will be how our dashboard looks.

We can further customize our dashboards. This is just an example for this lab. 

![](https://ajeuwbhvhr.cloudimg.io/colony-recorder.s3.amazonaws.com/files/2024-03-23/fc82843a-978c-4e94-a78b-dabb891da88b/screenshot.jpeg?tl_px=40,0&br_px=900,409&force_format=png&width=860)
#### [Made with Scribe](https://scribehow.com/shared/Creating_SIEM_Dashboard__KdFhU8hvRLWAK7a8-NQVJQ)



