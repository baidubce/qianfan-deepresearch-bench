<div align="center">
  <img src="assets/baidu.png" alt="Logo Baidu" height="60" style="margin-right: 60px;" />
  <img src="assets/baidu-cloud-en.png" alt="Logo Baidu-Cloud" height="55" />
</div>

<h1 align="center">Qianfan-DeepResearch Benchmark Results</h1>


## 📖 Overview

This repository contains the official evaluation results of Qianfan-DeepResearch by Baidu Qianfan team on the [DeepResearch Bench benchmark](https://github.com/Ayanami0730/deep_research_bench), submitted to the [DeepResearch Bench Leaderboard](https://huggingface.co/spaces/muset-ai/DeepResearch-Bench-Leaderboard). 

## 📊 Evaluation Results on DeepResearch Bench

The results demonstrate **Qianfan-DeepResearch**'s overall score and performance across four key dimensions in the **DeepResearch Bench** evaluation:


| Rank | Model | Overall | Comprehensiveness | Insight | Instruction Following | Readability |
|:----:|-------|:-------:|:----:|:-------:|:--:|:----:|
| 1 | **Qianfan-DeepResearch Pro** | **54.48** | **55.21** | **56.47** | **52.35** | **52.02** |
| 2 | **Qianfan-DeepResearch** | <u>53.07</u> | 52.65 | <u>55.44</u> | 51.61 | 51.21 |
| 3 | Tavily Research | 52.44 | 52.84 | 53.59 | 51.92 | 49.21 |
| 4 | ThinkDepth.ai | 52.43 | 52.02 | 53.88 | 52.04 | 50.12 |
| 5 | Cellcog | 51.94 | 52.17 | 51.90 | 51.37 | 51.94 |
| 6 | Salesforce AIR | 50.65 | 50.00 | 51.09 | 50.77 | 50.32 |
| 7 | LangChain Open Deep Research GPT-5 with Gensee Search | 50.60 | 50.06 | 50.76 | 51.31 | 49.72 |
| 8 | Gemini 2.5 Pro DeepResearch* | 49.71 | 49.51 | 49.45 | 50.12 | 50.00 |
| 9 | LangChain Open Deep Research GPT-5 with Travily | 49.33 | 49.80 | 47.34 | 51.05 | 48.99 |
| 10 | OpenAI DeepResearch* | 46.45 | 46.46 | 43.73 | 49.39 | 47.22 |
| 11 | Claude Research* | 45.00 | 45.34 | 42.79 | 47.58 | 44.66 |

<small> 

*Note1*: We show the score in **bold** if our system achieves the best performance, and in <u>underline</u> if it is the second best. 

*Note2*: Models marked with an `*` represent results reproduced by the DeepResearch Bench paper and do not imply that the respective companies submitted these results to the leaderboard.

*Note3*: We report the performance of **Qianfan-DeepResearch Pro** and **Qianfan-DeepResearch** based on their median overall scores accross multiple runs.

</small>


The evaluation covers 100 research tasks across 22 distinct fields. Individual task results are available in `qianfan-deepresearch[-pro]_datas/eval_results/race/baidu-qianfan-drs[-pro]/raw_results.jsonl`, and detailed reports for each task can be found in the `qianfan-deepresearch[-pro]_datas/reports` directory.

## 🙏 Acknowledgements

We thank the DeepResearch Bench team for creating this comprehensive benchmark for evaluating deep research agents. Visit [DeepResearch Bench Leaderboard](https://huggingface.co/spaces/muset-ai/DeepResearch-Bench-Leaderboard) for the complete rankings and detailed evaluation criteria.
