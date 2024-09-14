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
  <img style="width: 20%;" src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/logos/Northwestern_University.png?raw=true" alt="NU Logo">
  <img style="width: 20%;" src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/logos/finai.png?raw=true" alt="FinAI logo">
  <img style="width: 20%;" src="https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/logos/FinRL.png?raw=true" alt="FinRL Logo">
</div>


Financial Reinforcement Learning (FinRL) is an interdisciplinary field that applies reinforcement learning to perform financial tasks. FinRL’s ability to adapt to changing market conditions makes it a powerful tool for developing strategies in various tasks, such as portfolio management, algorithmic trading, and option pricing.

The FinRL contest is a competition that explores and evaluates the capability of machine learning methods in finance. FinRL Contest 2024 introduces two tasks designed to address key challenges in FinRL. It features with: 
1. **Ensemble Learning:** One of the key challenges in reinforcement learning, particularly in financial tasks, is the issue of policy instability, where agents’ strategies may fail to converge to an optimal solution. **Ensemble learning** can reduce the variance and bias associated with individual agents, leading to more reliable performance in volatile market conditions. To overcome the sampling bottleneck and accelerate the training of component agents, we also provide a vectorized environment that supports massively parallel simulations.
2. **LLM-generated Signals:** LLMs have shown powerful natural language processing capabilities, making them well-suited for analyzing
complex financial documents, such as SEC 10-K, 10-Q, and XBRL filings. In the FinRL Contest, we combine the strengths of LLMs and FinRL: LLMs generate valuable signals from textual analysis, while FinRL agents leverage these signals to improve trading
strategies within dynamic market environments.

We design two tasks to reflect these advancements: (1) Cryptocurrency trading with ensemble methods, and (2) Stock trading with LLM-generated signals. We welcome students, researchers, and engineers who are passionate about finance and machine learning. And we encourage the development of ensemble strategies, novel signals, and innovative algorithms that can adapt to changing market conditions and generate superior returns for investors.

## Data
We have more than 30 market data sources to deal with different financial tasks. We hold the data APIs and sample market environments in an open-source repository, FinRL-Meta, as shown in Figure 1. Contestants are welcome to explore and use in the FinRL Contest.

![figure1](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/pictures/FinRL_Meta_Data.png?raw=true)

Figure 1: Market data sources of FinRL-Meta

## Environment
With a deep reinforcement learning approach, market datasets are processed into gym-style market environments. The market environment provided to participants is designed to enhance both the realism and efficiency of the simulation process.

Table 1 lists the state spaces, action spaces, and reward functions of different FinRL applications. A state shows how an agent perceives a market situation. Facing a state, the agent can take an action from the action set, which may vary according to the financial tasks. Reward is an incentive mechanism for an agent to learn a better policy. Contestants will specify the state space, action space, and reward functions in the environment for both tasks.

