# GCP Practice Questions

### [Take a look to guide to add questions](Guide_to_add_questions.md)


**1. Que:** You support a Node.js application running on Google Kubernetes Engine (GKE) in production. The application makes several HTTP requests to dependent applications. You want to anticipate which dependent applications might cause performance issues.

<details><summary><strong>What should you do? </strong></summary>

- [ ] Instrument all applications with Stackdriver Profiler.
- [x] Instrument all applications with Stackdriver Trace and review inter-service HTTP requests.
- [ ] Use Stackdriver Debugger to review the execution of logic within each application to instrument all applications.
- [ ] Modify the Node.js application to log HTTP request and response times to dependent applications. Use Stackdriver Logging to find dependent applications that are performing poorly.

</details>

---

**2. Que:** (SRE) team only. You want to ensure you follow the principle of least privilege.

<details><summary><strong>What should you do?</strong></summary>

- [x] Share the workspace Project ID with the SRE team. Assign the SRE team the Monitoring Viewer IAM role in the workspace project.
- [ ] Share the workspace Project ID with the SRE team. Assign the SRE team the Dashboard Viewer IAM role in the workspace project.
- [ ] Share chart by URL  and provide the URL to the SRE team. Assign the SRE team the Monitoring Viewer IAM role in the workspace project.
- [ ] Share chart by URL and provide the URL to the SRE team. Assign the SRE team the Dashboard Viewer IAM role in the workspace project.

</details>

---

**3. Que:** Your organization wants to implement Site Reliability Engineering (SRE) culture and principles. Recently, a service that you support had a limited outage. A manager on another team asks you to provide a formal explanation of what happened so they can action remediations. 

<details><summary><strong> What should you do? </strong></summary>

- [ ] Develop a postmortem that includes the root causes, resolution, lessons learned, and a prioritized list of action items. Share it with the manager only.
- [x] Develop a postmortem that includes the root causes, resolution, lessons learned, and a prioritized list of action items. Share it on the engineering organization's document portal.

- [ ]  Develop a postmortem that includes the root causes, resolution, lessons learned, the list of people responsible, and a list of action items for each person. Share it with the manager only
- [ ] Develop a postmortem that includes the root causes, resolution, lessons learned, the list of people responsible, and a list of action items for each person. Share it on the engineering organization's document portal.

</details>

---

**4. Que:** You have a set of applications running on a Google Kubernetes Engine (GKE) cluster, and you are using Stackdriver Kubernetes Engine Monitoring. You are bringing a new containerized application required by your company into production. This application is written by a third party and cannot be modified or reconfigured. The application writes its log information to /var/log/app_messages.log, and you want to send these log entries to Stackdriver Logging. 
<details><summary><strong> What should you do? </strong></summary>

- [ ] Use the default Stackdriver Kubernetes Engine Monitoring agent configuration.
- [x] Deploy a Fluentd daemonset to GKE. Then create a customized input and output      configration to tail the log file in the application's pods and write to Stackdriver Logging.
- [ ] Install Kubernetes on Google Compute Engine (GCE) and redeploy your applications. Then customize the built-in Stackdriver Logging configuration to tail the log file in the application's pods and write to Stackdriver Logging.
- [ ] Write a script to tail the log file within the pod and write entries to standard output. Run the script as a sidecar container with the application's pod. Configure a shared volume between the containers to allow the script to have read access to /var/log in the application container.


</details>

Reference links or explanation: https://cloud.google.com/solutions/customizing-stackdriver-logs-fluentd

---

**5. Que:** You are running an application in a virtual machine (VM) using a custom Debian image. The image has the Stackdriver Logging agent installed. The VM has the cloud-platform scope. The application is logging information via syslog. You want to use Stackdriver Logging in the Google Cloud Platform Console to visualize the logs. You notice that syslog is not showing up in the "All logs" dropdown list of the Logs Viewer. 

<details><summary><strong> What is the first thing you should do? </strong></summary>

