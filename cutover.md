## What is cutover in Software?
A cutover plan is simply **the list of tasks** that focuses on transitioning from the old system to the new system. This should include a series of steps that must be planned, executed, and monitored to ensure successful deployment.

During production release we hear cutover sound where scrum master(or product owner) creats excel sheet which has list of steps and assigne name with time of execution. Refer here few Activities.
- **Pre-cutover (Pre prod deployment) Activities**.
  - Security and secrets configured.
  - Performance baselines established.
  - UAT Signoff.
  - Prepare rollback plan and backup current systems.
- **Cutover (Deployment Window) Activities**.
  - Deploy the Mule application
  - Apply API policies
  - Perform smoke testing: Immediately after deployment, execute a set of high-priority test cases to confirm the API endpoints are reachable, responsive, and processing key transactions correctly
  - Business sign-off for Go-Live: Obtain formal confirmation from business leads that the system is functioning as expected and transactions can resume
- **Post-cutover (post production) Activities (Hypercare)**.
  - **Monitor system stability:** Continuously monitor API performance, error rates, and traffic patterns using Anypoint Monitoring or external analytics tools (like Splunk/ELK) for the first 24-48 hours.
  - **Document lessons learned:** Create a "lessons learned" document based on the cutover experience to improve future deployments.
  - **Retire old versions (if applicable):** Once the new API is stable and functional, plan for the deprecation and eventual retirement of older API versions