![table1](https://github.com/Open-Finance-Lab/ACM_ICAIF_2023/blob/main/web/app/assets/figures/table1.png?raw=true)

Table 1: List of state space, action space, and reward function

## Timeline
* **Team Registration Begin**: September 17th, 2024
* **Traning Datasets and Baseline Solution Release**: September 27th, 2024
* **Submission Open**: October 10th, 2024
* **Solution Submission Deadline**: October 29th, 2024
* **Report Submission Deadline**: November 5th, 2024
* **Winner Notification**: November 12th, 2023
* **Winner Announcement**: November 14th ~ 17th, 2023

<span style="color:blue;">(All deadlines are at 11:59pm EST on the specified date.)</span>


Winners will be invited to attend the ACM ICAIF 2024 conference and have the opportunity to present their work at the conference.

## Tasks

Each team can choose to participate in one or both tasks. The prizes will be awarded for each task.


### Starter Kit
The starter kit and related resources will be released soon.

### Task I: Cryptocurrency Trading with Ensemble Learning
This task aims to develop robust and effective trading agents for cryptocurrencies using ensemble methods. Participants are expected to to explore innovative ensemble methods for single cryptocurrency trading. They are also encouraged to harness the power of massively parallel simulations by utilizing the provided vectorized environments.

A dataset containing minute-level Limit Order Book (LOB) data for Bitcoin is provided. Contestants are free to apply various techniques to the data, design component models, and use innovative methods to increase the diversity of component models in the ensemble. 

Then the contestants are required to:
1. Specify the state space, action space, and reward functions in the environment.
2. Ensure that the final ensemble model should be able to interact with the provided trading environment..

Each team should also submit a 1-2 page report with the [ACM sigconf template](https://www.overleaf.com/latex/templates/acm-conference-proceedings-primary-article-template/wbvnghjbzwpc) through Open Review. The title should start with “FinRL Contest 2024 Task I.”


### Task II: Stock Trading with LLM-generated Signals
This task aims to enhance FinRL trading strategies by incorporating LLM-generated signals, integrating the advantages of FinRL and
LLMs. participants are expected to use LLMs to generate valuable trading signals from structured data, including SEC 10-K, 10-Q, and XBRL filings. These signals are then integrated into the FinRL trading environment to enhance the decision-making of the trading agents.

![figure2](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/pictures/task_2.png?raw=true)
Figure 2: Task 2 stock trading with LLM-generated signals

In this task, as shown in Fig 2, participants need to perform the stock trading task:
1. **Use LLMs to generate signals**. Participants will utilize LLMs to analyze SEC 10-K, 10-Q, and XBRL filings, assessing a company’s financial health, risk factors, and business performance, to generate valuable trading signals.
2. **Integrate signals into FinRL**. These signals will be incorporated into the state of the FinRL environments. Participants should specify the state space, action space, and reward functions in the environment.
3. **Perform stock trading with FinRL**. The trading agent will utilize this enriched state to make more informed decisions.


We provide the SEC 10-K, 10-Q, XBRL filings, and the OHLCV dataset for a list of stocks. Participants are permitted to use external datasets, such as news articles, to enhance their analysis. For a fair comparison, participants are required to use the same FinRL agent, specifically the PPO agent, and the same provided environment


Participants need to submit a well-organized repository containing all scripts, models, and any custom libraries used to implement the solution. The models should be easily loaded and tested. Each team should also submit a 1-2 page report with the [ACM sigconf template](https://www.overleaf.com/latex/templates/acm-conference-proceedings-primary-article-template/wbvnghjbzwpc) through Open Review. The title should start with “FinRL Contest 2024 Task II.”

## Evaluation

For each task, the final ranking of participants will be determined by a weighted combination of model evaluation and report assessment, with weights of 60% and 40% respectively.

**Model evaluation** is the geometric mean of the rankings of following metrics:

1. Cumulative return. It is the total return generated by the trading strategy over a trading period.
2. Sharpe ratio. It takes into account both the returns of the portfolio and the level of risk.
3. Max drawdown. It is the portfolio’s largest percentage drop from a peak to a trough in a certain time period, which provides a measure of downside risk.

**Report assessment** of the report:

The assessment of the reports will be conducted by invited experts and professionals. The judges will independently rate the data and model analysis, results and discussion, robustness and generalizability, innovation and creativity, organization and readability, each accounting for 20% of the qualitative assessment. 

The final ranking will be determined by the combination of 60% quantitative and 40% qualitative assessment.


## Organizers

### Core Organizers

| Photo                | Biography              |
|----------------------|-------------------|
| ![Keyi Wang](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/keyi.jpeg?raw=true)      | **Keyi Wang**, master’s candidate at Northwestern University, bachelor’s at Columbia University. Organizer of FinRL Contest 2023. Interested in machine learning and financial engineering. Core member of AI4Finance open-source community, responsible for project development and maintenance of FinRL.|
| ![Nikolaus Holzer](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/nik.jepg?raw=true)      | **Nikolaus Holzer**, master’s candidate at Columbia University, bachelor’s at Columbia Univeristy. Interested in machine learning, natural language processing, and their applications in finance.|
| ![Yangyang Yu](https://github.com/Open-Finance-Lab/finrl-contest-2024.github.io/blob/main/assets/organizers/yangyang.jepg?raw=true)      | **Nikolaus Holzer**, Ph.D. candidate at Stevens Institute of Technology, master’s at Syracuse University. Her research integrates cognitive science, language agent design, Bayesian statistics, and multimodal learning, focusing on FinTech applications. She serves as a program committee member and an organizer for workshops at IJCAI and COLING. She also serves as a reviewer of NeurIPS, ICLR, CogSci, UIST, etc.|



### Advisors

| Photo                | Biography              |
|----------------------|-------------------|
| ![Xiao-Ying Liu](https://github.com/Open-Finance-Lab/ACM_ICAIF_2023/blob/main/web/app/assets/staffphotos/advisors/liu-xy.png?raw=true) | **Xiao-Yang Liu** Ph.D., Columbia University, faculty at Rensselaer Polytechnic Institute. His research interests include deep reinforcement learning, big data, and high-performance computing. He created several open-source projects, such as FinRL, ElegantRL, and FinGPT. He contributed chapters to a textbook on reinforcement learning for cyber-physical systems and a textbook on tensors for data processing. He serves as a PC member for NeurIPS, ICML, ICLR, AAAI, IJCAI, AISTATS, and ICAIF. He also served as a Session Chair for IJCAI 2019. He organized Financial Challenges in Large Language Models (FinLLM)@IJCAI 2024, FinRL Competition at ACM ICAIF 2023, the First/Second Workshop on Quantum Tensor Networks in Machine Learning (QTNML) at NeurIPS 2020/2021, IJCAI 2020 Workshop on Tensor Networks Representations in Machine Learning, and the NeurIPS 2019 Workshop on Machine Learning for Autonomous Driving.|
| ![Jiechao Gao](https://github.com/Open-Finance-Lab/ACM_ICAIF_2023/blob/main/web/app/assets/staffphotos/advisors/jiechao_gao.jpeg?raw=true) | **Jiechao Gao** Ph.D., University of Virginia. His research interests include machine learning, reinforcement learning, federated learning algorithms and applications in distributed networks, cyberphysical systems and financial environments. He serves as a PC member and reviewer for NeurIPS, KDD, ICLR, AAAI, INFOCOM, IEEE Big Data, IEEE TNNLS, IEEE IoT Journal, etc. He organized FinRL Competition at ACM ICAIF 2023, UbiComp/ISWC 2024Workshop on Design with Autistic Children, and EAI SecureComm 2022 Workshop on S/P-IoT.|


## Contact
Contestants can communicate any questions on [Discord](https://discord.gg/a6ebcwPa).

Contact email: [finrlcontest@gmail.com](mailto:finrlcontest@gmail.com)
