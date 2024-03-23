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


