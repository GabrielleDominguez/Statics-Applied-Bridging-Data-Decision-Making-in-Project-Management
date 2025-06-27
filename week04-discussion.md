# Week 4 Discussion: How the Central Limit Theorem Supports Confident Decision-Making

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
- **Confidence interval** = 2.8 ± 0.37 → between **2.43 and 3.17 hours**

This tells me that I can be **95% confident** that the true average time for code reviews of similar work will fall within this range - there is no guesswork. I have a statistically backed estimate that will help me plan more realistically and communicate with the team.

Earlier in my career, I felt pressure to know all the answers or be the most technically knowledgeable person in the room. Over time, I’ve learned that the best leaders aren't the people who have all the answers - but rather, the ones who know how to ask the right questions and use the right tools. **CLT is one of those tools** that will help me make smarter, more confident decisions.

---

> **Reply from Chloe Lanham:**  
> Hey Gabrielle, your response was clear to read and helped me understand CLT even more. I wonder what would happen if the random sample were even more than 40? Would we still feel 95% confident that the reviews would fall in the range? I agree that CLT can help us make smarter, more confident decisions.

> **Response from Gabrielle Dominguez:**  
> This is a great question, Chloe. You're spot on about sample size - if I used 80 or 100 code reviews instead of 40, the confidence interval would actually get tighter.  
>  
> With a larger sample, the **standard error decreases** because we're dividing by the square root of a bigger number. This shrinks our margin of error, so instead of that 2.43 to 3.17 hour range, we might get something like 2.55 to 3.05 hours. We'd still be 95% confident, but with **much more precision**. This is exactly why I'm excited about applying this principle to project data.  
>  
> Ironically, I have been collecting this data for years, but never thought to use it statistically. I'm realizing how much more value I can squeeze out of information I have access to.  
>  
> I am glad CLT is making sense to you too! I have a feeling it'll change how many of us approach decision making. I am looking forward to picking up more tools like this throughout the semester alongside you.

---
<h3>CLT & Confidence Interval Visualizations</h3>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>CLT & Confidence Interval Visualizations</title>
  <style>
    body {
      font-family: sans-serif;
      margin: 20px;
      background-color: #f9f9f9;
    }

    h3 {
      text-align: center;
      margin-bottom: 20px;
    }

    .image-row {
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
      justify-content: space-between;
    }

    .img-container {
      position: relative;
      flex: 1 1 calc(50% - 6px); /* Two per row */
      max-width: calc(50% - 6px);
      overflow: hidden;
      border-radius: 8px;
    }

    .img-container img {
      width: 100%;
      height: auto;
      display: block;
      border-radius: 8px;
    }

    .zoom-plus {
      position: absolute;
      top: 8px;
      right: 10px;
      background-color: rgba(0,0,0,0.6);
      color: white;
      font-size: 20px;
      padding: 4px 8px;
      border-radius: 4px;
      cursor: pointer;
      z-index: 1;
    }

    /* Modal styles */
    .modal {
      display: none;
      position: fixed;
      z-index: 1000;
      top: 0; left: 0;
      width: 100vw;
      height: 100vh;
      background-color: rgba(0, 0, 0, 0.85);
      justify-content: center;
      align-items: center;
    }

    .modal img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(0,0,0,0.6);
    }

    .modal-close {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 36px;
      color: white;
      cursor: pointer;
    }
  </style>
</head>
<body>

<h3>CLT & Confidence Interval Visualizations</h3>

<div class="image-row">
  <div class="img-container">
    <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/8c4f724222070eb46f3559983df6db39bf0ab724/thumbnail%205%20sample.png?raw=true" alt="Thumbnail 5 Sample" class="zoomable" />
    <div class="zoom-plus" aria-hidden="true">+</div>
  </div>

  <div class="img-container">
    <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/458e09ac013829d4397024b04d0328ed321315f4/CLT%20Article%202.png?raw=true" alt="CLT Article 2" class="zoomable" />
    <div class="zoom-plus" aria-hidden="true">+</div>
  </div>
</div>

<div class="image-row" style="margin-top: 12px;">
  <div class="img-container">
    <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/458e09ac013829d4397024b04d0328ed321315f4/CLT%20Article%203.png?raw=true" alt="CLT Article 3" class="zoomable" />
    <div class="zoom-plus" aria-hidden="true">+</div>
  </div>

  <div class="img-container">
    <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/458e09ac013829d4397024b04d0328ed321315f4/CLT%20Article%204.png?raw=true" alt="CLT Article 4" class="zoomable" />
    <div class="zoom-plus" aria-hidden="true">+</div>
  </div>
</div>

<!-- Modal for Zoom -->
<div id="modal" class="modal" role="dialog" aria-modal="true" aria-labelledby="modal-label">
  <span id="modal-close" class="modal-close" aria-label="Close modal">&times;</span>
  <img src="" alt="" id="modal-img" />
</div>

<script>
  const modal = document.getElementById("modal");
  const modalImg = document.getElementById("modal-img");
  const closeModal = document.getElementById("modal-close");

  document.querySelectorAll(".zoom-plus").forEach(plusIcon => {
    plusIcon.addEventListener("click", function (e) {
      const img = this.previousElementSibling;
      modal.style.display = "flex";
      modalImg.src = img.src;
      modalImg.alt = img.alt;
      e.stopPropagation();
    });
  });

  closeModal.addEventListener("click", function () {
    modal.style.display = "none";
  });

  modal.addEventListener("click", function (e) {
    if (e.target === modal) {
      modal.style.display = "none";
    }
  });
</script>

</body>
</html>
---

## References

Triola, M. F. (2022). *Elementary statistics* (13th ed.). Pearson.  
Pearson Education. (2022). *Elementary statistics* course materials.

---

[← Back to Home](https://gabrielledominguez.github.io/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/)

