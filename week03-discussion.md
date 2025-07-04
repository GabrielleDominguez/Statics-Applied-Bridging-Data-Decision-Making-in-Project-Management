# Week 3 Discussion: Using Probability to Mitigate Risk and Guide Strategic Decisions

> *This discussion demonstrates how expected value and binomial probability inform smarter, more disciplined decision-making under uncertainty, both in the game of chance and project management.*

---

## **Discussion Topic**

#### Imagine you’re offered a game where a fair six-sided die is rolled. If it lands on a 6, you win $10. If it lands on any other number, you win nothing. It costs $1 to play each time.  
### Would you play this game repeatedly? Why or why not? What role does probability play in your decision, and how would you determine if this is a "fair" game in the long run?

---
Would I play this game repeatedly? Yes, but with clear decision criteria inspired by both statistics and family wisdom.

Growing up, my grandfather used to sing a Kenny Rogers song called "The Gambler." In the chorus Kenny says, *"You need to know when to hold them, fold them, and when to walk away"* (Rogers, 1978). This country star, intentionally or not, perfectly captured how strategy comes into play in the dice game scenario.

This game follows a *binomial probability distribution* with positive expected value: (1/6 × $10) + (5/6 × $0) - $1 = $0.67 per game. Using binomial formulas μ = np and σ = √npq (Triola, 2022, p. 224), if I play 30 games, I expect 5 wins with a standard deviation of 2.04 wins.

**The Kenny Rogers approach:** 

**Hold them:** When I'm within normal variance (1-9 wins in 30 games). The geometric distribution reminds me that waiting several games for my first win is mathematically normal - *no reason to panic* during early losses.  

**Fold them:** When performance becomes significantly poor using the Range Rule of Thumb - fewer than 0.92 wins in 30 games signals *something's wrong* statistically.

**Walk away:** When I hit significantly good performance (9+ wins) or reach my predetermined profit target. *Greed kills* more positive-expectation opportunities than bad luck could ever.

As a project manager, I use this same framework. Every project has expected outcomes and normal variance ranges. Success comes from setting clear criteria upfront, not making emotional decisions. The math shows that it is a "fair" game in my favor, but Kenny Rogers makes a good point, you got to know when to walk away.

---

> **Reply from Classmate:**  
> Hi Gabrielle, I like that you are the only one who has said yes so far to this question. I loved how you used such a strong example; it helped me understand why you would choose to play the game, but also helped me understand that you can play games of this sort, but be mindful, like gambling. I also think it's cool that you use this strategy in your everyday life; it shows that probability influences several decisions and plans. Are there ways you think this game would become "unfair" to play? Or do you approach every situation with both statistical and family wisdom?

> **Response from Gabrielle Dominguez:**  
> Hi Alexis,  
>  
> You raise an excellent question in regards to when the game becomes *"unfair."* From my vantage point, the answer has **both mathematical and subjective parts.**   
>  
> Mathematically, the game remains "fair" to play as long as there's no tampering from the gamemaster. e.g., there are no trick dice in use, they pay out what they promise, and the rules don't change while you're playing. But what you're getting at connects to something economists call **"utility theory"** - the idea that the same outcome affects different people differently.
>  
> An example that comes to mind: Take two players, Player A only has $10 they can afford to lose and Player B has abundant resources and can easily play 100+ rounds. They're both playing the same game with the same $0.67 expected value per round, but their experience is going to be completely different. Player A might feel like the game is rigged after a few losses and the circumstances force them to quit. In contrast, Player B can stick it out through the bad streaks and actually see that positive expected value pay off.  
>  
> This ties into **diminishing marginal utility;** losing a dollar hurts Player A way more than it hurts Player B. The math stays the same, but the practical impact depends on what each person can handle.  
>  
> In short: from my vantage point, **the game becomes *"unfair"* not when the statistics change, but when external circumstances force a player to quit before the probabilities can work in their favor.** The game doesn't discriminate, but our personal circumstances create very different playing fields.

---

## Kenny Rogers-Inspired Risk Framework

<style>
  .kenny-img-container {
    position: relative;
    max-width: 100%;
    width: 400px;
    margin: 0 auto;
    border: 1.5px solid #e2e8f0; /* Added border */
    overflow: hidden; /* Ensure hover effect stays clean */
  }

  .kenny-img-container img {
    display: block;
    width: 100%;
    height: auto;
    cursor: pointer;
    border-radius: 0;
    transition: filter 0.3s ease;
  }

  .kenny-plus {
    position: absolute;
    top: 6px;
    right: 6px;
    font-size: 16px;
    font-weight: normal;
    color: rgba(0, 0, 0, 0.4);
    user-select: none;
    pointer-events: none;
    transition: color 0.3s ease;
  }

  .kenny-img-container:hover .kenny-plus {
    color: rgba(0, 0, 0, 0.7);
  }

  @media (hover: hover) and (pointer: fine) {
    .kenny-img-container:hover img {
      filter: brightness(0.9);
    }
  }

  .kenny-modal {
    display: none;
    position: fixed;
    z-index: 1000;
    top: 0; left: 0;
    width: 100vw;
    height: 100vh;
    background: rgba(0,0,0,0.8);
    justify-content: center;
    align-items: center;
  }

  .kenny-modal.active {
    display: flex;
  }

  .kenny-modal img {
    max-width: 90%;
    max-height: 90%;
    box-shadow: 0 0 15px rgba(0,0,0,0.5);
    border-radius: 8px;
  }

  .kenny-close {
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

<div class="kenny-img-container">
  <img src="Kenny%20Rogers%20PNG.png" alt="Kenny Rogers Decision Framework" id="kenny-zoom" />
  <div class="kenny-plus">+</div>
</div>

<div id="kenny-modal" class="kenny-modal" role="dialog" aria-modal="true">
  <span id="kenny-close" class="kenny-close" aria-label="Close modal">&times;</span>
  <img src="" alt="Zoomed Kenny" id="kenny-modal-img" />
</div>

<script>
  const kennyImg = document.getElementById('kenny-zoom');
  const kennyModal = document.getElementById('kenny-modal');
  const kennyModalImg = document.getElementById('kenny-modal-img');
  const kennyClose = document.getElementById('kenny-close');

  kennyImg.addEventListener('click', () => {
    kennyModal.classList.add('active');
    kennyModalImg.src = kennyImg.src;
    kennyModalImg.alt = kennyImg.alt;
  });

  kennyClose.addEventListener('click', () => {
    kennyModal.classList.remove('active');
    kennyModalImg.src = '';
  });

  kennyModal.addEventListener('click', (e) => {
    if (e.target === kennyModal) {
      kennyModal.classList.remove('active');
      kennyModalImg.src = '';
    }
  });

  document.addEventListener('keydown', (e) => {
    if (e.key === "Escape" && kennyModal.classList.contains('active')) {
      kennyModal.classList.remove('active');
      kennyModalImg.src = '';
    }
  });
</script>

---

## References

Rogers, K. (1978). *The Gambler* [Song]. On *The Gambler*. United Artists Records.  
Triola, M. F. (2022). *Elementary statistics* (13th ed.). Pearson  

---

[← Back to Home](https://gabrielledominguez.github.io/Statistics-Applied-Bridging-Data-Decision-Making-in-Project-Management/)
