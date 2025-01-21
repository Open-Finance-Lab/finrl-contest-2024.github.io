---
layout: page
title: Overview
permalink: /
---
<div style="text-align: center; display: flex; width: 100%; justify-content: space-evenly; align-items: center; gap: 1em; padding: 2em">
  <img style="width: 20%;" src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/logos/acm.png?raw=true" alt="ACM Logo">
  <img style="width: 20%;" src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/logos/columbiau.jpeg?raw=true" alt="Columbia Logo">
  <img style="width: 20%;" src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/logos/stevens.png?raw=true" alt="Stevens Logo">
  <img style="width: 20%;" src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/logos/rpi.png?raw=true" alt="RPI Logo">
</div>
<div style="text-align: center; display: flex; width: 100%; justify-content: space-evenly; align-items: center; gap: 1em; padding: 2em">
  <img style="width: 25%;" src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/logos/Northwestern_University.png?raw=true" alt="NU Logo">
  <img style="width: 25%;" src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/logos/finai.png?raw=true" alt="FinAI logo">
  <img style="width: 25%;" src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/logos/idea.jpeg?raw=true" alt="IDEA">
</div>

#### **Thank You to Our Sponsors**
<div style="text-align: center; display: flex; width: 100%; justify-content: space-evenly; align-items: center; gap: 1em; padding: 2em">
  <img style="width: 40%;" src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/logos/vatic.png?raw=true" alt="VATIC logo">
</div>

