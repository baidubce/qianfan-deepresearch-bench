<div align="center">
  <p>
    <img src="assets/baidu.png" alt="Baidu" height="42" />
    &nbsp;&nbsp;&nbsp;&nbsp;
    <img src="assets/baidu-cloud-en.png" alt="Baidu AI Cloud" height="38" />
  </p>

  <a href="https://www.dumate.cn/">
    <img src="assets/dumate.png" alt="DuMate" height="68" />
  </a>

  <h1>DuMate-DeepResearch</h1>

  <p>
    <strong>An auditable multi-agent deep research system with recursive search and rubric-grounded reasoning.</strong>
  </p>

  <p>
    <a href="README_zh.md">中文</a>
    ·
    <a href="#leaderboard-snapshot">Leaderboard</a>
    ·
    <a href="#reports">Reports</a>
    ·
    <a href="#citation">Citation</a>
  </p>

  <p>
    <a href="https://arxiv.org/abs/2606.07299"><img src="https://img.shields.io/badge/arXiv-2606.07299-b31b1b.svg" alt="arXiv" /></a>
    <a href="https://www.dumate.cn/"><img src="https://img.shields.io/badge/Try-DuMate-3F2CE7.svg" alt="Try DuMate" /></a>
    <a href="https://cloud.baidu.com/doc/qianfan-api/s/vmizwyngh"><img src="https://img.shields.io/badge/API-Qianfan-1677FF.svg" alt="Qianfan API" /></a>
    <img src="https://img.shields.io/badge/Benchmarks-2-5174FF.svg" alt="Benchmarks" />
    <img src="https://img.shields.io/badge/Reports-232%20Markdown-0F9D58.svg" alt="Reports" />
  </p>
</div>

---

## 📌 Overview

This repository publishes the official **DuMate-DeepResearch** evaluation reports from the Baidu Qianfan team on two deep research benchmarks:

