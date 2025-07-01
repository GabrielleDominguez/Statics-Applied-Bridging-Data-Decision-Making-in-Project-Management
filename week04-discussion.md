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
<div align="center">
  <table class="forecast-table">
    <tr>
      <td>
        <div class="img-wrapper">
          <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/93f32c8b2ecd9146c1ce521b00630e13e77c3d53/Article%204%2C%20image%201%2C%20resize%20v2.png?raw=true"
               alt="Forecasting Image 1" class="zoomable" />
          <div class="corner top-left"></div>
          <div class="corner top-right"></div>
          <div class="corner bottom-left"></div>
          <div class="corner bottom-right"></div>
          <div class="plus-sign">+</div>
        </div>
      </td>
      <td>
        <div class="img-wrapper">
          <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/93f32c8b2ecd9146c1ce521b00630e13e77c3d53/Article%204%2C%20image%202%2C%20resize%20v2.png?raw=true"
               alt="Forecasting Image 2" class="zoomable" />
          <div class="corner top-left"></div>
          <div class="corner top-right"></div>
          <div class="corner bottom-left"></div>
          <div class="corner bottom-right"></div>
          <div class="plus-sign">+</div>
        </div>
      </td>
    </tr>
  </table>
</div>

<style>
  .forecast-table {
    border-spacing: 0;
    border-collapse: collapse;
  }

  .forecast-table td {
    padding: 0;
    margin: 0;
    border: 1.5px solid #e2e8f0;
    border-radius: 12px;
    background-color: #fff;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05);
    transition: border-color 0.3s cubic-bezier(0.4, 0, 0.2, 1), box-shadow 0.3s;
    vertical-align: top;
  }

  .img-wrapper {
    position: relative;
    padding: 15px;
    border-radius: 12px;
    overflow: visible; /* show corners outside */
  }

  .img-wrapper img.zoomable {
    width: 100%;
    height: auto;
    border-radius: 4px;
    display: block;
    cursor: pointer;
    transition: filter 0.3s ease, transform 0.3s ease;
  }

  /* Corner flair pieces */
  .corner {
    position: absolute;
    width: 12px;
    height: 12px;
    background-color: #cbd5e1;
    border-radius: 3px;
    box-shadow: 0 0 6px rgba(0,0,0,0.1);
    opacity: 0.6;
    transition: opacity 0.3s ease, background-color 0.3s ease;
    pointer-events: none;
  }

  .top-left {
    top: 6px;
    left: 6px;
    clip-path: polygon(0 0, 100% 0, 0 100%);
  }

  .top-right {
    top: 6px;
    right: 6px;
    clip-path: polygon(100% 0, 100% 100%, 0 0);
  }

  .bottom-left {
    bottom: 6px;
    left: 6px;
    clip-path: polygon(0 100%, 100% 100%, 0 0);
  }

  .bottom-right {
    bottom: 6px;
    right: 6px;
    clip-path: polygon(100% 100%, 100% 0, 0 100%);
  }

  .plus-sign {
    position: absolute;
    bottom: 10px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 20px;
    color: rgba(0, 0, 0, 0.4);
    font-weight: normal;
    user-select: none;
    transition: color 0.3s ease, text-shadow 0.3s ease, font-weight 0.3s ease;
    pointer-events: none;
  }

  /* Desktop hover styles */
  @media (hover: hover) and (pointer: fine) {
    .forecast-table td:hover {
      border-color: #cbd5e1;
      box-shadow: 0 8px 25px rgba(0, 0, 0, 0.08);
    }

    .forecast-table td:hover .zoomable {
      filter: brightness(0.88);
      transform: scale(1.05);
    }

    .forecast-table td:hover .corner {
      background-color: #94a3b8;
      opacity: 1;
      box-shadow: 0 0 8px rgba(0,0,0,0.2);
    }

    .forecast-table td:hover .plus-sign {
      color: #475569;
      text-shadow: 0 0 6px rgba(71, 85, 105, 0.8);
      font-weight: 700;
    }
  }

  /* Mobile flare - always show corner flair and subtle shadow */
  @media (hover: none) and (pointer: coarse) {
    .forecast-table td {
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
    }

    .corner {
      opacity: 1;
      background-color: #cbd5e1;
      box-shadow: 0 0 8px rgba(0,0,0,0.1);
    }

    .plus-sign {
      color: rgba(0, 0, 0, 0.5);
      font-weight: 600;
    }

    .zoomable {
      transition: none;
    }
  }
</style>

---

## References

Triola, M. F. (2022). *Elementary statistics* (13th ed.). Pearson.  
Pearson Education. (2022). *Elementary statistics* course materials.

---

[← Back to Home](https://gabrielledominguez.github.io/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/)

