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

## Forecasting Visualizations

<style>
  .image-row {
    display: flex;
    gap: 12px;
    justify-content: space-between;
    flex-wrap: nowrap;
  }

  .img-container {
    position: relative;
    flex: 1 1 0;
    max-width: none;
  }

  .img-container img {
    display: block;
    width: 100%;
    height: auto;
    cursor: pointer;
    border-radius: 4px;
  }

  .zoom-plus {
    position: absolute;
    top: 4px;
    right: 4px;
    font-weight: normal;
    font-size: 14px;
    color: rgba(0, 0, 0, 0.4);
    background: transparent;
    padding: 0;
    user-select: none;
    pointer-events: none;
    transition: color 0.3s ease;
  }

  .img-container:hover .zoom-plus {
    color: rgba(0, 0, 0, 0.7);
  }

  .modal {
    display: none;
    position: fixed;
    z-index: 1000;
    left: 0;
    top: 0;
    width: 100vw;
    height: 100vh;
    background: rgba(0,0,0,0.8);
    justify-content: center;
    align-items: center;
  }

  .modal.active {
    display: flex;
  }

  .modal img {
    max-width: 90%;
    max-height: 90%;
    box-shadow: 0 0 15px rgba(0,0,0,0.5);
    border-radius: 8px;
  }

  .modal-close {
    position: fixed;
    top: 20px;
    right: 30px;
    color: white;
    font-size: 30px;
    font-weight: bold;
    cursor: pointer;
    user-select: none;
  }
</style>

<div class="image-row">
  <div class="img-container">
    <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/93f32c8b2ecd9146c1ce521b00630e13e77c3d53/Article%204%2C%20image%201%2C%20resize%20v2.png?raw=true" alt="Forecasting Image 1" class="zoomable" />
    <div class="zoom-plus" aria-hidden="true">+</div>
  </div>

  <div class="img-container">
    <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/93f32c8b2ecd9146c1ce521b00630e13e77c3d53/Article%204%2C%20image%202%2C%20resize%20v2.png?raw=true" alt="Forecasting Image 2" class="zoomable" />
    <div class="zoom-plus" aria-hidden="true">+</div>
  </div>
</div>

<!-- Modal -->
<div id="modal" class="modal" role="dialog" aria-modal="true">
  <span id="modal-close" class="modal-close" aria-label="Close modal">&times;</span>
  <img src="" alt="" id="modal-img" />
</div>

<script>
  const zoomables = document.querySelectorAll('.zoomable');
  const modal = document.getElementById('modal');
  const modalImg = document.getElementById('modal-img');
  const modalClose = document.getElementById('modal-close');

  zoomables.forEach(img => {
    img.addEventListener('click', () => {
      modal.classList.add('active');
      modalImg.src = img.src;
      modalImg.alt = img.alt;
    });
  });

  modalClose.addEventListener('click', () => {
    modal.classList.remove('active');
    modalImg.src = '';
  });

  modal.addEventListener('click', (e) => {
    if (e.target === modal) {
      modal.classList.remove('active');
      modalImg.src = '';
    }
  });

  document.addEventListener('keydown', (e) => {
    if (e.key === "Escape" && modal.classList.contains('active')) {
      modal.classList.remove('active');
      modalImg.src = '';
    }
  });
</script>

---

## References

Triola, M. F. (2022). *Elementary statistics* (13th ed.). Pearson.  
Pearson Education. (2022). *Elementary statistics* course materials.

---
[← Back to Home](https://gabrielledominguez.github.io/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/)


