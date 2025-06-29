# Week 4 Discussion: Using the Central Limit Theorem to Strengthen Project Forecasting

> *This discussion explores how the Central Limit Theorem allows project managers to use sample data to reliably estimate population parameters, enhancing planning accuracy and leadership confidence.*

---

## **Discussion Topic**

#### Discuss how the Central Limit Theorem supports the use of sample data to estimate population parameters. Provide an example showing a confidence interval for a population mean and interpret the result. Cite at least one reliable source.

---

In project management, I often have to make instant decisions without having all of the information. The **Central Limit Theorem (CLT)** is a statistical concept that I am excited to add to my toolkit.

The CLT states that with a sufficiently large random sample (usually n > 30), *the distribution of sample means will approximate a normal distribution, even if the population itself is not normally distributed* (Triola, 2022).

Here’s how I’d apply this principle to better plan team capacity: Let's say over the last six months, a team logs 450 code reviews. If I randomly sample 40 of them and find a mean duration of 2.8 hours with a standard deviation of 1.2 hours, the CLT applies (since n = 40). From there, I can calculate a 95% confidence interval for the mean:

- **Standard error** = 1.2 ÷ √40 ≈ 0.19  
- **Margin of error** = 1.96 × 0.19 ≈ 0.37  
- **Confidence interval** = 2.8 ± 0.37 → between 2.43 and 3.17 hours

This tells me that I can be **95% confident** that the true average time for code reviews of similar work will fall within this range - there is *no guesswork.* I have a statistically backed estimate that will help me plan more realistically and communicate with the team.

Earlier in my career, I felt pressure to know all the answers or be the most technically knowledgeable person in the room. Over time, I’ve learned that the best leaders *aren't* the people who have all the answers - but rather, the ones who know how to ask the right questions and use the right tools. **CLT is one of those tools** that will help me make smarter, more confident decisions.

---

> **Reply from Chloe Lanham:**  
> Hey Gabrielle, your response was clear to read and helped me understand CLT even more. I wonder what would happen if the random sample were even more than 40? Would we still feel 95% confident that the reviews would fall in the range? I agree that CLT can help us make smarter, more confident decisions.

> **Response from Gabrielle Dominguez:**  
> This is a great question, Chloe. You're spot on about sample size - if I used 80 or 100 code reviews instead of 40, the confidence interval would actually get tighter.  
>  
> With a larger sample, the **standard error decreases** because we're dividing by the square root of a bigger number. This shrinks our margin of error, so instead of that 2.43 to 3.17 hour range, we might get something like 2.55 to 3.05 hours. We'd still be 95% confident, but with *much more precision*. This is exactly why I'm excited about applying this principle to project data.  
>  
> Ironically, I have been collecting this data for years, but never thought to use it statistically. I'm realizing how much more value I can squeeze out of information I have access to.  
>  
> I am glad CLT is making sense to you too! I have a feeling it'll change how many of us approach decision making. I am looking forward to picking up more tools like this throughout the semester alongside you.

---

## Forecasting Visualizations

<style>
  .image-row {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 4px;
    margin-bottom: 12px;
  }

  .img-container {
    position: relative;
    width: calc(50% - 2px);
    flex: 0 0 calc(50% - 2px);
  }

  .img-container img {
    width: 100%;
    height: auto;
    display: block;
    object-fit: cover;
    border-radius: 4px;
    cursor: pointer;
  }

  .zoom-plus {
    position: absolute;
    top: 4px;
    right: 4px;
    font-size: 14px;
    color: rgba(0, 0, 0, 0.4);
    user-select: none;
    pointer-events: none;
    z-index: 10;
  }

  .img-container:hover .zoom-plus {
    color: rgba(0, 0, 0, 0.7);
  }

  @media screen and (max-width: 768px) {
    .image-row {
      gap: 2px;
    }

    .img-container {
      width: calc(50% - 1px);
      flex: 0 0 calc(50% - 1px);
    }

    .zoom-plus {
      font-size: 12px;
      top: 2px;
      right: 2px;
    }
  }

  .modal {
    display: none;
    position: fixed;
    z-index: 1000;
    left: 0;
    top: 0;
    width: 100vw;
    height: 100vh;
    background: rgba(0, 0, 0, 0.8);
    justify-content: center;
    align-items: center;
  }

  .modal.active {
    display: flex;
  }

  .modal img {
    max-width: 90%;
    max-height: 90%;
    border-radius: 8px;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
  }

  .modal-close {
    position: fixed;
    top: 20px;
    right: 30px;
    color: white;
    font-size: 30px;
    font-weight: bold;
    cursor: pointer;
  }
</style>

<div class="image-row">
  <div class="img-container">
    <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/93f32c8b2ecd9146c1ce521b00630e13e77c3d53/Article%204%2C%20image%201%2C%20resize%20v2.png?raw=true" alt="Forecasting Image 1" class="zoomable" />
    <div class="zoom-plus">+</div>
  </div>
  <div class="img-container">
    <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/93f32c8b2ecd9146c1ce521b00630e13e77c3d53/Article%204%2C%20image%202%2C%20resize%20v2.png?raw=true" alt="Forecasting Image 2" class="zoomable" />
    <div class="zoom-plus">+</div>
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
    if (e.key === "Escape") {
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

