# 易宏基因组——简单易用的宏基因组分析流程

# EasyMetagenome - A user-friendly and flexible pipeline for shotgun metagenomic analysis in microbiome research

版本Version：v1.23

更新时间Update：2024/11/26

![image](http://www.imeta.science/github/EasyMetagenome/result/EasyMetagenomePipeline.jpg)

**图1. 易宏基因组的工作流程：分析宏基因组测序从原始数据到物种和功能组成表.**

从原始数据到物种和功能组成表可分为四步进行：1.数据的预处理,包括分析前准备工作(安装软件和数据库、环境变量设置和元数据和序列文件检查)、Fastp质量控制和Kneaddata去宿主。2.基于读长分析(HUMAnN3+MetaPhlAn4+Kraken2), 包括准备HUMAnN输入文件、HUMAnN计算物种和功能组成、物种组成表整理、功能组成分析、GraPhlAn图绘制、LEfSe差异分析物种和Kraken2+Bracken物种注释和丰度估计。3.组装分析，包括组装、基因预测/去冗余和定量、功能基因注释和Kraken2基因物种注释。4.分箱挖掘单菌基因组，包括MetaWRAP混合样本分箱、dRep去冗余种/株基因组集、CoverM基因组定量、GTDB-tk物种注释和进化树

**Figure 1. EasyMetagenome Pipeline from raw data to taxonomic & functional table for analyzing metagenomic sequencing.**

The process from raw data to species and functional composition tables can be divided into four steps: 1. Data preprocessing, including pre-analysis preparation (installing software and database, setting environmental variables and checking metadata and sequence files), Fastp quality control and Kneaddata host removal. 2. Read-based analysis (HUMAnN3+MetaPhlAn4+Kraken2), including preparation of HUMAnN input files, calculation of species and functional composition by HUMAnN, arrangement of species composition tables, functional composition analysis, GraPhlAn map drawing, LEfSe differential analysis of species and Kraken2+Bracken species annotation and abundance estimation. 3. Assembly analysis, including assembly, gene prediction/de-redundancy and quantification, functional gene annotation and Kraken2 gene species annotation. 4. Binning and mining of single bacterial genomes, including MetaWRAP mixed sample binning, dRep de-redundant species/strain genome sets, CoverM genome quantification, GTDB-tk species annotation and evolutionary tree.

## 文件介绍File introduction

## 0Install.sh：软件和数据库安装Software and database installation

### 一、数据预处理 1. Data preprocessing

*   初始化 Initialization

    1.  EasyMetagenome流程安装 EasyMetagenome pipeline installation
    2.  EasyMicrobiome软件和数据库合集 EasyMicrobiome software and database collection
    3.  软件管理器Conda Software Manager Conda
*   质控Quality control: kneaddata/fstqc/multiqc/fastp

    1.  方法1.kneaddata直接安装 Method 1. kneaddata direct installation
    2.  方法2.kneaddata下载解压安装 Method 2. Download and decompress kneaddata and install it
    3.  kneaddata安装测试 kneaddata installation test
    4.  kneaddata数据库下载 kneaddata database download
    5.  kneaddata自定义参考基因组索引 kneaddata custom reference genome index

### 二、基于读长分析 2. Read-based (HUMAnN3/Kraken2)

*   宏基因组基于读长的分析 Metagenomic read-based analysis（HUMAnN3/MetaPhlAn4/GraPhlAn）

    1.  HUMAnN3直接安装 HUMAnN3 direct installation
    2.  HUMAnN3解包安装 HUMAnN3 unpacking and installation
    3.  HUMAnN3安装测试 HUMAnN3 installation test
    4.  HUMAnN3物种和功能数据库 HUMAnN3 species and function database
    5.  MetaPhlAn4物种数据库 MetaPhlAn4 species database
*   物种注释 Species annotation (Kraken2/bracken/krakentools/krona)

    1.  Kraken2解包安装 Unpack and install Kraken2
    2.  Kraken2安装指定版本 Install the specified version of Kraken2
    3.  Kraken2数据库安装 Kraken2 Database Installation

### 三、组装 3. Assemble-based

*   组装、注释和定量 Assembly, annotation, and quantification (megahit/spades/quast/cd-hit/emboss/salmon/prodigal)

    1.  megahit解包安装 Megahit Unpacking and Installation
    2.  megahit直接安装 megahit direct installation
    3.  megahit安装后测试 megahit post-installation test
*   蛋白同源综合注释 Protein homology comprehensive annotation (eggNOG)

    1.  eggNOG解包安装 Unpack and install eggNOG
    2.  eggNOG直接安装 eggNOG direct installation
    3.  eggNOG安装测试 eggNOG installation test
    4.  eggNOG数据库安装  eggNOG database installation
    5.  碳水化合物CAZy Carbohydrates CAZy
*   抗生素抗性基因 Antibiotic resistance genes (CARD/rgi)

    1.  rgi解包安装 rgi unpacking installation
    2.  rgi直接安装 rgi direct installation
    3.  rgi版本和数据库部署 rgi version and database deployment

### 四、分箱挖掘单菌基因组 4. Binning and mining of single bacterial genomes

*   metawrap分箱 metawrap binning

    1.  metawrap下载安装 Download and install metawrap
    2.  metawrap conda安装 metawrap conda installation
    3.  metawrap相关数据库 Metawrap related database
*   drep基因组去冗余 drep genome redundancy removal

    1.  drep 基因组去冗余解包安装 drep genome redundancy removal package installation
    2.  drep 基因组去冗余直接安装 drep genome redundancy removal direct installation
    3.  drep 数据库构建 drep database construction
*   coverm基因组定量 CoverM genome quantification
*   GTDB细菌基因组注释和进化分析 GTDB bacterial genome annotation and evolutionary analysis

    1.  GTDB-Tk直接安装 GTDB-Tk direct installation
    2.  GTDB-Tk解包安装 GTDB-Tk Unpack and Install
    3.  GTDB-Tks数据库安装 GTDB-Tks database installation

### 五、单菌基因组、病毒组等其他软件 5. Single bacterial genome, virus group and other software

*   CheckM2

### 常见问题 Frequently asked questions

*   软件和数据库国内备份 Domestic backup of software and database

    1.  国家微生物科学数据中心 —— 数据下载 National Microbial Science Data Center —— Data Download
    2.  百度云备份链接 Baidu Cloud backup link
*   kneaddata常见问题 kneaddata frequently asked questions

    1.  kneaddata运行提示java版本不支持 kneaddata prompts that the java version is not supported when running
    2.  解压失败-重新下载再安装 Unzip failed - re-download and install
    3.  Lefse在Rstudio中运行命令调用R版本问题的解决 Solution to the problem of calling R version by running command in Rstudio
*   Kraken2

    1.  定制数据库 Custom database
    2.  Perl版本不对 Wrong Perl version
*   salmon手动安装和使用 Manual installation and use of salmon
*   MetaWRAP分箱 MetaWRAP Binning

    1.  shorten\_contig\_names.py报错 shorten\_contig\_names.py reports an error
    2.  绘图plot\_binning\_results.py报错 Plotting plot\_binning\_results.py reports an error
    3.  blast版本不兼容 Incompatible blast version

### 附录 Appendix

*   Conda安装小工具 Conda installation gadget
*   宿主参考基因组下载 Host reference genome download
*   KEGG层级注释整理 KEGG hierarchical annotation
*   毒力因子数据库VFDB Virulence Factor Database (VFDB)
*   宏基因组基于读长的分析 Metagenomic read-based analysis (HUMAnN2/Metaphlan2/graphlan)

    1.  HUMAnN2解包安装 HUMAnN2 unpacking and installation
    2.  HUMAnN2直接安装 HUMAnN2 Direct Installation
    3.  HUMAnN2安装测试 HUMAnN2 installation test
    4.  HUMAnN2物种和功能数据库 HUMAnN2 species and function database
    5.  删除env环境 Delete the env environment



## 1Pipeline.sh：分析流程Analysis pipeline

### 一、数据预处理 1. Data preprocessing

*   1.1 准备工作 Preparing
*   1.2 Fastp质量控制 Quality Control Using Fastp
*   1.3 KneadData去宿主 Host removal Using KneadData

### 二、基于读长分析 2. Read-based (HUMAnN3+MetaPhlAn4+Kraken2)

*   2.1 准备HUMAnN输入文件 Preparing HUMAnN input files
*   2.2 HUMAnN计算物种和功能组成 HUMAnN calculation of species and functional composition
*   2.3 物种组成表 Species composition table
*   2.4 功能组成分析 Functional composition analysis

    1.  差异比较和柱状图 Difference comparison and histogram
    2.  KEGG注释 KEGG annotation
*   2.5 GraPhlAn图 GraPhlAn Diagram
*   2.6 LEfSe差异分析物种 LEfSe differential analysis species
*   2.7 Kraken2+Bracken物种注释和丰度估计 Kraken2+Bracken species annotation and abundance estimation

    1.  Kraken2物种注释 Kraken2 species annotation
    2.  Bracken丰度估计 Bracken abundance estimate

### 三、组装分析流程 3. Assemble-based

*   3.1 组装 Assembly

    1.  MEGAHIT组装 MEGAHIT Assembly
    2.  (可选)metaSPAdes精细组装 (Optional) metaSPAdes fine assembly
    3.  QUAST评估 QUAST Evaluation
*   3.2 基因预测、去冗余和定量Gene prediction, cluster & quantitfy

    1.  metaProdigal基因预测 metaProdigal gene prediction
    2.  cd-hit基因聚类/去冗余 cd-hit cluster & redundancy
    3.  salmon基因定量 Salmon gene quantification
*   3.3 功能基因注释Functional gene annotation

    1.  eggNOG基因注释 eggNOG gene annotation(COG/KEGG/CAZy)
    2.  CAZy碳水化合物酶 CAZy Carbohydrate Enzymes
    3.  CARD耐药基因 CARD resistance gene
*   3.4 Kraken2基因物种注释 Species gene annotation using Kraken2&#x20;

### 四、分箱挖掘单菌基因组 4. Binning and mining of single bacterial genomes

*   4.1 MetaWRAP混合样本分箱 MetaWRAP mixed sample binning

    1.  数据和环境变量 Data and enviroment
    2.  分箱 Binning
    3.  分箱提纯 Bin refinement
*   (可选Opt)单样本分箱 Single sample binning
*   (可选Opt)分组分箱 Subgroup binning
*   4.2 dRep去冗余种/株基因组集 dRep de-redundant species/strain genome collection
*   4.3 CoverM基因组定量 CoverM genome quantification
*   4.4 GTDB-tk物种注释和进化树 GTDB-tk species annotation and evolutionary tree

### 五、(可选)单菌基因组 5. (Optional) Single bacterial genome

*   5.1 Fastp质量控制 Fastp Quality Control
*   5.2 metaspades组装 Metaspades assembly
*   5.3 checkm质量评估 checkm quality assessment
*   5.4 混菌metawarp分箱 Mixed Metawarp binning
*   5.5 drep基因组去冗余 drep genome redundancy removal
*   5.6 gtdb物种注释 GTDB species annotation
*   5.7 功能注释 Functional annotation (eggnog/dbcan/arg/antismash)

### 六、(可选)泛基因组 6. (Optional) Pan-genome

*   6.1 从NCBI下载基因组 Download genome from NCBI
*   6.2 建立CONTIGS库 Building a CONTIGS library
*   6.3 泛基因组分析 Pan-genome analysis

### 附录：常见分析问题和补充代码 Appendix: Common analysis problems and additional

计算时间统计表 Computation time statistics table

补充代码 Supplementary scripts

KneadData质控去宿主 Quality Control De-hosting Using KneadData

HUMANN物种功能定量 HUMANN species function quantification

LEfSe生物标志鉴定 LEfSe biomarker identification

Kraken2物种分类 Kraken2 Species Classification

Megahit组装 Megahit Assembly

二三代混合组装 Second and third generation mixed assembly

prodigal基因序列 prodigal gene sequence

cd-hit基因去冗余 CD-hit gene redundancy removal

salmon基因定量 Salmon gene quantification

基因功能数据库 Gene Function Database

MetaWRAP分箱 MetaWRAP Binning



## 2StatPlot.sh：统计和可视化 Statistics and visualization

*   环境设置 Settings
*   Metaphlan4物种数据 Metaphlan4 species data

    1.  Alpha多样性指数计算 Alpha diversity index calculation
    2.  绘制alpha多样性指数箱线图 Draw a box plot of the alpha diversity index
    3.  批量计算6种指数的箱线图+统计 Batch calculation of box plots + statistics of 6 indices
    4.  Beta多样性距离矩阵计算 Beta diversity distance matrix calculation
    5.  Beta多样性PCoA分析 Beta diversity PCoA analysis
    6.  热图 Heatmap
    7.  不同分类级别树状图 Dendrograms at different classification levels
    8.  维恩图 Venn
    9.  丰度箱线图 Abundance box plot
    10. 堆叠柱状图 Stacked bar plot
    11. STAMP组间比较图 Group comparison using STAMP
    12. MaAsLin2差异物种分析火山图 MaAsLin2 differential species analysis volcano plot
    13. 物种稀疏相关网络(SparCC)分析 Species sparse correlation network (SparCC) analysis
*   HUMAnN3功能数据 HUMAnN3 functional data

    1.  分组聚类热图 Grouped cluster heatmap
*   kraken2物种数据 Kraken2 species data

    1.  Alpha多样性 Alpha diversity
    2.  热图 Heatmap
    3.  箱线图(kraken2) Box plot
*   kraken2-braken2物种数据 kraken2-braken2 species data

    1.  Alpha多样性 Alpha diversity
    2.  Beta多样性 Beta diversity
    3.  堆叠柱状图 Stacked bar plot
    4.  STAMP图  Group comparison using STAMP
*   table2itol基因组进化树注释 Genome evolutionary tree annotation using table2itol
*   MAGs分析数据 MAGs data

    1.  MAGs与样本稀疏曲线 MAGs and sample rarefaction curves
    2.  MAGs不同功能数据库注释结果比较UpSet图 UpSet diagram comparing annotation results of different functional databases of MAGs
    3.  MAGs功能通路桑基图 Sankey diagram of MAGs functional pathway
    4.  MAGs完整性和污染率关系图 MAGs integrity and contamination rate relationship diagram
    5.  MAGs系统发育分析树状图 Dendrogram of phylogenetic analysis of MAGs
    6.  MAGs耐药基因丰度热图 Heatmap of MAGs resistance gene abundance
*   单菌基因组注释和绘图 Single bacterial genome annotation and mapping
*   宏基因组数据泛基因组分析绘图 Pan-genome analysis and mapping of metagenomic data
*   附录 Appendix

    1.  windows换行符处理 Windows line break processing
    2.  表格合并 Table Merge



Shell脚本(.sh)兼容Markdown格式，可使用有道云笔记、VSCode等工具中Markdown格式查看，有目录导航更方便浏览和阅读。

The Shell scripts are compatible with the Markdown format, which can be viewed in the Markdown editor, such as YoudaoCloudNotes, VSCode, and the menu navigation is more convenient for browsing and reading.

各文档附录部分为常见问题，供参考。

The appendices of each document are frequently asked questions for reference.

## 使用方法Instructions

在64位版本Linux系统，如Ubuntu 20.04+ / CentOS 7.7+，按代码文件0，1，2顺序逐个运行

In 64-bit version Linux system, such as Ubuntu 20.04+ / CentOS 7.7+, run step by step according to scripts 0, 1, 2.

在终端命令行，或RStudio的Terminal环境下使用，可以有道云笔记中显示代码目录，方便预览大纲

Used in the terminal command line or RStudio's terminal environment. You can display the code menu in Youdaoyun Notes, which is convenient for previewing the outline

## Citation (引文)

If used this script, please cited

使用此脚本，请引用下文：

**Yong-Xin Liu**, Lei Chen, Tengfei Ma, Xiaofang Li, Maosheng Zheng, Xin Zhou, Liang Chen, Xubo Qian, Jiao Xi, Hongye Lu, Huiluo Cao, Xiaoya Ma, Bian Bian, Pengfan Zhang, Jiqiu Wu, Ren-You Gan, Baolei Jia, Linyang Sun, Zhicheng Ju, Yunyun Gao, Tao Wen, **Tong Chen**. 2023. EasyAmplicon: An easy-to-use, open-source, reproducible, and community-based pipeline for amplicon data analysis in microbiome research. **iMeta** 2: e83. <https://doi.org/10.1002/imt2.83>

**Yong-Xin Liu**, Yuan Qin, **Tong Chen**, Meiping Lu, Xubo Qian, Xiaoxuan Guo, Yang Bai. 2021. A practical guide to amplicon and metagenomic analysis of microbiome data. Protein & Cell 12: 315-330. <https://doi.org/10.1007/s13238-020-00724-8> (Highly Cited)

Copyright 2016-2025 Yong-Xin Liu <liuyongxin@caas.cn>, Tong Chen <chent@nrc.ac.cn>
