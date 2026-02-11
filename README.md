# 🚀 Daily Data Science & Engineering Log

**Goal:** Consistent daily progress on my path to becoming a Data Scientist.
**Focus:** IBM Data Science Professional Certificate, Python, and Machine Learning.

![Status](https://img.shields.io/badge/Status-Active-success)
![Focus](https://img.shields.io/badge/Focus-Data%20Science-blue)
![Commitment](https://img.shields.io/badge/Update-Daily-green)

---

## 📅 Daily Progress Tracker

This repository serves as the central hub for my daily work. It captures every step of my learning journey, ensuring a complete record of my progress.

* **Code Updates:** Daily pushes of Python scripts, Jupyter Notebooks, and project files.
* **Theory & Concepts:** Detailed logs of theoretical concepts, algorithms, and study notes updated daily in the log below.

Whether I am writing code or studying complex algorithms, every learning detail is documented and updated here every single day.

---

## 📂 Repository Structure

* `notebooks/` - Jupyter Notebooks from the IBM Data Science course.
* `scripts/` - Python scripts and experiments.
* `projects/` - Larger projects (e.g., Nova Voice Assistant).
* `README.md` - This file, containing the daily learning log.

---

## 📈 Daily Learning Log

*Detailed notes on concepts, algorithms, and theory.*

### 2026-02-08
* **Topic:** Repository Initialization
* **Notes:** Established the repository structure and workflow. Set up the environment to track daily progress for both coding tasks and theoretical study.

### Update: 2026-02-08
- Daily progress logged via bvcbcbcbcvbcbcv.

### Update: 2026-02-08
- Day 40 of learning Data Science with IBM.

After building my first linear regression models yesterday, I was left with a big question: How do I actually know if the model is good? I assumed I just had to look at the numbers, but today I learned that visualizing the "mistakes" is actually more powerful.

At first, I didn't get the point of a "Residual Plot." I thought the goal was to plot the prediction line and see if it touched the data points. If the line looks close to the dots, the model works, right? I was confused why we needed a whole separate graph just to show the error (the difference between the predicted value and the actual value). It seemed negative to focus on where the model went wrong.

It clicked for me when I realized that the *shape* of those errors tells a hidden story. The notes explained that if your linear model is good, the errors should just be random noise—scattered everywhere with no pattern. But if the errors form a specific shape, like a "U" curve, it means my "straight line" model is trying to fit data that actually curves. The residual plot proved that a linear assumption was actually incorrect for my data.

It turns out that seeing where you failed is just as important as seeing where you succeeded because it tells you when you need to switch to a different method. Since my residuals are showing a curve, it looks like I need to explore "Polynomial Regression" next to handle the bends in the data. For those of you who analyze data, is the residual plot your first check, or do you rely more on score metrics like R-squared?

### Update: 2026-02-08
- Day 40 of learning Data Science with IBM.

After building my first linear regression models yesterday, I was left with a big question: How do I actually know if the model is good? I assumed I just had to look at the numbers, but today I learned that visualizing the "mistakes" is actually more powerful.

At first, I didn't get the point of a "Residual Plot." I thought the goal was to plot the prediction line and see if it touched the data points. If the line looks close to the dots, the model works, right? I was confused why we needed a whole separate graph just to show the error (the difference between the predicted value and the actual value). It seemed negative to focus on where the model went wrong.

It clicked for me when I realized that the *shape* of those errors tells a hidden story. The notes explained that if your linear model is good, the errors should just be random noise—scattered everywhere with no pattern. But if the errors form a specific shape, like a "U" curve, it means my "straight line" model is trying to fit data that actually curves. The residual plot proved that a linear assumption was actually incorrect for my data.

It turns out that seeing where you failed is just as important as seeing where you succeeded because it tells you when you need to switch to a different method. Since my residuals are showing a curve, it looks like I need to explore "Polynomial Regression" next to handle the bends in the data. For those of you who analyze data, is the residual plot your first check, or do you rely more on score metrics like R-squared?

### Update: 2026-02-08
- Day 41 of learning Data Science with IBM.

After learning how to visually check my model with residual plots yesterday, today I moved on to numerical evaluation and a crucial concept called the "Train/Test Split."

At first, I didn't get why I would purposefully hide data from my model. The notes explained that we usually split our dataset, using about 70% to train the model and keeping 30% secret for testing. This confused me because I thought data was fuel for the algorithm. If I have 100 cars in my dataset, why would I only let the computer learn from 70 of them? It felt like I was handicapping the model by withholding information that could help it learn better.

It clicked for me when I understood the difference between "In-Sample" and "Out-of-Sample" evaluation. If I train the model on 100% of the data and then test it on that exact same data, the model isn't necessarily predicting anything; it might just be memorizing the answers. It’s like studying for a history exam by memorizing the specific wording of the practice questions. You might get a 100% on the practice test, but you'll fail the real exam because you didn't actually learn the concepts (this is what the notes call "Generalization Error").

By holding back that 30% (the Test set), I’m creating a simulation of the "real world" to see if the model can actually handle data it has never seen before.

Now that I know I need to split the data to get an honest score, I'm wondering: is the 70/30 split a strict rule, or do you change that ratio depending on how much total data you have?

### Update: 2026-02-09
- Day 42 of learning Data Science with IBM.

After learning about the Train/Test split yesterday, today I dove into Polynomial Regression and how to choose the right "complexity" for a model.

At first, I didn't get why we wouldn't always choose the most flexible model available. I assumed that if a curved line fits the data better than a straight line, then a *super* squiggly line (like a 16th-order polynomial) that touches every single data point would be the ultimate goal. I thought, "If the training error is zero, I've created the perfect model."

It clicked for me when I learned about **Overfitting**. I saw a graph showing that when the model becomes *too* complex, it starts chasing the random noise in the data rather than the actual trend. It’s like a student who memorizes the exact answers to the homework but fails the exam because they didn't understand the underlying concepts. The notes showed that while the training error goes down as you make the model more complex, the "test error" eventually shoots back up because the model tries too hard to fit anomalies.

It seems like Data Science is a constant balancing act between being "too simple" (Underfitting) and "too complex" (Overfitting). To handle this, the notes introduced "Cross Validation"—is this the standard way you all ensure your model isn't just getting lucky with its predictions?

### Update: 2026-02-10
- Day 43 of learning Data Science with IBM.

After learning yesterday that "Overfitting" is what happens when a model tries too hard and memorizes the noise in the data, I was left wondering how to fix it. I assumed the only solution was to use a simpler model, but today I learned about a technique called "Ridge Regression" that handles this specifically.

At first, I didn't get how Ridge Regression actually worked. The notes mentioned that when a model overfits (like a high-order polynomial), the mathematical "coefficients" become massive numbers. I was stuck on the concept of "Alpha"—a parameter used to control these numbers. It felt counterintuitive to me: why would we purposefully penalize the model and force the coefficients to be smaller? I thought the goal was to let the model do whatever math it needed to fit the data points.

It clicked for me when I visualized Alpha as a sort of "stiffness" control or a dampener. If Alpha is zero, the model is loose and wild, chasing every single outlier and creating those crazy squiggly lines I saw yesterday. But as you increase Alpha, it forces the model to ignore the small, random fluctuations and focus on the general trend. It basically stops the model from reacting too extremely to outliers.

It seems like finding the right Alpha is the key—if it's too high, the model becomes too rigid (Underfitting), but if it's too low, it stays wild (Overfitting). I learned that we use Cross Validation to test different Alpha values and find the "sweet spot." For those of you working with noisy data, do you usually stick with Ridge Regression, or is Lasso better for handling these outliers?

### Update: 2026-02-11
- Day 44 of learning Data Science with IBM.

After learning yesterday that the "Alpha" value in Ridge Regression helps prevent overfitting, I was left with a big practical question: How do I actually know which number to pick for Alpha? Do I just keep guessing until it works? Today, I learned the answer is a technique called "Grid Search."

At first, I was confused by the distinction between a "parameter" and a "hyperparameter." I assumed the model learned *everything* from the data. I also dreaded the idea of manual trial-and-error, imagining I’d have to write code to run the model 50 times with 50 different Alpha values just to see which one was best.

It clicked for me when I realized that Hyperparameters (like Alpha) are settings *I* have to control because the model can't learn them from the data itself. Grid Search basically automates that whole messy trial-and-error process. I can essentially give the computer a list (a "grid") of different settings—like various Alpha values and normalization options—and it systematically builds a model for every single combination using Cross Validation. It then compares the R-squared scores and tells me exactly which combination wins.

It feels great to have a method that removes the guesswork from tuning the model. However, considering it builds a new model for every single combination, does Grid Search become incredibly slow when you start working with massive datasets?