- [DeepResearch Bench](https://github.com/Ayanami0730/deep_research_bench)
- [DeepResearch Bench II](https://github.com/imlrz/DeepResearch-Bench-II)

DuMate-DeepResearch is built on the Qianfan Agent Foundry and designed for long-horizon, evidence-grounded research tasks. It combines graph-based planning, recursive search execution, and rubric-guided reasoning so that research trajectories can be inspected, adapted, and evaluated with fine-grained criteria.

## ✨ Highlights

<table>
  <tr>
    <td width="33%">
      <strong>Graph-Based Dynamic Planning</strong>
      <br />
      An evolving DAG expands from coarse goals into fine-grained research actions, with reflection, re-planning, backtracking, and parallel branching.
    </td>
    <td width="33%">
      <strong>Recursive Two-Level Execution</strong>
      <br />
      An outer Research Agent delegates complex search subtasks to inner Searcher Agents, each with its own planning loop to keep noisy retrieval away from global strategy.
    </td>
    <td width="33%">
      <strong>Rubric-Grounded Optimization</strong>
      <br />
      Dynamically generated quality criteria act as test-time reasoning scaffolds for evidence-grounded synthesis and adaptive stopping.
    </td>
  </tr>
</table>

## 🚀 Access

| Entry | Description |
|:--|:--|
| [DuMate](https://www.dumate.cn/) | Download and use DuMate clients for macOS, Windows, and mobile devices. |
| [Qianfan DeepResearch](https://console.bce.baidu.com/qianfan/studio/officialAppCenter) | Use the DeepResearch Agent application on Baidu AI Cloud's Qianfan API platform. |
| [API Documentation](https://cloud.baidu.com/doc/qianfan-api/s/vmizwyngh) | Read the documentation for integrating with Qianfan DeepResearch. |

<table>
  <tr>
    <td align="center" width="50%">
      <a href="https://www.dumate.cn/">
        <img src="assets/dumate-screenshot.png" alt="DuMate product screenshot" width="100%" />
      </a>
      <br />
      <sub><strong>DuMate</strong></sub>
    </td>
    <td align="center" width="50%">
      <a href="https://console.bce.baidu.com/qianfan/studio/officialAppCenter">
        <img src="assets/qianfandrs_screenshot.png" alt="Qianfan DeepResearch product screenshot" width="100%" />
      </a>
      <br />
      <sub><strong>Qianfan DeepResearch</strong></sub>
    </td>
  </tr>
</table>

<a id="leaderboard-snapshot"></a>

## 🏆 Leaderboard Snapshot

<table>
  <tr>
    <td width="50%">
      <h3>DeepResearch Bench</h3>
      <p><strong>Overall: 58.03</strong></p>
      <p>100 tasks across 22 domains, evaluated with the RACE LLM-as-a-judge framework.</p>
    </td>
    <td width="50%">
      <h3>DeepResearch Bench II</h3>
      <p><strong>Overall: 61.95</strong></p>
      <p>132 tasks with 9,430 fine-grained binary rubrics derived from expert reports.</p>
    </td>
  </tr>
</table>

### DeepResearch Bench

| Model/System | Comprehensiveness | Insight | Instruction Following | Readability | Overall |
|:-------------|:-:|:-:|:-:|:-:|:-:|
| **DuMate-DeepResearch** | **59.48** | **61.48** | 53.87 | 54.34 | **58.03** |
| ZTE Nebula DeepResearch | 58.37 | 59.76 | **54.06** | 54.66 | 57.27 |
| iFlow-Researcher | 58.24 | 59.74 | 53.24 | **55.05** | 57.08 |
| Zhipu Deep Research | 58.15 | 60.14 | 53.47 | 53.88 | 57.06 |
| Xiaoyi DeepResearch 6.0 | 58.58 | 59.38 | 53.58 | 53.99 | 57.00 |
| Cellcog-Max | 57.40 | 60.01 | 53.25 | 53.21 | 56.67 |
| 1688AILab-DeepResearch | 57.32 | 59.27 | 53.51 | 53.36 | 56.53 |
| Octen DeepResearch | 56.89 | 59.00 | 53.39 | 53.83 | 56.31 |
| Grep Deep Research | 56.82 | 58.92 | 53.38 | 53.44 | 56.23 |
| NVIDIA-AIQ | 56.90 | 58.49 | 52.89 | 53.43 | 55.95 |

<small>
We report the performance of DuMate-DeepResearch based on the median overall score across multiple runs. See the full leaderboard at [DeepResearch Bench Leaderboard](https://huggingface.co/spaces/muset-ai/DeepResearch-Bench-Leaderboard).
</small>

### DeepResearch Bench II

| Model/System | Information Recall | Analysis | Presentation | Overall |
|:-------------|:-:|:-:|:-:|:-:|
| **DuMate-DeepResearch** | **57.58** | **71.70** | 89.89 | **61.95** |
| iFlow-Researcher | 54.99 | 69.54 | 92.56 | 59.91 |
| Xiaoyi DeepResearch 6.0 | 53.05 | 69.90 | 91.12 | 58.72 |
| CMCC-DeepInsight | 49.60 | 62.95 | 92.94 | 55.39 |
| NVIDIA-AIQ | 49.23 | 61.55 | **93.15** | 54.50 |
| OpenAI-GPT-o3 Deep Research | 39.98 | 49.85 | 89.16 | 45.40 |
| Gemini-3-Pro Deep Research | 39.09 | 48.94 | 91.85 | 44.60 |
| Gemini-2.5-Pro Deep Research | 34.91 | 51.91 | 90.24 | 41.98 |

<a id="reports"></a>

## 📁 Reports

| Benchmark | Contents | Directory |
|:--|:--|:--|
| DeepResearch Bench | 100 generated reports in Markdown | [`reports/deepresearch_bench/`](reports/deepresearch_bench/) |
| DeepResearch Bench II | 132 generated reports in Markdown | [`reports/deepresearch_bench_ii/`](reports/deepresearch_bench_ii/) |

```text
.
├── assets/
│   ├── dumate-screenshot.png
│   └── qianfandrs_screenshot.png
├── reports/
│   ├── deepresearch_bench/
│   └── deepresearch_bench_ii/
├── README.md
└── README_zh.md
```

<a id="citation"></a>

## 📝 Citation

If you find DuMate-DeepResearch useful, please cite our paper:

```bibtex
@article{yan2026dumatedeepresearchauditablemultiagentrecursive,
      title={DuMate-DeepResearch: An Auditable Multi-Agent System with Recursive Search and Rubric-Grounded Reasoning},
      author={Lingyong Yan and Can Xu and Yukun Zhao and Wenxuan Li and Qingyang Chen and Jiulong Wu and Wenli Song and Xiangnan Li and Weixian Shi and Yiqun Chen and Xuchen Ma and Yuchen Li and Jiashu Zhao and Shuaiqiang Wang and Jianmin Wu and Dawei Yin},
      year={2026},
      eprint={2606.07299},
      archivePrefix={arXiv},
      primaryClass={cs.AI},
      url={https://arxiv.org/abs/2606.07299},
}
```

## 🙏 Acknowledgements

We thank the [DeepResearch Bench](https://github.com/Ayanami0730/deep_research_bench) and [DeepResearch Bench II](https://github.com/imlrz/DeepResearch-Bench-II) teams for building comprehensive benchmarks for evaluating deep research agents.