#### **GitHub**
The starter kit and related resources are available at [Github](https://github.com/Open-Finance-Lab/FinRL_Contest_2024).


#### **All FinRL Contests**
**FinRL Contest 2023**: [Contest Website](https://open-finance-lab.github.io/finrl-contest.github.io/); [Github](https://github.com/Open-Finance-Lab/FinRL_Contest_2023)

**FinRL Contest 2024**: [Contest Website](https://open-finance-lab.github.io/finrl-contest-2024.github.io/); [Github](https://github.com/Open-Finance-Lab/FinRL_Contest_2024)

## Introduction
Financial Reinforcement Learning (FinRL) is an interdisciplinary field that applies reinforcement learning to perform financial tasks. FinRL’s ability to adapt to changing market conditions makes it a powerful tool for developing strategies in various tasks, such as portfolio management, algorithmic trading, and option pricing.

The FinRL contest is a competition that explores and evaluates the capability of machine learning methods in finance. FinRL Contest 2024 introduces two tasks designed to address key challenges in FinRL. It features with: 
1. **Ensemble Learning:** Tackling the challenge of policy instability in FinRL, **ensemble learning** can reduce the variance and bias associated with individual agents, leading to more reliable performance in volatile market conditions. To overcome the sampling bottleneck and accelerate the training of component agents, we also provide a vectorized environment that supports massively parallel simulations.
2. **Reinforcement Learning from Market Feedback (RLMF)**: Large language models (LLMs) have been used in financial tasks, such as sentiment analysis and generating novel trading signals. However, there is a gap between general-purpose LLMs and financial markets, since general-purpose LLMs trained on Internet data may not capture the intrinsic dynamics of financial markets. To align LLMs with financial markets, we propose to adapt LLMs using **Reinforcement Learning from Market Feedback**, as a counterpart of Reinforcement Learning from Human Feedback (RLHF). RLMF utilizes feedback from the financial market as reward signals, enabling LLMs to learn from financial market behaviors.

We design two tasks to reflect these advancements: (1) Cryptocurrency trading with ensemble methods, and (2) LLM-engineered signals with RLMF. We welcome students, researchers, and engineers who are passionate about finance and machine learning. And we encourage the development of ensemble strategies, novel signals, and innovative algorithms that can adapt to changing market conditions and generate superior returns for investors.

## Data
We have more than 30 market data sources to deal with different financial tasks. We hold the data APIs and sample market environments in an open-source repository, [FinRL-Meta](https://github.com/AI4Finance-Foundation/FinRL-Meta), as shown in Figure 1. In addition, in [FinGPT](https://github.com/AI4Finance-Foundation/FinGPT), as shown in Figure 2, we have a variety of financial data sources that assures comprehensive market coverage. Contestants are welcome to explore and use in the FinRL Contest.

<div style="display: flex; justify-content: center; align-items: flex-start; flex-wrap: wrap; text-align: center;">
  <figure style="display: inline-block; margin: 10px; text-align: center;">
    <img src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/pictures/FinRL_Meta_Data.png?raw=true" alt="Figure 1: Market data sources of FinRL-Meta" width="500"/>
    <p>Figure 1: FinRL-Meta market data sources</p>
  </figure>
  <figure style="display: inline-block; margin: 10px; text-align: center;">
    <img src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/pictures/fingpt_data_sources.jpg?raw=true" alt="Figure 2: FinGPT-FinNLP data sources" width="800"/>
    <p>Figure 2: Financial data sources for FinGPT</p>
  </figure>
</div>

## Environment
With a deep reinforcement learning approach, market datasets are processed into gym-style environments. The market environment provided to participants is designed to enhance both the realism and efficiency of the simulation process.

Table 1 lists the state spaces, action spaces, and reward functions of different FinRL applications. A state shows how an agent perceives a market situation. Facing a state, the agent can take an action from the action set, which may vary according to the financial tasks. Reward is an incentive mechanism for an agent to learn a better policy. Contestants will specify the state space, action space, and reward functions in the environment for both tasks.

Figure 3 shows the provided vectorized environment to support massively parallel simulataions. It manages multiple parallel sub-environments, each simulating different market scenarios and incorporating realistic market constraints.

<div style="display: flex; justify-content: center; align-items: flex-start; flex-wrap: wrap; text-align: center;">
  <figure style="display: inline-block; margin: 10px; text-align: center;">
    <img src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/pictures/table1.png?raw=true" alt="Table 1: List of state space, action space, and reward function" width="300"/>
    <p>Table 1: List of state space, action space, and reward function</p>
  </figure>
  <figure style="display: inline-block; margin: 10px; text-align: center;">
    <img src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/pictures/vec_env.png?raw=true" alt="Figure 3: Vectorized environment" width="210"/>
    <p>Figure 3: Vectorized environment</p>
  </figure>
</div>

## Timeline
* **Team Registration Begin**: October 6th, 2024
* **Starter-Kit Release**: October 15th, 2024
* **Submission Open**: October 20th, 2024
* **Solution Submission Deadline**: ~~November 3rd, 2024~~ <span style="color:red;">November 7th, 2024</span>
* **Report Submission Deadline**: ~~November 7th, 2024~~ <span style="color:red;">November 8th, 2024</span>
* **Winner Notification**: November 12th, 2024
* **Winner Announcement**: November 15th, 2024

<span style="color:blue;">(All deadlines are at 11:59pm EST on the specified date.)</span>

Winners will be invited to attend the ACM ICAIF 2024 conference and have the opportunity to present their work at the conference.

## Tasks

Each team can choose to participate in one or both tasks. The prizes will be awarded for each task.


### Tutorials and Starter Kit
We provide some [tutorials](https://github.com/Open-Finance-Lab/FinRL_Contest_2024) for participants to learn FinRL.

The starter kits are released [here](https://github.com/Open-Finance-Lab/FinRL_Contest_2024)

### Task I: Cryptocurrency Trading with Ensemble Learning
This task aims to develop robust and effective trading agents for cryptocurrencies using ensemble methods. Participants are expected to explore innovative ensemble methods for single cryptocurrency trading. They are also encouraged to take advantage of the power of massively parallel simulations by utilizing the provided vectorized environments.

#### Dataset
A dataset containing second-level Limit Order Book (LOB) data for Bitcoin is provided. Contestants are free to apply various techniques to the data, design component models, and use innovative methods to increase the diversity of component models in the ensemble. 

#### Environments
The initial cash should be $1 million.

The contestants are required to:
1. Specify the state space, action space, and reward functions in the environment.
2. Ensure that the final ensemble model should be able to interact with the provided trading environment.

#### Model Evaluation
The performance of the model will be assessed by the following metrics:

1. Cumulative return. It is the total return generated by the trading strategy over a trading period.
2. Sharpe ratio. It takes into account both the returns of the portfolio and the level of risk.
3. Max drawdown. It is the portfolio’s largest percentage drop from a peak to a trough in a certain time period, which provides a measure of downside risk.

#### Submission
Participants need to submit a well-organized repository containing all scripts, models, and any custom libraries used to implement the solution. Each team should also submit a 1-2 page report with the [ACM sigconf template](https://www.overleaf.com/latex/templates/acm-conference-proceedings-primary-article-template/wbvnghjbzwpc) through [Open Review](https://openreview.net/group?id=ACM.org/ICAIF/2024/Competition/FinRL#tab-your-consoles). The title should start with “FinRL Contest 2024 Task I.”

### Task II: LLM-Engineered Signals with RLMF
This task aims to develop LLMs that can generate and engineer effictive signals from news by using Reinforcement Learning from Market Feedback (RLMF). By incorporating market feedback in the fine-tuning process, LLMs can learn from and adapt to financial market behaviors.

In this task, the LLM will be used to generate one type of signal (e.g., a sentiment score) based on the content of news. Contestants will develop models that leverage RLMF to adjust the signals based on the market feedback. Contestants are expected to explore useful market feedback from market data and innovative reward models to fine-tune their LLMs. 

#### Dataset
An OHLCV dataset and a corresponding news dataset for a list of stocks are provided. Contestants are free to use external datasets to deveop RLMF methods and fine-tune the LLMs.

#### Requirements
1. Contestants should use the LLM that can be loaded with huggingface and can do inference on 20GB GPU.
2. Contestants can determine what signal to generate and engineer.
3. Contestants should provide the prompt for their LLM. For example, _"What is the sentiment score of {stock ticker} after the release of this news: {news}. Give and only return the score in the range of [-1, 1]. Answer: "_

#### Model Evaluation
To assess the effectiveness of the signal engineered by the LLMs, we will apply the signal to a simple and practical trading strategy: 
1. Buy the top 3 stocks with the highest signals on the day of the news release and sell them 3 days later.
2. Short-sell the 3 stocks with the lowest signals on the day of the news release and cover the short position 3 days later.

The initial cash is $1 million, which will be allocated equally to each trading day and each stock.

The performance will be assessed by the following metrics:

1. Cumulative return. It is the total return generated by the trading strategy over a trading period.
2. Win/loss ratio. It is calculated by dividing the number of winning trades by the number of losing trades over a trading period.

#### Submission
Participants need to submit the prompt and their LLM , which should be easily loaded and tested. Each team should also submit a 1-2 page report with the [ACM sigconf template](https://www.overleaf.com/latex/templates/acm-conference-proceedings-primary-article-template/wbvnghjbzwpc) through [Open Review](https://openreview.net/group?id=ACM.org/ICAIF/2024/Competition/FinRL#tab-your-consoles). The title should start with “FinRL Contest 2024 Task II.”


## Evaluation
For each task, the final ranking of participants will be determined by a weighted combination of model evaluation and report assessment, with weights of 60% and 40% respectively.

**Model evaluation**:
* Task 1: the geometric mean of the rankings of cumulative return, Sharpe ratio, and Max drawdown.
* Task 2: the geometric mean of the rankings of cumulative return and win/loss ratio.

**Report assessment**:

The assessment of the reports will be conducted by invited experts and professionals. The judges will independently rate the data and model analysis, results and discussion, robustness and generalizability, innovation and creativity, organization and readability, each accounting for 20% of the qualitative assessment. 

## Organizers

### Core Organizers

| Photo                | Biography              |
|----------------------|-------------------|
| ![Keyi Wang](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/keyi.jpeg?raw=true)      | **Keyi Wang**, master’s candidate at Northwestern University, bachelor’s at Columbia University. Organizer of FinRL Contest 2023. Interested in machine learning and financial engineering. Core member of AI4Finance open-source community, responsible for project development and maintenance of FinRL.|
| ![Nikolaus Holzer](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/nikolaus_holzer.jpeg?raw=true)      | **Nikolaus Holzer**, master’s candidate at Columbia University, bachelor’s at Columbia Univeristy. Interested in machine learning, natural language processing, and their applications in finance.|
| ![Yangyang Yu](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/yangyang_yu.jpg?raw=true)      | **Yangyang Yu**, Ph.D. candidate at Stevens Institute of Technology, master’s at Syracuse University. Her research integrates cognitive science, language agent design, Bayesian statistics, and multimodal learning, focusing on FinTech applications. She serves as a program committee member and an organizer for workshops at IJCAI and COLING. She also serves as a reviewer of NeurIPS, ICLR, CogSci, UIST, etc.|
| ![Qian Chen](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/qian_chen.jpg?raw=true)      | **Qian Chen**, senior data scientist at Tencent Games, has over five years of experience as data scientist at tech companies including Uber & Upstart. He got a master degree at Columbia University. His research interests include machine learning, deep reinforcement learning, and big data. He is one of the core members of the FinRL project.|
| ![Jaisal Patel](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/jaisal_patel.png?raw=true)      | **Jaisal Patel**, undergraduate at Rensselaer Polytechnic Institute. Interested in quantitative finance, venture capital, and the intersection of AI and finance. Program committee member for the International Workshop on Multimodal Financial Foundation Models (MFFMs) at ICAIF 2024. Only student award recipient at GitHub Universe 2023.|
| ![Andy Zhu](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/andy_zhu.jpg?raw=true)      | **Andy Zhu**, undergraduate student researcher at Rensselaer Polytechnic Institute. Researching the intersection of large language models and finance. Program committee member and submission reviewer of Multimodal Financial Foundation Models workshop at ICAIF 2024. Software Development intern at SDSC (San Diego Supercomputer Center).|




### Advisors

| Photo                | Biography              |
|----------------------|-------------------|
| ![Xiao-Ying Liu](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/supervisors/liu-xy.png?raw=true) | **Xiao-Yang Liu**, Ph.D., Columbia University, faculty at Rensselaer Polytechnic Institute. His research interests include deep reinforcement learning, big data, and high-performance computing. He created several open-source projects, such as FinRL, ElegantRL, and FinGPT. He contributed chapters to a textbook on reinforcement learning for cyber-physical systems and a textbook on tensors for data processing. He serves as a PC member for NeurIPS, ICML, ICLR, AAAI, IJCAI, AISTATS, and ICAIF. He also served as a Session Chair for IJCAI 2019. He organized Financial Challenges in Large Language Models (FinLLM)@IJCAI 2024, FinRL Competition at ACM ICAIF 2023, the First/Second Workshop on Quantum Tensor Networks in Machine Learning (QTNML) at NeurIPS 2020/2021, IJCAI 2020 Workshop on Tensor Networks Representations in Machine Learning, and the NeurIPS 2019 Workshop on Machine Learning for Autonomous Driving.|
| ![Kairong Xiao](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/supervisors/kairong_xiao.jpg?raw=true) | **Kairong Xiao**, Roger F. Murray Associate Professor of Business at Columbia Business School. His research interests span financial intermediation, corporate finance, monetary economics, industrial organization, and political economy. His research papers have been published in top finance and economics journals, including the Journal of Finance, the Review of Financial Studies, the  Journal of Financial Economics, Econometrica, the Journal of Monetary Economics, and Management Science. He received numerous awards for research excellence, including the Review of Financial Studies Rising Scholar Award, the Journal of Finance Dimensional Fund Advisors Prize for Distinguished Paper, and the Review of Financial Studies Best Paper Award runner-up.|
| ![Jiechao Gao](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/supervisors/jiechao_gao.jpeg?raw=true) | **Jiechao Gao**, Ph.D., University of Virginia. His research interests include machine learning, reinforcement learning, federated learning algorithms and applications in distributed networks, cyberphysical systems and financial environments. He serves as a PC member and reviewer for NeurIPS, KDD, ICLR, AAAI, INFOCOM, IEEE Big Data, IEEE TNNLS, IEEE IoT Journal, etc. He organized FinRL Competition at ACM ICAIF 2023, UbiComp/ISWC 2024Workshop on Design with Autistic Children, and EAI SecureComm 2022 Workshop on S/P-IoT.|
| ![Christina Dan Wang](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/supervisors/dan_wang.jpeg?raw=true) | **Christina Dan Wang**, Assistant Professor of Finance, NYU Shanghai; Global Network Assistant Professor, NYU. Prior to joining NYU Shanghai, Wang was an Assistant Professor in the Department of Statistics at Columbia University and a Postdoctoral Researcher in the Operations Research and Financial Engineering department and at the Bendheim Center for Finance at Princeton University.|


## Contact
Contestants can communicate any questions on [Discord](https://discord.gg/RNYsEwcXVj).

Contact email: [finrlcontest@gmail.com](mailto:finrlcontest@gmail.com)
