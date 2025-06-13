# Qwen-Finetune-Project
微调小模型尝试获得思维链能力

# Qwen2.5-0.5B 笑话生成模型微调项目

本项目完整记录了使用 Unsloth 框架对 Qwen2.5-0.5B 模型进行 LoRA 微调的全过程，旨在训练一个能以“链式思考”（Chain-of-Thought）模式对于一些需要一定是为能力问题生成幽默感答复的语言模型。

## ✨ 模型成果

本项目训练得到的最终模型已上传至 Hugging Face Hub，您可以直接下载使用。

**➡️ [点击此处访问Hugging Face模型主页](https://huggingface.co/hanxiaoyu2026/Qwen2.5-ruozhiba-punchline)** 

## 🚀 复现指南

您可以按照以下步骤完整复现本项目的训练过程：

1.  **克隆本仓库**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/hanxiaoyu-coder/Qwen-Finetune-Project
.git)
    cd Qwen-Finetune-Project

    ```

2.  **创建并激活环境** (推荐使用 Conda)
    ```bash
    conda create -n qwen_finetune python=3.10 -y
    conda activate qwen_finetune
    ```

3.  **安装依赖**
    ```bash
    pip install -r requirements.txt
    ```
    *请确保您的环境中已正确安装支持CUDA的PyTorch版本。*

4.  **运行 Jupyter Notebook**
    打开并按顺序执行 `Qwen2.5-weitiaoban-3.ipynb` 中的所有代码单元。

##  B 文件结构

* `Qwen2.5-weitiaoban-3.ipynb`: 核心代码文件，包含了数据处理、模型加载、LoRA训练和测试的全部逻辑。
* `requirements.txt`: 项目运行所需的Python库列表。
* `.gitignore`: 定义了Git应忽略追踪的文件和目录，如模型输出等。

## 核心训练参数

* **基础模型**: `unsloth/Qwen2.5-0.5B-bnb-4bit`
* **数据集**: `LooksJuicy/ruozhiba-punchline`
* **训练轮数**: 10
* **学习率**: 2e-4
* **LoRA 秩 (r)**: 16

详细的超参数配置和训练结果请参考 Jupyter Notebook 内的说明和输出。
