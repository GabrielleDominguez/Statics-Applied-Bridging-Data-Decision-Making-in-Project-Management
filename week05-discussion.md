# Week 5 Discussion: Using Hypothesis Testing to Make Smarter Project Decisions

> *This discussion shows how hypothesis testing helps validate project outcomes with data, improving decision-making and proving real business impact.*

---

## **Discussion Topic**
#### Describe the steps in hypothesis testing and discuss the differences between testing a population mean and a population proportion. Use an example for each and explain how results are interpreted. Cite your sources.

---

In project management, **hypothesis testing** could provide a structured approach for validating project outcomes and promoting data-driven decisions. The process involves five steps: stating your **null and alternative hypotheses**, selecting a significance level (typically *0.05*), choosing the appropriate test statistic, calculating the **P-value**, and making a decision based on the results (Triola, 2020).

When selecting what method to use, I need to factor in the type of data I have available to me. If I was measuring success rates, compliance percentages, or other yes/no outcomes, I would use **proportion tests with z-statistics**. When measuring performance metrics, think response times or processing speeds, I'd use **mean tests with t-statistics**.

For a lot of project managers, project success is often measured by completion rates. Hypothesis testing would allow me to shift the focus to actual performance improvements with statistical evidence.

**Proportion Example:**  
Testing if cybersecurity training increases compliance above our 60% baseline.  
H₀: p ≤ 0.60 vs H₁: p > 0.60. After training 200 employees, 138 comply (69%). Using z-test, P-value = 0.015. Since 0.015 < 0.05, **I reject H₀**: the data shows that the training initiatives have significantly improved company compliance.

**Mean Example:**  
Testing if server upgrades reduce response times from 4.2 seconds.  
H₀: μ = 4.2 vs H₁: μ < 4.2. Measuring 35 post-upgrade responses with mean = 3.7 seconds. Using t-test, P-value = 0.008. Since 0.008 < 0.05, **I reject H₀**: the data shows that the server upgrades have significantly reduced the standard response times.

This statistical approach would help me move beyond basic project metrics and demonstrate to key leadership how their IT investments are delivering real, measurable business results.

---

> **Reply from Alexis Martin:**  
> Hi Gabrielle, you did a great job of determining whether hypothesis testing could support better decision-making in project management.
> 
> I like how you used clear examples for both proportion and mean, like checking if training increases compliance or if upgrades reduce response times. It really shows how statistics can help you prove whether the changes made a difference. I also love how you think beyond just statistics and how the data can show real value and importance. I am wondering, when looking at all these projects, how do you determine which performance metrics are worth testing?

> **Response from Gabrielle Dominguez:**  
> Thank you, Alexis, for your kind words and great question. **Determining which performance metrics are worth testing** is indeed a crucial consideration.  
>  
> When managing projects, I go back to the **'why' behind the project** we are working to complete. **What is the goal?** For example, if I am working on migrating an internal database to a new platform, the metric may be how many people are adopting the new system and using it in real time, instead of hesitating because they do not like change. In this case, I would test the **adoption rate** of the platform. I already know the migration was successful, but this gives me a new lens to look through: **how easy is it to use for an early adopter?**
> 
> Some projects are more nuanced than this, these are when they are opinion-based and there is no clear metric to measure. An example of this would be client satisfaction with a product or service. There is no inherent metric to measure satisfaction because **satisfaction is their measurement**. This is why many companies send surveys to try and put words or metrics to feelings.  
>  
> For example, you go to a restaurant and they send you a survey asking about your food, server, and experience. They could gather this data by using a **1–5 rating system** and put data to what was once only a feeling.
>  
> Great question again, and I am looking forward to continuing to learn alongside you for the remainder of the semester.

---

> **Reply from Hannah Blake:**  
> I also thought your point about focusing on performance improvements instead of just completion rates was really smart. Have you ever had a situation where the data didn’t support what was expected? It’d be interesting to see how hypothesis testing could guide next steps in that case.  
> Thanks for sharing such a thoughtful perspective!

> **Response from Gabrielle Dominguez:**  
> Hi Hannah! This is a great question on what to do when you run into unexpected results - which happens more frequently than you would think. I haven't used hypothesis testing in practice yet, but I can explain to you how valuable it could be on a situational basis.  
>  
> For example, I worked on a software upgrade project where we expected to improve performance based on historical data (past patterns), but the results were disappointing. If we had used hypothesis testing from the start, we could have set clear performance benchmarks and determined whether the upgrade actually failed to meet expectations or if other factors were at play.  
>  
> The structured approach really does seem like it would prevent jumping to conclusions and help with better decision-making when reality doesn't match expectations.  
>  
> How do you think you'll apply hypothesis testing in your future career field? Maybe it will be of similar nature to the work I do!
> Hi Gabrielle, great post! I really liked how you connected hypothesis testing to project management—it made the topic feel much more real-world and applicable. Your examples were super clear, especially the one about measuring compliance after cybersecurity training.
> 

---

## Z Test and T Test Visuals

<div style="text-align: center;">
  <a href="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/main/z%20%20test%20final.png?raw=true" target="_blank" rel="noopener">
    <img 
      src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/main/z%20%20test%20final.png?raw=true" 
      alt="Z Test Visual Final" 
      width="720" 
      style="margin-bottom: 40px;" 
    />
  </a>
  <br />
  <a href="https://raw.githubusercontent.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/c036336eb9f646fa3d1c747a894f8b80e8251d69/t%20test%20final.png" target="_blank" rel="noopener">
    <img 
      src="https://raw.githubusercontent.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/c036336eb9f646fa3d1c747a894f8b80e8251d69/t%20test%20final.png" 
      alt="T Test Visual Final" 
      width="720" 
    />
  </a>
</div>

---




---
## References

Triola, M. F. (2022). *Elementary statistics* (13th ed.). Pearson.  
Pearson Education. (2022). *Elementary statistics* course materials.

---

[← Back to Home](https://gabrielledominguez.github.io/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/)