- [ ] Look for the agent’s test log entry in the Logs Viewer.
- [ ] Install the most recent version of the Stackdriver agent.
- [ ] Verify the VM service account access scope includes the monitoring.write scope.
- [x] SSH to the VM and execute the following commands on your VM: ps ax | grep fluentd.


</details>

Reference links or explanation: https://groups.google.com/g/google-stackdriver-discussion/c/FXehB9a-5Vk?pli=1

---

**6. Que:** You use Spinnaker to deploy your application and have created a canary deployment stage in the pipeline. Your application has an in-memory cache that loads objects at start time. You want to automate the comparison of the canary version against the production version.

<details><summary><strong> How should you configure the canary analysis? </strong></summary>

- [ ] Compare the canary with a new deployment of the current production version
- [ ] Compare the canary with a new deployment of the previous production version
- [ ] Compare the canary with the existing deployment of the current production version.
- [x] Compare the canary with the average performance of a sliding window of previous production versions.

</details>

Reference links or explanation: https://cloud.google.com/solutions/automated-canary-analysis-kubernetes-engine-spinnaker

---

**7. Que:** You support a high-traffic web application and want to ensure that the home page loads in a timely manner. As a first step, you decide to implement a Service Level Indicator (SLI) to represent home page request latency with an acceptable page load time set to 100 ms.

<details><summary><strong> What is the Google-recommended way of calculating this SLI?
 </strong></summary>

- [ ] Bucketize the request latencies into ranges, and then compute the percentile at 100 ms.
- [ ] Bucketize the request latencies into ranges, and then compute the median and 90th percentiles.
- [x] Count the number of home page requests that load in under 100 ms, and then divide by the total number of home page requests.
- [ ] Count the number of home page request that load in under 100 ms, and then divide by the total number of all web application requests.

</details>

Reference links or explanation: https://sre.google/workbook/implementing-slos/


---

**8. Que:** You support the backend of a mobile phone game that runs on a Google Kubernetes Engine (GKE) cluster. The application is serving HTTP requests from users. You need to implement a solution that will reduce the network cost.

<details><summary><strong> What should you do? </strong></summary>

- [ ] Configure the VPC as a Shared VPC Host project.
- [ ] Configure your network services on the Standard Tier.
- [x] Configure your Kubernetes cluster as a Private Cluster.
- [ ] Configure a Google Cloud HTTP Load Balancer as Ingress.


</details>

Reference links or explanation: Configure a Google Cloud HTTP Load Balancer as Ingress.

---

**9. Que:** You are managing the production deployment to a set of Google Kubernetes Engine (GKE) clusters. You want to make sure only images which are successfully built by your trusted CI/CD pipeline are deployed to production.

<details><summary><strong> What should you do? </strong></summary>

- [ ] Enable Cloud Security Scanner on the clusters.
- [x] Enable Vulnerability Analysis on the Container Registry.
- [ ] Set up the Kubernetes Engine clusters as private clusters.
- [ ] Set up the Kubernetes Engine clusters with Binary Authorization.

</details>

Reference links or explanation: https://codelabs.developers.google.com/codelabs/cloud-builder-gke-continuous-deploy/index.html#1


---

**10. Que:** You deploy a new release of an internal application during a weekend maintenance window when there is minimal user tragic. After the window ends, you learn that one of the new features isn't working as expected in the production environment. After an extended outage, you roll back the new release and deploy a fix. You want to modify your release process to reduce the mean time to recovery so you can avoid extended outages in the future.

<details><summary><strong> What should you do? (Choose two.) </strong></summary>

- [x] Before merging new code, require 2 different peers to review the code changes.
- [ ] Adopt the blue/green deployment strategy when releasing new code via a CD server.
- [x] Integrate a code linting tool to validate coding standards before any code is accepted into the repository.
- [ ] Require developers to run automated integration tests on their local development environments before release.
- [ ] Configure a CI server. Add a suite of unit tests to your code and have your CI server run them on commit and verify any changes.

</details>
