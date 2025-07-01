# Week 1 Discussion: Using Data Types & Graphs to Uncover Meaningful Project Insights

> *This discussion explores how different types of data can be used to analyze project management tools and their impact on project success, demonstrating the use of nominal and ratio data with appropriate graphical methods.*

---

## **Discussion Topic**

#### Choose a dataset that includes at least two types of data (e.g., nominal and interval). Describe the types of data and explain which graphical methods (such as frequency distribution tables or histograms) are most suitable to represent them. Justify your answer using course materials or a credible source.

---

For this discussion, I chose a hypothetical dataset that looks at how different project management tools impact project success. I chose this concept because it ties into my business administration major, my minor in business analytics, and my experience as a project manager.

The dataset has two main types of data:

**Project Management Tracking Platforms (Nominal data)**  
The first form of data observes popular project tracking tools like **MS Project, Asana, Jira, and Trello.** It's nominal data because these are distinct categories without any rankings. As our textbook explains, nominal data consists of names or labels and they *can’t* be logically ordered.

To graph the rate of adoption across tracking platforms, I would use a **bar graph**. This would display the *quantity of projects* monitored on each platform and compare them visually at a glance.

**Project Success Rate (Ratio data)**  
Building off the first, the second data set shows what percentage of project milestones teams finished on time (ranging from 0% to 100%). It's ratio data because it has equal intervals and a true zero point—0% means no milestones were completed on time.

I would use a **histogram** to display the success rates. This graph would display how the distribution of success rates is viewed among projects. In addition to showing the adoption of individual tools, we can now also group projects by *success rate ranges* (like 0–20%, 21–40%, etc.)

This kind of analysis would help answer whether using a project management platform actually improves on-time task completion and gives insight into which platforms are more widely adopted or easier to implement. This would be valuable information for any business to have access to when deciding what software is *worth* their invest of time and money.

From the course content, we learned that statistics helps us *"describe data, make inferences, and support decisions under uncertainty"* (Pearson Education, 2022). This analysis supports that idea well because of the measurement of project outcomes and the use of data to explore which tools may contribute most to team success.

---

## Graph Visualizations

<style>
  table.graph-table {
    border-collapse: separate;
    border-spacing: 24px;
    margin: 0 auto;
  }

  table.graph-table td {
    width: 50%;
    padding: 0;
    vertical-align: top;
  }

  .img-wrapper {
    position: relative;
    border: 1.25px solid #ddd;
    background-color: white;
    overflow: hidden;
    box-sizing: border-box;
    cursor: pointer;
  }

  .img-wrapper::before,
  .img-wrapper::after {
    content: "";
    position: absolute;
    width: 10px;
    height: 10px;
    background-color: white;
    z-index: 2;
  }

  .img-wrapper::before {
    top: 0;
    left: 0;
    border-top: 1.25px solid #ddd;
    border-left: 1.25px solid #ddd;
    transform: translate(-50%, -50%);
  }

  .img-wrapper::after {
    bottom: 0;
    right: 0;
    border-bottom: 1.25px solid #ddd;
    border-right: 1.25px solid #ddd;
    transform: translate(50%, 50%);
  }

  .img-wrapper img {
    display: block;
    width: 100%;
    height: auto;
  }

  .zoom-plus {
    position: absolute;
    top: 8px;
    right: 8px;
    font-size: 16px;
    color: rgba(0, 0, 0, 0.3);
    pointer-events: none;
    user-select: none;
  }

  .img-wrapper:hover .zoom-plus {
    color: rgba(0, 0, 0, 0.6);
  }
</style>

<div align="center">
  <table class="graph-table">
    <tr>
      <td>
        <div class="img-wrapper">
          <img src="https://raw.githubusercontent.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/main/Screenshot%202025-06-23%20104128.png" alt="Graph 1" class="zoomable" />
          <div class="zoom-plus">+</div>
        </div>
      </td>
      <td>
        <div class="img-wrapper">
          <img src="https://raw.githubusercontent.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/main/Screenshot%202025-06-23%20104113.png" alt="Graph 2" class="zoomable" />
          <div class="zoom-plus">+</div>
        </div>
      </td>
    </tr>
  </table>
</div>

---

## References

Triola, M. F. (2022). *Elementary statistics* (13th ed.). Pearson.  
Pearson Education. (2022). *Elementary statistics* course materials.

---
[← Back to Home](https://gabrielledominguez.github.io/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/)


