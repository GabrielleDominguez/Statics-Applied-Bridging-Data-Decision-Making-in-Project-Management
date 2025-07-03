# Week 1 Discussion: Using Data Types & Graphs to Uncover Meaningful Project Insights

<img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/e9bfec267e13ca9bd2a7fd51882c703d766e1d63/Article%201%2C%20image%201.png?raw=true" alt="Cover image" style="display:none" />

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
<div style="display: flex; flex-wrap: nowrap; max-width: 1100px; margin: 0 auto;">
  <div class="imageBorder" >
    <img
      src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/e9bfec267e13ca9bd2a7fd51882c703d766e1d63/Article%201%2C%20image%201.png?raw=true"
      alt="Graph Visualization 1"
      style="width: 100%; height: auto; display: block; cursor: pointer; border-radius: 0; transition: filter 0.3s ease;"
      class="zoomable"
    />
    <div class="plus">+</div>
  </div>

  <div class="imageBorder borderLeft" >
    <img
      src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/a726a09148e94f6302b2a706f8dfdfa9ef6c7852/Article%201%2C%20image%202%20v6.png?raw=true" 
      alt="Graph Visualization 2"
      style="width: 100%; height: auto; display: block; cursor: pointer; border-radius: 0; transition: filter 0.3s ease;"
      class="zoomable"
    />
    <div style="position: absolute; top: 6px; right: 6px; font-size: 16px; color: rgba(0,0,0,0.4); pointer-events:none;">+</div>
  </div>
</div>

<style>
  
.imageBorder {
flex: 1; border: 1.5px solid #e2e8f0; position: relative; overflow: hidden;
}

.borderLeft {
border-left: none;
}

.plus {
position: absolute; top: 6px; right: 6px; font-size: 16px; color: rgba(0,0,0,0.4); pointer-events:none;
}
  
  /* Desktop: double size from 250px to ~500px */
  @media (min-width: 769px) {
    div[style*="flex: 1"] {
      min-width: 500px;
    }
    div[style*="flex: 1"]:hover img.zoomable {
      filter: brightness(0.85);
      transition: filter 0.3s ease;
    }
    div[style*="flex: 1"]:hover {
      box-shadow: none;
      filter: none;
      z-index: 10;
      transition: none;
    }
  }

  /* Mobile: keep exactly as is, side by side */
  @media (max-width: 768px) {
    div[style*="flex: 1"] {
      min-width: 45vw;
    }
  }

  /* Remove right border on last box */
  div[style*="flex: 1"]:last-child {
    border-right: none !important;
  }
  
  /* Hover effect for desktop only (shared across all articles) */
@media (hover: hover) and (pointer: fine) {
  .imageBorder:hover img.zoomable {
    filter: brightness(0.9);
    transition: filter 0.3s ease;
  }

  .imageBorder:hover .plus {
    color: rgba(0, 0, 0, 0.7);
    transition: color 0.3s ease;
  }
}<style>
  .imageBorder {
    flex: 1;
    border: 1.5px solid #e2e8f0;
    position: relative;
    overflow: hidden;
  }

  .borderLeft {
    border-left: none;
  }

  .plus {
    position: absolute;
    top: 6px;
    right: 6px;
    font-size: 16px;
    color: rgba(0,0,0,0.4);
    pointer-events: none;
  }
  
@media (hover: hover) and (pointer: fine) {
  .imageBorder:hover img.zoomable {
    filter: brightness(0.9);
    transition: filter 0.3s ease;
  }

  .imageBorder:hover .plus {
    color: rgba(0, 0, 0, 0.7);
    transition: color 0.3s ease;
  }
}
</style>

<script>
  // Modal Zoom script unchanged
  const zoomables = document.querySelectorAll('.zoomable');
  const modal = document.createElement('div');
  modal.id = 'modal';
  modal.style.cssText = `
    display:none; 
    position:fixed; 
    z-index:1000; 
    top:0; left:0; 
    width:100vw; height:100vh; 
    background:rgba(0,0,0,0.8); 
    justify-content:center; 
    align-items:center;
  `;
  modal.innerHTML = `
    <span id="modal-close" style="position: fixed; top: 20px; right: 30px; color: white; font-size: 30px; font-weight: bold; cursor: pointer;">&times;</span>
    <img id="modal-img" src="" alt="" style="max-width: 90%; max-height: 90%; border-radius: 8px; box-shadow: 0 0 15px rgba(0,0,0,0.5);" />
  `;
  document.body.appendChild(modal);

  const modalImg = document.getElementById('modal-img');
  const modalClose = document.getElementById('modal-close');

  zoomables.forEach(img => {
    img.addEventListener('click', () => {
      modal.style.display = 'flex';
      modalImg.src = img.src;
      modalImg.alt = img.alt;
    });
  });

  modalClose.addEventListener('click', () => {
    modal.style.display = 'none';
    modalImg.src = '';
  });

  modal.addEventListener('click', e => {
    if (e.target === modal) {
      modal.style.display = 'none';
      modalImg.src = '';
    }
  });

  document.addEventListener('keydown', e => {
    if (e.key === 'Escape') {
      modal.style.display = 'none';
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


