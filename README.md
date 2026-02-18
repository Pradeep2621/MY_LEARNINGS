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

### Update: 2026-02-12
- Day 45 of learning Data Science with IBM.

After spending the last few days focusing on specific techniques like Ridge Regression and Grid Search, today I finally put everything together in a comprehensive project. I worked on a real-world dataset to predict medical insurance costs based on factors like age, BMI, and smoking status.

At first, as I started building the model, my workflow felt incredibly disjointed. I had separate blocks of code for everything: one part to fill in missing values, another to normalize the data using `StandardScaler`, another to add polynomial features, and finally the regression model itself. I was constantly worried that I might make a mistake, like forgetting to scale the "test" data exactly the same way I scaled the "training" data, which I learned can ruin the predictions.

It clicked for me when I built a **Machine Learning Pipeline**. I realized that I didn't have to manage these steps manually in separate chunks. By using a pipeline, I could chain the scaler, the polynomial transformer, and the model into a single object. It felt like moving from an assembly line where I had to carry the parts between stations myself, to a fully automated conveyor belt. I just fed the raw data in at the start, and the pipeline handled all the transformations and the final prediction automatically.

It was also satisfying to see the Exploratory Data Analysis (EDA) confirm real-world intuition; the visualizations clearly showed that smoking status was the strongest predictor of high costs, overpowering even BMI.

Now that I see how much cleaner the code is, I can't imagine going back to manual steps. For those of you in the field, do you build pipelines right from the start of a project, or is that something you only add once you know which model works best?

### Update: 2026-02-13
- Day 46 of learning Data Science with IBM.

After setting up my machine learning pipeline yesterday, I spent today refining the Medical Insurance project and dealing with the messy reality of the raw data. Specifically, I ran into a problem I hadn't thought much about before: missing values.

At first, when I saw rows in the dataset where the age or smoking status was just a "?", my instinct was to simply delete them. I thought, "If the data isn't there, I can't trust it, so I should get rid of it." It felt safer to only work with "perfect" rows.

It clicked for me when I understood the concept of "Imputation." I realized that by deleting a whole row just because one number (like Age) was missing, I was also throwing away valuable, valid information about that person's BMI, region, and number of children. Instead of deleting, I learned to fill the gaps—using the mean for continuous numbers like age, and the most frequent value for categories like smoking status. It allowed me to preserve the dataset size while keeping the model statistically sound.

It feels like a delicate balance between saving data and "guessing." For those of you who handle messy datasets, at what point do you decide a row has too much missing info to save and just delete it?

### Update: 2026-02-14
- Day 47 of learning Data Science with IBM.

After spending the last few days deep in the weeds of cleaning missing values and building pipelines, today I shifted gears to focus on how to actually present that data through Data Visualization.

At first, I honestly thought the goal of a chart was to show *everything* I had worked on. My instinct was to pack as much data as possible into a single graph—using multiple colors, stacked bars, and complex legends—because I didn't want to "hide" any information. I thought a complex chart made the analysis look more impressive.

It clicked for me when I studied the concept of "chart junk" and the philosophy that "less is more." I realized that adding unnecessary grid lines, 3D effects, or too many variables doesn't make the data better; it just confuses the person looking at it. I learned that a good visualization isn't a data dump; it's a tool to tell a specific story or highlight a single trend, like how the New York Times uses simple line graphs to show clear spikes in data.

I am trying to retrain my brain to delete elements from my charts rather than add them. for those of you who build dashboards, is it difficult to convince stakeholders that a simpler chart is actually more accurate than a complex one?

### Update: 2026-02-15
- Day 48 of learning Data Science with IBM.

Following my realization yesterday about avoiding "chart junk," today I dove into the specific tools in the visualization toolbox: Line plots, Bar charts, Scatter plots, Box plots, and Histograms.

At first, I assumed that as long as I plotted the correct numbers, the chart would automatically tell the "truth." I thought a graph was just a direct reflection of the dataset.

It clicked for me when I saw two different bar charts representing the exact same data about immigration trends. One chart made a decrease look like a catastrophic crash, while the other showed it as a barely noticeable dip. I was confused until I looked at the Y-axis. The "scary" chart started the axis at a high number (zooming in on the top of the bars), while the "calm" chart started at zero. I realized that visualization isn't just about accuracy; it’s about perspective. A zoomed-in scale can manipulate how the viewer feels about the data without technically lying about the numbers.

I am now much more cautious about how I set my axes to ensure I'm not accidentally exaggerating a trend. For those who present data often, do you have a hard rule about always starting the Y-axis at zero, or are there times when zooming in is actually better?

### Update: 2026-02-16
- Day 49 of learning Data Science with IBM.

After learning about the theory of charts and misleading axes yesterday, today I finally opened the toolbox to see *what* we actually use to build them in Python. The list was longer than I expected: Matplotlib, Pandas, Seaborn, Folium, Plotly, and PyWaffle.

At first, I was honestly confused by the redundancy. I didn't get why I needed three different libraries (Matplotlib, Pandas, and Seaborn) just to make a simple bar chart or scatter plot. I thought, "Why not just learn one and ignore the rest?"

It clicked for me when I realized that Matplotlib is basically the engine under the hood for both Pandas and Seaborn. I learned that while Matplotlib gives you granular control over every single pixel, it requires a lot of code to do simple things. Seaborn and Pandas are built *on top* of it to make the code shorter and the charts prettier by default. It helped me see them as layers rather than competitors: use Pandas for a quick check, Seaborn for a beautiful statistical report, and Folium if—and only if—I need a map.

I am looking forward to seeing if I actually stick to the "easy" wrappers or if I end up needing the raw power of Matplotlib more often. For those of you who code in Python, do you stick to Seaborn for the aesthetics, or do you prefer building everything from scratch in Matplotlib?

### Update: 2026-02-18
- Day 50 of learning Data Science with IBM.

Yesterday I was wondering if I’d ever need to use the raw power of Matplotlib instead of the simpler wrappers like Seaborn and Pandas. Today, I think I got my answer after taking a peek under the hood at Matplotlib’s architecture.

At first, I was completely lost in the jargon. I heard about a "Backend layer," an "Artist layer," and a "Scripting layer," and it felt way too abstract. I just wanted to make a plot, not learn about the internal plumbing of the library. My thinking was, "Why do I need to know this? I just call a function like `plt.hist()` and a chart appears."

It clicked for me when I stopped thinking of Matplotlib as a chart-making tool and started seeing it as a blank canvas. The "Scripting layer" (Pyplot) is the easy, automated way to paint—it gives you a pre-made canvas and some basic tools. But the "Artist layer" is where the real control is. I learned that every single element on a plot—every line, every tick mark, the title, the labels—is considered its own independent "artist" object.

Suddenly, I understood. Using a wrapper library is like asking an assistant to draw a bar chart for you. Using the Matplotlib Artist layer is like being given the pen and ruler to draw every single rectangle and write every label yourself. It's more work, but it gives you total control over every tiny detail.

It feels like I’ve been driving an automatic car (Seaborn) and just learned how a manual transmission (Matplotlib) actually works. It’s a bit intimidating, but I can see why you’d need it for custom or complex visualizations. I wonder how often experienced users have to "get their hands dirty" with individual artist objects?