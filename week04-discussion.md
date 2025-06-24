# Week 4 Discussion: How the Central Limit Theorem Supports Confident Decision-Making

> *This discussion explores how the Central Limit Theorem allows project managers to use sample data to reliably estimate population parameters, enhancing planning accuracy and leadership confidence.*

---

## **Discussion Topic**

#### Discuss how the Central Limit Theorem supports the use of sample data to estimate population parameters. Provide an example showing a confidence interval for a population mean and interpret the result. Cite at least one reliable source.

---

In project management, I often have to make instant decisions without having all of the information. The **Central Limit Theorem (CLT)** is a statistical concept that I am excited to add to my toolkit.

The CLT states that with a sufficiently large random sample (usually n > 30), *the distribution of sample means will approximate a normal distribution, even if the population itself is not normally distributed* (Triola, 2022).

Here’s how I’d apply this principle: Often I find myself estimating how long code reviews typically take to better plan team capacity. Let's say over the last six months, a team logs 450 code reviews. If I randomly sample 40 of them and find a mean duration of 2.8 hours with a standard deviation of 1.2 hours, the CLT applies (since n = 40). From there, I can calculate a 95% confidence interval for the mean:

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

> **Reply from Justina Fedeli:**  
> This is a really great post, and it’s cool that you shared how you actually use the Central Limit Theorem in your work with code reviews. Your example made it easy to understand how CLT helps with planning and gives you more confidence in your estimates. I also liked how you talked about growing as a leader and learning that using the right tools is more important than having all the answers. It’s inspiring to see how statistics can be so useful in real situations. I’m curious—how has using CLT changed the way you plan team capacity compared to how you did it before? And have you shared this method with your team to help them understand your estimates better?

> **Response from Gabrielle Dominguez:**  
> Thank you for your thoughtful questions, Justina! To clarify, I haven't implemented CLT methods in my planning yet, but this example highlighted its potential value in business realms.  
>  
> Currently, I use **RACI models** to track individual responsibilities and daily calls ("standups") to monitor team progress. For future planning, I conduct **lessons learned sessions** after each project to capture information: what worked, what didn't, and tangible effort metrics. I maintain this historical data for estimates, but it's been more **intuitive analysis** than rigorous statistical methods.  
>  
> What is exciting is that I already collect extensive project data. I just haven't applied statistical techniques to it yet. Instead of telling our management "this typically takes X hours based on past projects," I could provide **confidence intervals** using CLT and our historical dataset.  
>  
> I believe any (and all) teams would value seeing the methodology behind estimates rather than relying solely on experience. Since we're already fairly data-driven, incorporating statistical analysis feels like a logical evolution of our planning process.  
>  
> I am looking forward to continuing to learn alongside you this semester.

---

## CLT and Confidence Interval Visuals

<!-- CLT 2 and 3 side-by-side -->
<table>
  <tr>
    <td align="center" style="padding: 10px;">
      <a href="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/main/CLT%202.png?raw=true" target="_blank" rel="noopener">
        <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/main/CLT%202.png?raw=true" width="450" alt="CLT 2" />
      </a>
    </td>
    <td align="center" style="padding: 10px;">
      <a href="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/main/CLT%203.png?raw=true" target="_blank" rel="noopener">
        <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/main/CLT%203.png?raw=true" width="450" alt="CLT 3" />
      </a>
    </td>
  </tr>
</table>

<!-- CLT 4 full width but limited height -->
<table>
  <tr>
    <td align="center" style="padding: 10px;">
      <a href="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/main/CLT%204.png?raw=true" target="_blank" rel="noopener">
        <img src="https://github.com/GabrielleDominguez/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/blob/main/CLT%204.png?raw=true" width="900" style="height: 400px; object-fit: contain;" alt="CLT 4" />
      </a>
    </td>
  </tr>
</table>

---

## References

Triola, M. F. (2022). *Elementary statistics* (13th ed.). Pearson.  
Pearson Education. (2022). *Elementary statistics* course materials.

---

[← Back to Home](https://gabrielledominguez.github.io/Statics-Applied-Bridging-Data-Decision-Making-in-Project-Management/)

