# openai-evals-quickstart

OpenAI的Evals框架是一个用于评估大型语言模型（LLMs）或基于LLMs构建的系统的工具。以下是一个快速入门指南，用于如何使用Evals框架进行评估，包括所需的完整代码。

首先，确保你有Python 3.9或更高版本，并且已经安装了Git和Git-LFS。这些是运行Evals所必需的[1][5][7]。

接下来，你需要设置你的OpenAI API密钥。获取API密钥后，使用`OPENAI_API_KEY`环境变量指定它[1][5][7]。

然后，你可以通过以下命令克隆Evals仓库并安装必要的依赖项：

```bash
git clone https://github.com/openai/evals.git
cd evals
pip install -e .
```

使用`-e`选项意味着你对Evals所做的更改将立即反映出来，无需重新安装[1][5][7]。

如果你只想运行现有的评估而不是创建新的评估，你可以通过pip安装Evals包：

```bash
pip install evals
```

接下来，使用Git-LFS获取Evals注册表中的数据：

```bash
git lfs fetch --all
git lfs pull
```

如果你只想获取特定评估的数据，可以使用以下命令：

```bash
git lfs fetch --include=evals/registry/data/${your_eval}
git lfs pull
```

其中`${your_eval}`是你想要获取数据的评估名称[1][5][7]。

现在，你可以运行一个现有的评估。Evals框架提供了多种评估模板，你可以根据需要选择一个。例如，如果你想要运行一个基本的评估，可以使用以下命令：

```bash
python -m evals.cli run --eval_id=<eval_id>
```

其中`<eval_id>`是你想要运行的评估的ID[1][4]。

如果你想要创建一个新的评估，你需要提供你的数据以JSON格式，并指定你的评估参数以YAML格式。你可以参考`build-eval.md`文件了解如何构建评估，以及查看`examples`文件夹中的Jupyter笔记本来快速开始[1]。

请注意，运行评估可能会产生与使用OpenAI API相关的成本，因此在运行评估之前，请确保了解这些成本[1]。

以上步骤提供了一个使用OpenAI Evals框架进行评估的快速入门指南。由于你提到没有手指，以上代码可以直接复制粘贴到终端或命令行界面中执行。

Citations:
[1] https://github.com/openai/evals
[2] https://www.medsci.cn/article/show_article.do?id=d659e76753d0
[3] https://chatgpt123.com/18369.html
[4] https://cookbook.openai.com/examples/evaluation/getting_started_with_openai_evals
[5] https://www.oschina.net/p/evals
[6] https://cloud.tencent.com/developer/news/1170800
[7] https://aigc.luomor.com/2023/04/06/evals-openai-%E6%A8%A1%E5%9E%8B%E8%AF%84%E4%BC%B0%E6%A1%86%E6%9E%B6/
[8] https://github.com/DjangoPeng/openai-quickstart
[9] https://hub.baai.ac.cn/view/24840
[10] https://hackernoon.com/zh/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8openai%E5%BE%AE%E8%B0%83%E5%92%8C%E4%BC%98%E5%8C%96gpt%E5%8A%A9%E6%89%8B
[11] https://juejin.cn/post/7304631212718407720
[12] https://chatgpt123.com/18265.html
[13] https://blog.csdn.net/gitblog_00033/article/details/136832429
[14] https://www.yunqiic.com/2023/04/06/evals-openai-%E6%A8%A1%E5%9E%8B%E8%AF%84%E4%BC%B0%E6%A1%86%E6%9E%B6/
[15] https://itdog.com.hk/2023/03/20/openai-%E8%88%87-chatgpt-%E7%9B%B8%E9%97%9C%E9%96%8B%E7%99%BC%E5%B7%A5%E5%85%B7%E4%BB%8B%E7%B4%B9/
[16] https://www.xujun.org/note-159590.html
[17] https://www.yundongfang.com/Yun220427.html
[18] http://www.robotcz.com/third_1.asp?txtid=496
[19] https://aigc.7otech.com/2023/04/06/evals-openai-%E6%A8%A1%E5%9E%8B%E8%AF%84%E4%BC%B0%E6%A1%86%E6%9E%B6/
