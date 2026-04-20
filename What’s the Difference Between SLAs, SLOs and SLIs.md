# What’s the Difference Between SLAs, SLOs and SLIs?

- Every tech company providing a service, whether it be free or paid, shares one similar objective: Deliver the best possible experience in order to attract and retain users. After all, without the users there is no reason (or money for that matter) for the service to exist.
- When using a service, you want to be able to trust it will perform as promised. If Google suddenly became notorious for outages and slowdowns we’d likely see a mass exodus of users looking for a new search engine. Yet because of Google’s ability to consistently meet user expectations and deliver (at least) 99.99% uptime month-after-month, the search engine giant continues to dominate with over 70,000 searches every second.
- Maintaining these high uptime percentages isn’t just something Google “shoots for” every month because it looks good. Their Monthly Uptime Percentage is a key indicator that is measured in order to determine whether or not they’re delivering on the promises made to their users – in this case, a search engine that works as planned 99.99% of the time.
- These different promises or agreements that tech companies make with their customers are often defined within a Service Level Agreement (SLA). These SLAs consist of different Service Level Objectives (SLO) that are tracked and monitored by measuring specific Service Level Indicators (SLI).
- Companies define, track, and monitor these SLAs, SLOs and SLIs with the goal of creating a more reliable service for their customers. But what exactly do these terms mean and how do they relate to one another?

1. #### What is a SLA?

   - **SLA: Service Level Agreement (The Contract)**

   - **Service Level Agreement**, is an agreement made between a company and its users of a given service. The SLA defines the different promises that the company makes to users regarding specific metrics, such as service availability. For example, Google’s SLA from our example earlier promises the user a Monthly Uptime Percentage of no less least 99.99%.
   - The SLA is a **formal contract** between a service provider and a customer. It specifies the promised service levels and the **consequences** (like financial credits or refunds) if those levels are not met. 
     - **Purpose:** To formalize business commitments and protect both parties legally.
     - **Important Practice:** Most teams set SLOs **stricter** than SLAs (e.g., a 99.9% internal SLO but a 99.5% external SLA) to provide a safety buffer for catching issues before they trigger legal penalties.
   - **SLA Challenges.** Unfortunately SLAs are often written by a company’s business or legal team with little to no input from the tech team. Without involving tech in the writing process, an SLA can end up leaving out important aspects and be extremely difficult to measure.
   - **When to use SLAs:** SLAs are made between vendors (company providing the service) and paid users. Free-to-use services do not need an SLA.

2. #### **What is SLO?**

   - **SLO: Service Level Objective (The Internal Goal or The Target)**

   - Service Level Objective, is the promise that a company makes to users regarding a specific metric such as incident response or uptime. SLOs exist within an SLA as individual promises contained within the full user agreement.
   - The SLO is a **target value** or range for an SLI over a specific period (e.g., 30 days). It is an internal benchmark used by engineering teams to determine if a service is "reliable enough".
     - **Purpose:** To guide internal decision-making and balance reliability with innovation.
     - **Key Concept:** **Error Budgets.** The difference between 100% and your SLO (e.g., 0.1% if your SLO is 99.9%) is the amount of downtime you can "afford" before you must stop shipping features and focus on reliability.
   - **SLO Challenges.** A common challenge with SLOs is when they are too vague, complicated, or immeasurable. SLOs should always be simple, clearly defined, easily measured to determine whether or not the objective is being fulfilled. This will also keep your engineers from hitting roadblocks when something doesn’t make sense.
   - **When to use SLOs.** SLOs can be useful for both paid and free-to-use services as they can help companies improve the overall quality and reliability of their service.

   ### SLAs vs. SLOs: What’s the Difference?

   - SLAs are used externally to define an agreement between a company’s service and its paid users.
   - SLOs are objectives that are measured internally to determine whether the SLA is being met.
   - If an SLO’s terms are violated, teams must respond and react quickly to prevent from breaking the SLA.
   - These SLOs are measured by closely monitoring key Service Level Indicators (SLIs).

3. #### What is SLI?

   - **SLI: Service Level Indicator (The Metric)**

   - **Service Level Indicator**, is a key metric used to determine whether or not the SLO is being met. It is the measured value of the metric described within the SLO. For example, where Google’s SLO is 99.99%, the SLI is the actual measured value at the time. In order to remain in compliance with the SLA, the SLI’s value must always meet or exceed the value determined by the SLO.
   - The SLI is the **raw data** that tells you how your service is performing right now. It measures specific aspects of a service, such as latency, availability, or error rates.
     - **Purpose:** To provide a quantitative signal of service health.
     - **Examples:** Average request latency, success rate of login attempts, or the percentage of 200 OK responses. 
   - **SLI Challenges.** To prevent overcomplicating things, it’s important to keep things simple and choose the right key metrics to monitor. Tracking too many metrics will just make for more work that makes little difference to the user.
   - **When to Use SLIs.** SLIs are essential for monitoring how effectively a service is meeting SLOs. Without them, there’s no way of accurately measuring performance.

### Why SLAs, SLOs, and SLIs are Important

- SLAs, SLOs, and SLIs allow companies to define, track, and monitor the promises made for a service to its users. Together, SLAs, SLOs, and SLIs should help teams generate more user trust in their services with an added emphasis on continuous improvement to incident management and response processes.