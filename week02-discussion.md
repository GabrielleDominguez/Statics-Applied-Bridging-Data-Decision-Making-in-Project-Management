# Week 2 Discussion: Using Measures of Center & Variation to Evaluate Team Performance

> *This discussion demonstrates how variation can uncover critical performance differences that averages alone may conceal, enhancing analysis of team output and delivery risk.*

---

## **Discussion Topic**

#### Why is it important to consider both measures of center and measures of variation when analyzing a dataset? Provide an example and construct a boxplot to visualize your explanation. Cite your sources.

---

When analyzing business data sets, examining only measures of center provides an incomplete and potentially misleading picture. As Triola explains in our textbook, *"we need objective measures instead of relying on subjective judgments"* when evaluating variation (Triola, 2022, p. 105). This principle is essential when drawing accurate results because two data sets can have identical means, but *dramatically* different amounts of variation.

Drawing from my project management experience, I've created the following scenario: Two software development teams, **Team Alpha** and **Team Beta**, both complete an average of 15 user stories per sprint over their last 10 sprints. (A user-story is a feature or task that needs to be completed, and a sprint is the 1–4 week window given to complete the tasks.) Their performance data shows:

**Team Alpha completion rates:** 14, 15, 16, 15, 14, 15, 16, 14, 15, 16  
**Team Beta completion rates:** 8, 25, 12, 18, 6, 22, 15, 19, 10, 15

While both teams have identical means (15 user stories completed), their variations greatly differ. **Team Alpha** shows minimal variation with a standard deviation of 0.82, while **Team Beta** exhibits substantial variation with a standard deviation of 5.94.

This difference in variation has *critical business consequences.* A development team with excessive variation in sprint completion can create significant project management challenges.

**Team Alpha's consistent performance** enables reliable sprint planning and delivery schedules. **Team Beta's high variation,** even though they are *capable* of delivering 25 user stories per sprint, creates uncertainty that could often jeopardize project timelines and client commitments.

The **boxplot** shows that while both teams are centered on the same mean, one team has a much greater range of results. This contrast makes it easy for stakeholders to spot the difference in their project performance.

---

## Boxplot Visualizations

<div style="display: flex; flex-wrap: nowrap; max-width: 1100px; margin: 0 auto;">
  <div class="imageBorder" >
    <img
   src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/0ace3bb0847c61018f2c28df93381757fd91469c/Article%202%2C%20image%201%20v8.png?raw=true"
      alt="Boxplot Image 1"
      style="width: 100%; height: auto; display: block; cursor: pointer; border-radius: 0; transition: filter 0.3s ease;"
      class="zoomable"
    />
    <div class="plus">+</div>
  </div>

  <div class="imageBorder borderLeft" >
    <img
   src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/4a74e50303f921a564c35dad7ae6df8e7c4d7fcc/Article%202%2C%20image%202%20v5.png?raw=true"
      alt="Boxplot Image 2"
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
  
  function generateOpenGraphTags() {
    const currentURL = window.location.href;
    
    const titleElement = document.querySelector('h1');
    const title = titleElement ? titleElement.textContent.trim() : '';
    
    const imageElement = document.querySelector('img');
    let imageURL = '';
    if (imageElement) {
      imageURL = imageElement.src;
      if (imageURL.startsWith('/')) {
        imageURL = window.location.origin + imageURL;
      }
    }
    
    const paragraphs = document.querySelectorAll('p');
    let description = '';
    for (let p of paragraphs) {
      if (p.textContent.trim() && p.textContent.trim().length > 20) {
        description = p.textContent.trim();
        if (description.length > 160) {
          description = description.substring(0, 157) + '...';
        }
        break;
      }
    }
    
    function updateMetaTag(property, content, attribute = 'property') {
      if (!content) return;
      let metaTag = document.querySelector(`meta[${attribute}="${property}"]`);
      if (!metaTag) {
        metaTag = document.createElement('meta');
        metaTag.setAttribute(attribute, property);
        document.head.appendChild(metaTag);
      }
      metaTag.setAttribute('content', content);
    }
    
    updateMetaTag('og:title', title);
    updateMetaTag('og:description', description);
    updateMetaTag('og:image', imageURL);
    updateMetaTag('og:url', currentURL);
    updateMetaTag('twitter:title', title);
    updateMetaTag('twitter:description', description);
    updateMetaTag('twitter:image', imageURL);
    
    if (title) document.title = title;
  }

  document.addEventListener('DOMContentLoaded', function() {
    setTimeout(generateOpenGraphTags, 100);
  });
</script>
  
---

## References

Triola, M. F. (2022). *Elementary statistics* (13th ed.). Pearson.  
Pearson Education. (2022). *Elementary statistics* course materials.

---

[← Back to Home](https://gabrielledominguez.github.io/Statistics-Applied-Bridging-Data-Decision-Making-in-Project-Management/)

