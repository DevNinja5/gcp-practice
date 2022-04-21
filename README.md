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

