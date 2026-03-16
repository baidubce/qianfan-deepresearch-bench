<div align="center">
  <img src="assets/baidu.png" alt="Logo Baidu" height="60" style="margin-right: 60px;" />
  <img src="assets/baidu-cloud-zh.png" alt="Logo Baidu-Cloud" height="55" />
</div>

<h1 align="center">Qianfan-DeepResearch Benchmark Results</h1>


## 📖 概述

本仓库包含了百度千帆团队在 [DeepResearch Bench 基准测试](https://github.com/Ayanami0730/deep_research_bench) 上的官方评估结果，这些结果已提交至 [DeepResearch Bench 排行榜](https://huggingface.co/spaces/muset-ai/DeepResearch-Bench-Leaderboard)。

**Qianfan-DeepResearch** 是一个基于千帆大模型（Qianfan-DeepResearch Pro 和 Qianfan-DeepResearch）的深度研究智能体，它能够理解、执行和总结研究任务。你可以在[千帆Agent平台](https://console.bce.baidu.com/qianfan/studio/officialAppCenter)上使用它，或通过 API 调用它。

## 📊 DeepResearch Bench 评估结果

下表展示了 **Qianfan-DeepResearch** 在 **DeepResearch Bench** 上总分及四个关键维度的评估结果：

| Rank | Model | Overall | Comprehensiveness | Insight | Instruction Following | Readability |
|:----:|-------|:-------:|:----:|:-------:|:--:|:----:|
| 1 | **Qianfan-DeepResearch Pro<sup>†</sup>** | **54.48** | **55.21** | **56.47** | **52.35** | **52.02** |
| - | Qianfan-DeepResearch Pro [Leaderboard] | 54.22 | 55.07 | 56.09 | 51.77 | 52.12 |
| 2 | **Qianfan-DeepResearch<sup>†</sup>** | <u>53.07</u> | 52.65 | <u>55.44</u> | 51.61 | 51.21 |
| - | Qianfan-DeepResearch [Leaderboard] | 53.02 | 52.33 | 55.63 | 51.24 | 51.39 |
| 3 | Tavily Research | 52.44 | 52.84 | 53.59 | 51.92 | 49.21 |
| 4 | ThinkDepth.ai | 52.43 | 52.02 | 53.88 | 52.04 | 50.12 |
| 5 | Cellcog | 51.94 | 52.17 | 51.90 | 51.37 | 51.94 |
| 6 | Salesforce AIR | 50.65 | 50.00 | 51.09 | 50.77 | 50.32 |
| 7 | LangChain Open Deep Research GPT-5 with Gensee Search | 50.60 | 50.06 | 50.76 | 51.31 | 49.72 |
| 8 | Gemini 2.5 Pro DeepResearch<sup>\*</sup> | 49.71 | 49.51 | 49.45 | 50.12 | 50.00 |
| 9 | LangChain Open Deep Research GPT-5 with Travily | 49.33 | 49.80 | 47.34 | 51.05 | 48.99 |
| 10 | OpenAI DeepResearch<sup>\*</sup> | 46.45 | 46.46 | 43.73 | 49.39 | 47.22 |
| 11 | Claude Research<sup>\*</sup> | 45.00 | 45.34 | 42.79 | 47.58 | 44.66 |

<small> 

*备注*：若本系统取得最佳性能，其得分将以**粗体**显示；若为次优，则以<u>下划线</u>标注。 

\*：标有星号\*的模型代表 DeepResearch Bench 论文复现的结果，并不代表相关公司向排行榜提交了测试结果。

†：我们基于多次评估的Overall得分中位数，汇报 **Qianfan-DeepResearch Pro** 和 **Qianfan-DeepResearch** 的性能表现。

</small>


评估涵盖了 22 个不同领域中的 100 个研究任务。各个任务的详细结果可在 `qianfan-deepresearch[-pro]_datas/eval_results/race/baidu-qianfan-drs[-pro]/raw_results.jsonl` 中查看，每个任务的详细报告可以在 `qianfan-deepresearch[-pro]_datas/reports` 目录中找到。

## 🙏 致谢

我们感谢 DeepResearch Bench 团队创建了这一全面的基准测试，用于评估深度研究智能体。请访问 [DeepResearch Bench 排行榜](https://huggingface.co/spaces/muset-ai/DeepResearch-Bench-Leaderboard) 查看完整排名和详细评估标准。