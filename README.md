## 目录
- [1.0 传统抗体设计, 计算机辅助抗体设计及AI抗体设计](#10-传统抗体设计计算机辅助抗体设计及AI抗体设计)
  - [1.1 抗体简述](#11-抗体简述)
  - [1.2 抗体类型](#12-抗体类型)
    - [1.2.1 单克隆抗体（Monoclonal Antibodies, mAbs）](#121-单克隆抗体monoclonal-antibodies-mabs)
    - [1.2.2 纳米抗体（Nanobody）](#122-纳米抗体nanobody)
    - [1.2.3 抗体偶联药物（ADCs）](#123-抗体偶联药物adcs)
    - [1.2.4 双特异性抗体（BsAbs）](#124-双特异性抗体bsabs)
    - [1.2.5 三特异性抗体（Trispecific Antibodies）](#125-三特异性抗体trispecific-antibodies)
  - [1.3 传统抗体设计的主要技术](#13-传统抗体设计的主要技术)
    - [1.3.1 基于体内免疫的方法](#131-基于体内免疫的方法)
    - [1.3.2 基于体外展示的筛选方法](#132-基于体外展示的筛选方法)
    - [1.3.3 基于单细胞分析的方法](#133-基于单细胞分析的方法)
    - [1.3.4 基于原生B细胞库的抗体筛选方法](#134-基于原生b细胞库的抗体筛选方法)
    - [1.3.5 抗体人源化](#135-抗体人源化)
    - [1.3.6 亲和力成熟](#136-亲和力成熟)
  - [1.4 计算机辅助抗体设计（Computer-Aided Antibody Design, CAAD）](#14-计算机辅助抗体设计computer-aided-antibody-design-caad)
    - [1.4.1 抗体与抗原的结构建模](#141-抗体与抗原的结构建模)
    - [1.4.2 抗体与抗原结合位点的预测](#142-抗体与抗原结合位点的预测)
    - [1.4.3 抗体-抗原复合物结构预测](#143-抗体-抗原复合物结构预测)
    - [1.4.4 抗体人源化](#144-抗体人源化)
    - [1.4.5 抗体亲和力提升](#145-抗体亲和力提升)
  - [1.5 AI辅助抗体设计（AI-aided Antibody Design, AIAD）](#15-ai辅助抗体设计ai-aided-antibody-design-aiad)
    - [1.5.1 全新设计CDR3](#151-全新设计cdr3)
    - [1.5.2 CDR1/2/3综合优化](#152-cdr123综合优化)
    - [1.5.3 AI模型生成序列](#153-ai模型生成序列)
    - [1.5.4 AI抗体人源化设计](#154-ai抗体人源化设计)
    - [1.5.5 AI抗体亲和力成熟度](#155-ai抗体亲和力成熟度)
  - [1.6 本章结语](#16-本章结语)

- [2.0 抗体/抗原的结构模建 (Structural Modeling)](#20-抗体抗原的结构模建-structural-modeling)
  - [2.1 同源模建的技术原理](#21-同源模建的技术原理)
    - [2.1.1 同源模建的具体方法和流程](#211-同源模建的具体方法和流程)
    - [2.1.2 同源模建的优势与局限性](#212-同源模建的优势与局限性)
    - [2.1.3 深度学习驱动的结构模建：AlphaFold与RoseTTAFold](#213-深度学习驱动的结构模建alphafold与rosettafold)
  - [2.2 SWISS-MODEL](#22-swiss-model)
    - [2.2.1 SWISS-MODEL模板搜索和选择过程](#221-swiss-model模板搜索和选择过程)
    - [2.2.2 SWISS-MODEL模型构建过程](#222-swiss-model模型构建过程)
    - [2.2.3 SWISS-MODEL结构评估与验证](#223-swiss-model结构评估与验证)
    - [2.2.4 SWISS-MODEL模型优化与序列叠合问题](#224-swiss-model模型优化与序列叠合问题)
  - [2.3 RoseTTAFold](#23-rosettafold)
    - [2.3.1 RoseTTAFold的核心技术及原理](#231-rosettafold的核心技术及原理)
    - [2.3.2 RoseTTAFold在线预测步骤](#232-rosettafold在线预测步骤)
  - [2.4 AlphaFold](#24-alphafold)
    - [2.4.1 AlphaFold核心功能及原理](#241-alphafold核心功能及原理)
    - [2.4.2 已知的AlphaFold预测结构](#242-已知的alphafold预测结构)
    - [2.4.3 在线使用AlphaFold2/3进行预测](#243-在线使用alphafold23进行预测)
  - [2.5 本章结语](#25-本章结语)

- [3.0 抗体-抗原结合模式预测（Binding Mode Prediction）](#30-抗体抗原结合模式预测binding-mode-prediction)
  - [3.1 蛋白-蛋白结合模式预测的原理](#31-蛋白蛋白结合模式预测的原理)
    - [3.1.1 蛋白-蛋白对接的原理](#311-蛋白蛋白对接的原理)
    - [3.1.2 蛋白-蛋白对接的详细流程](#312-蛋白蛋白对接的详细流程)
    - [3.1.3 构象搜索与评分](#313-构象搜索与评分)
    - [3.1.4 结果优化与验证](#314-结果优化与验证)
    - [3.1.5 AlphaFold在蛋白-蛋白对接中的应用](#315-alphafold在蛋白蛋白对接中的应用)
    - [3.1.6 蛋白-蛋白对接的工具与软件](#316-蛋白蛋白对接的工具与软件)
  - [3.2 ClusPro](#32-cluspro)
    - [3.2.1 ClusPro算法概述及工作原理](#321-cluspro算法概述及工作原理)
    - [3.2.2 ClusPro服务器(网站)的使用方法与步骤](#322-cluspro服务器网站的使用方法与步骤)
    - [3.2.3 ClusPro技术优势](#323-cluspro技术优势)
    - [3.2.4 ClusPro局限性](#324-cluspro局限性)
  - [3.3 AlphaFold服务器](#33-alphafold服务器)
    - [3.3.1 AlphaFold概述](#331-alphafold概述)
    - [3.3.2 AlphaFold服务器的使用方法与步骤](#332-alphafold服务器的使用方法与步骤)
  - [3.4 AF2Complex](#34-af2complex)
    - [3.4.1 AF2Complex概述](#341-af2complex概述)
    - [3.4.2 下载AF2Complex](#342-下载af2complex)
    - [3.4.3 下载遗传数据库](#343-下载遗传数据库)
    - [3.4.4 下载其他组件](#344-下载其他组件)
    - [3.4.5 案例演示1：gp120与J3用AF2Complex模建](#345-案例演示1gp120与j3用af2complex模建)
    - [3.4.6 案例演示2：利用AF2Complex进行CD276与抗体库的筛选](#346-案例演示2利用af2complex进行cd276与抗体库的筛选)
  - [3.5 AlphaFold 3](#35-alphafold-3)
    - [3.5.1 AlphaFold 3的本地安装](#351-alphafold-3的本地安装)
    - [3.5.2 AlphaFold 3运行](#352-alphafold-3运行)
    - [3.5.3 AlphaFold 3的结果解读](#353-alphafold-3的结果解读)
    - [3.5.4 AlphaFold3进行CD276与抗体库的筛选](#354-alphafold3进行cd276与抗体库的筛选)
  - [3.6 本章结语](#36-本章结语)

- [4. 扩散模型（Diffusion）蛋白质序列从头设计](#4-扩散模型Diffusion蛋白质序列从头设计)
  - [4.1 Diffusion模型的原理及框架](#41-Diffusion模型的原理及框架)
    - [4.1.1 Diffusion的扩散框架](#411-Diffusion的扩散框架)
    - [4.1.2 预测过程](#412-预测过程)
    - [4.1.3 噪声引入与去噪过程](#413-噪声引入与去噪过程)
    - [4.1.4 损失函数计算](#414-损失函数计算)
    - [4.1.5 Self-Condition训练技巧](#415-Self-Condition训练技巧)
  - [4.2 RFDiffusion的搭建及调试](#42-RFDiffusion的搭建及调试)
    - [4.2.1 克隆 RFdiffusion 仓库](#421-克隆-RFdiffusion-仓库)
    - [4.2.2 下载模型权重文件](#422-下载模型权重文件)
    - [4.2.3 安装 SE3-Transformer](#423-安装-SE3-Transformer)
    - [4.2.4 获取 PPI Scaffold 示例](#424-获取-PPI-Scaffold-示例)
    - [4.2.5 运行扩散脚本](#425-运行扩散脚本)
    - [4.2.6 基本执行 - 无条件单体设计](#426-基本执行-无条件单体设计)
    - [4.2.7 图案支架构建（Motif Scaffolding）](#427-图案支架构建Motif-Scaffolding)
    - [4.2.8 部分扩散（Partial Diffusion）](#428-部分扩散Partial-Diffusion)
    - [4.2.9 结合物设计（Binder Design）](#429-结合物设计Binder-Design)
    - [4.2.10 绑定设计的实际考虑](#4210-绑定设计的实际考虑)
    - [4.2.11 对称寡聚物的生成](#4211-对称寡聚物的生成)
    - [4.2.12 Docker](#4212-Docker)
  - [4.3 RFDiffusion的案列解析](#43-RFDiffusion的案列解析)
    - [4.3.1 任务1：无条件蛋白单体生成（Unconditional Protein Monomer Generation）](#431-任务1无条件蛋白单体生成Unconditional-Protein-Monomer-Generation)
    - [4.3.2 任务2：高阶对称寡聚体生成（High-order Symmetric Oligomers Generation）](#432-任务2高阶对称寡聚体生成High-order-Symmetric-Oligomers-Generation)
    - [4.3.3 任务3：功能位点支架设计（Functional-site Scaffolding）](#433-任务3功能位点支架设计Functional-site-Scaffolding)
    - [4.3.4 任务4：从头蛋白与肽结合物设计（De novo Protein and Peptide Binder Design）](#434-任务4从头蛋白与肽结合物设计De-novo-Protein-and-Peptide-Binder-Design)
  - [4.4 本章结语](#44-本章结语)

- [5. AntiBMPNN抗体序列设计](#5-AntiBMPNN抗体序列设计)
  - [5.1 Training Set的采集及处理](#51-Training-Set的采集及处理)
    - [5.1.1 下载抗体/纳米抗体的结构](#511-下载抗体纳米抗体的结构)
    - [5.1.2 清理数据](#512-清理数据)
    - [5.1.3 去掉重复数据](#513-去掉重复数据)
  - [5.2 训练集（Training Set） 从.pdb 到.pt格式转换的处理过程](#52-训练集Training-Set-从pdb-到pt格式转换的处理过程)
    - [5.2.1 将 .pdb 转换为 .cif 格式](#521-将-pdb-转换为-cif-格式)
    - [5.2.2 通过 GitHub 下载 PDBX](#522-通过-GitHub-下载-PDBX)
    - [5.2.3 使用 bash 脚本转化为.pt文件](#523-使用-bash-脚本转化为pt文件)
  - [5.3 Training Data的构建](#53-Training-Data的构建)
  - [5.4 Antibody数据集的Training策略及步骤](#54-Antibody数据集的Training策略及步骤)
  - [5.5 Parameters的调整](#55-Parameters的调整)
  - [5.6 Backbone Noise对模型输出结果的影响](#56-Backbone-Noise对模型输出结果的影响)
  - [5.7 AntiBMPNN架构与训练性能](#57-AntiBMPNN架构与训练性能)
  - [5.8 Nanobody及Antibody的序列恢复度（Sequence Recovery）](#58-Nanobody及Antibody的序列恢复度Sequence-Recovery)
  - [5.9 AntiBMPNN的打分函数](#59-AntiBMPNN的打分函数)
  - [5.10 本章结语](#510-本章结语)

- [6. AntiBMPNN的部署及与其他方法的比较](#6-AntiBMPNN的部署及与其他方法的比较)
  - [6.1 AntiBMPNN的部署及测试](#61-AntiBMPNN的部署及测试)
    - [6.1.1 安装说明](#611-安装说明)
    - [6.1.2 设计新的抗体序列](#612-设计新的抗体序列)
  - [6.2 AntiBMPNN进行单点序列设计及实验验证结果](#62-AntiBMPNN进行单点序列设计及实验验证结果)
  - [6.3 使用AntiBMPNN设计HuJ3 CDR1并进行实验验证](#63-使用AntiBMPNN设计HuJ3-CDR1并进行实验验证)
  - [6.4 使用AntiBMPNN设计HuJ3 CDR3并进行实验验证](#64-使用AntiBMPNN设计HuJ3-CDR3并进行实验验证)
  - [6.5 使用AntiBMPNN设计CD16A VH抗体（D6）的CDR2并进行实验验证](#65-使用AntiBMPNN设计CD16A-VH抗体D6的CDR2并进行实验验证)
  - [6.6 基于实验数据的AntiBMPNN与现有抗体序列设计方法的比较分析](#66-基于实验数据的AntiBMPNN与现有抗体序列设计方法的比较分析)
  - [6.7 本章结语](#67-本章结语)

- [7. 扩散模型（Diffusion）蛋白质序列从头设计](#7-扩散模型Diffusion蛋白质序列从头设计)
  - [7.1 Diffusion模型的原理及框架](#71-Diffusion模型的原理及框架)
    - [7.1.1 Diffusion的扩散框架](#711-Diffusion的扩散框架)
    - [7.1.2 预测过程](#712-预测过程)
    - [7.1.3 噪声引入与去噪过程](#713-噪声引入与去噪过程)
    - [7.1.4 损失函数计算](#714-损失函数计算)
    - [7.1.5 Self-Condition训练技巧](#715-Self-Condition训练技巧)
  - [7.2 RFDiffusion的搭建及调试](#72-RFDiffusion的搭建及调试)
    - [7.2.1 克隆 RFdiffusion 仓库](#721-克隆-RFdiffusion-仓库)
    - [7.2.2 下载模型权重文件](#722-下载模型权重文件)
    - [7.2.3 安装 SE3-Transformer](#723-安装-SE3-Transformer)
    - [7.2.4 获取 PPI Scaffold 示例](#724-获取-PPI-Scaffold-示例)
    - [7.2.5 运行扩散脚本](#725-运行扩散脚本)
    - [7.2.6 基本执行 - 无条件单体设计](#726-基本执行-无条件单体设计)
    - [7.2.7 图案支架构建（Motif Scaffolding）](#727-图案支架构建Motif-Scaffolding)
    - [7.2.8 部分扩散（Partial Diffusion）](#728-部分扩散Partial-Diffusion)
    - [7.2.9 结合物设计（Binder Design）](#729-结合物设计Binder-Design)
    - [7.2.10 绑定设计的实际考虑](#7210-绑定设计的实际考虑)
    - [7.2.11 对称寡聚物的生成](#7211-对称寡聚物的生成)
    - [7.2.12 Docker](#7212-Docker)
  - [7.3 RFDiffusion的案列解析](#73-RFDiffusion的案列解析)
    - [7.3.1 任务1：无条件蛋白单体生成（Unconditional Protein Monomer Generation）](#731-任务1无条件蛋白单体生成Unconditional-Protein-Monomer-Generation)
    - [7.3.2 任务2：高阶对称寡聚体生成（High-order Symmetric Oligomers Generation）](#732-任务2高阶对称寡聚体生成High-order-Symmetric-Oligomers-Generation)
    - [7.3.3 任务3：功能位点支架设计（Functional-site Scaffolding）](#733-任务3功能位点支架设计Functional-site-Scaffolding)
    - [7.3.4 任务4：从头蛋白与肽结合物设计（De novo Protein and Peptide Binder Design）](#734-任务4从头蛋白与肽结合物设计De-novo-Protein-and-Peptide-Binder-Design)
  - [7.4 本章结语](#74-本章结语)

- [8.0 抗体序列人源化AI设计](#80-抗体序列人源化ai设计)
  - [8.1 抗体人源化的概述](#81-抗体人源化的概述)
    - [8.1.1 抗体人源化设计的主要原理、步骤及流程](#811-抗体人源化设计的主要原理步骤及流程)
    - [8.1.2 AI抗体人源化设计的原理](#812-ai抗体人源化设计的原理)
    - [8.1.3 人工智能辅助抗体人源化工具](#813-人工智能辅助抗体人源化工具)
  - [8.2 BioPhi人源化设计平台](#82-biophi人源化设计平台)
    - [8.2.1 BioPhi技术原理](#821-biophi技术原理)
    - [8.2.2 BioPhi应用](#822-biophi应用)
    - [8.2.3 BioPhi平台特点](#823-biophi平台特点)
    - [8.2.4 BioPhi算法框架](#824-biophi算法框架)
    - [8.2.5 BioPhi在线平台](#825-biophi在线平台)
  - [8.3 CUMAb抗体人源化与智能设计平台](#83-cumab抗体人源化与智能设计平台)
    - [8.3.1 CUMAb算法概述](#831-cumab算法概述)
    - [8.3.2 CUMAb应用与功能](#832-cumab应用与功能)
    - [8.3.3 CUMAb平台特点](#833-cumab平台特点)
    - [8.3.4 CUMAb的算法框架](#834-cumab的算法框架)
    - [8.3.5 CUMAb在线平台](#835-cumab在线平台)
  - [8.4 HuDiff基于深度学习的抗体人源化工具](#84-hudiff基于深度学习的抗体人源化工具)
    - [8.4.1 HuDiff简介（HuDiff-Ab及HuDiff-Nb）](#841-hudiff简介hudiff-ab及hudiff-nb)
    - [8.4.2 Conda环境](#842-conda环境)
    - [8.4.3 HuDiff-Ab的搭建及模型训练](#843-hudiff-ab的搭建及模型训练)
    - [8.4.4 HuDiff人源化设计](#844-hudiff人源化设计)
  - [8.5 本章结语](#85-本章结语)

- [9.0 AI抗体亲和力成熟度](#90-ai抗体亲和力成熟度)
  - [9.1 抗体亲和力成熟度的概述](#91-抗体亲和力成熟度的概述)
    - [9.1.1 体外亲和力成熟的需求与意义](#911-体外亲和力成熟的需求与意义)
    - [9.1.2 体外亲和力成熟的实验方法与技术挑战](#912-体外亲和力成熟的实验方法与技术挑战)
    - [9.1.3 计算方法在亲和力成熟中的应用](#913-计算方法在亲和力成熟中的应用)
    - [9.1.4 数据限制与AI模型的进展](#914-数据限制与ai模型的进展)
  - [9.2 亲和力成熟度计算的原理](#92-亲和力成熟度计算的原理)
    - [9.2.1 亲和力的定义与理论基础](#921-亲和力的定义与理论基础)
    - [9.2.2 分子模拟中的计算方法](#922-分子模拟中的计算方法)
    - [9.2.3 统计能量函数](#923-统计能量函数)
    - [9.2.4 基于人工智能的计算方法](#924-基于人工智能的计算方法)
    - [9.2.5 亲和力成熟的优化策略](#925-亲和力成熟的优化策略)
    - [9.2.6 实验验证与反馈迭代](#926-实验验证与反馈迭代)
  - [9.3 AntiBERTy](#93-antiberty)
    - [9.3.1 AntiBERTy 概述](#931-antiberty-概述)
    - [9.3.2 AntiBERTy 的技术框架](#932-antiberty-的技术框架)
    - [9.3.3 AntiBERTy 的工作原理](#933-antiberty-的工作原理)
    - [9.3.4 AntiBERTy 在亲和力成熟中的应用](#934-antiberty-在亲和力成熟中的应用)
    - [9.3.5 AntiBERTy 的安装](#935-antiberty-的安装)
  - [9.4 GearBind](#94-gearbind)
    - [9.4.1 GearBind模型的设计与多层次几何信息传递](#941-gearbind模型的设计与多层次几何信息传递)
    - [9.4.2 自监督预训练与泛化能力增强](#942-自监督预训练与泛化能力增强)
    - [9.4.3 模型性能与架构设计分析](#943-模型性能与架构设计分析)
    - [9.4.4 集成模型的优势与贡献分析](#944-集成模型的优势与贡献分析)
    - [9.4.5 HER2结合体测试集上的表现](#945-her2结合体测试集上的表现)
    - [9.4.6 CR3022和anti-5T4 UdAb的亲和力成熟实验](#946-cr3022和anti-5t4-udab的亲和力成熟实验)
    - [9.4.7 GearBind安装及应用](#947-gearbind安装及应用)
  - [9.5 本章结语](#95-本章结语)

- [10.0 ChatGPT在抗体设计中的应用](#100-chatgpt在抗体设计中的应用)
  - [10.1 ChatGPT的概述](#101-chatgpt的概述)
  - [10.2 ChatGPT的原理](#102-chatgpt的原理)
    - [10.2.1 Transformer架构](#1021-transformer架构)
    - [10.2.2 预训练和微调](#1022-预训练和微调)
    - [10.2.3 自注意力机制](#1023-自注意力机制)
    - [10.2.4 文本生成和调节层](#1024-文本生成和调节层)
    - [10.2.5 模型参数和扩展性](#1025-模型参数和扩展性)
    - [10.2.6 应用与限制](#1026-应用与限制)
  - [10.3 Ollama及deepseek的安装与使用](#103-ollama及deepseek的安装与使用)
    - [10.3.1 安装WSL（Windows Subsystem for Linux）](#1031-安装wslwindows-subsystem-for-linux)
    - [10.3.2 进入 WSL 环境并设置根目录](#1032-进入-wsl-环境并设置根目录)
    - [10.3.3 下载 Ollama 平台](#1033-下载-ollama-平台)
    - [10.3.4 启动和管理 Ollama](#1034-启动和管理-ollama)
    - [10.3.5 下载模型](#1035-下载模型)
    - [10.3.6 安装图形界面 Open WebUI](#1036-安装图形界面-open-webui)
  - [10.4 ChatGPT在抗体数据处理的脚本生成及解析](#104-chatgpt在抗体数据处理的脚本生成及解析)
    - [10.4.1 单个请求的ChatGPT生成脚本](#1041-单个请求的chatgpt生成脚本)
    - [10.4.2 多次请求生成并修改脚本](#1042-多次请求生成并修改脚本)
    - [10.4.3 ChatGPT生成的.cif.gz分类文件](#1043-chatgpt生成的cifgz分类文件)
    - [10.4.4 ChatGPT生成统计 .pdb 文残基数量并移动特定文件](#1044-chatgpt生成统计-pdb-文残基数量并移动特定文件)
    - [10.4.5 ChatGPT生成统计 .pdb 文残基数量并复制符合条件的文件](#1045-chatgpt生成统计-pdb-文残基数量并复制符合条件的文件)
    - [10.4.6 ChatGPT生成脚本将抗体的数据集随机分割为训练、验证和测试集](#1046-chatgpt生成脚本将抗体的数据集随机分割为训练验证和测试集)
    - [10.4.7 ChatGPT生成读取日志文件并绘制训练与验证曲线以比较困惑度](#1047-chatgpt生成读取日志文件并绘制训练与验证曲线以比较困惑度)
    - [10.4.8 ChatGPT生成读取日志文件并绘制训练与验证曲线以比较准确率](#1048-chatgpt生成读取日志文件并绘制训练与验证曲线以比较准确率)
    - [10.4.9 ChatGPT生成统计 .pdb 文残基数量并移动特定文件](#1049-chatgpt生成统计-pdb-文残基数量并移动特定文件)
    - [10.4.10 ChatGPT生成SeqLogo的图片](#10410-chatgpt生成seqlogo的图片)
    - [10.4.11 ChatGPT生成脚本来处理.fas文件到.json文件以便进行AlphaFold3](#10411-chatgpt生成脚本来处理fas文件到json文件以便进行alphafold3)
  - [10.5 本章结语](#105-本章结语)


