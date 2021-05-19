# 软件和数据库清单(db)

扩增子、宏基因组分析常用软件、数据库、脚本文件

Scripts and databases for amplicon and metagenome

版本：EasyMetagenome v1.11

更新时间：2021/5/19

## 软件

- linux：Linux系统下分析软件
    - microbiome_helper：metaphlan2结果转换STAMP格式(metaphlan_to_stamp)，picurst结果功能组成绘图(plot_metagenome_contributions.R)
    - Miniconda2-latest-Linux-x86_64.sh：Conda安装程序
    - qiime2-2021.2.tar.gz：QIIME2安装包，解压至conda的envs目录可用
    - qiime2-2021.2-py36-linux-conda.yml：QIIME2软件安装清单，使用conda在线安装
    - sparcc.zip：sparcc网络分析python脚本
    - usearch：扩增子分析流程
    - vsearch：扩增子分析流程(免费64位版usearch)
- mac：Mac系统下分析软件
    - csvtk：表格分析工具
    - iqtree：进化树构建
    - qiime2-2021.2-py36-osx-conda.yml：QIIME2软件安装清单，使用conda在线安装
    - R-4.0.4.pkg：R语言安装包
    - RStudio-1.4.1106.dmg：RStudio安装包
    - rush：并行管理工具
    - seqkit：序列处理工具
    - taxonkit：NCBI分类处理工具
    - usearch：扩增子分析流程
    - vsearch：扩增子分析流程(免费64位版usearch)
- win：Windows系统下分析软件
    - STAMP2.1.3：微生物组图形界面差异分析工具
    - 4.0.zip：R语言常用400+包合集，解压至R包安装位置
    - Adobe_Illustrator_CC_2018_v22.1.0.314_x64_zh_CN_Portable.7z：图片拼图、模式图绘制工具
    - csvtk.exe：表格分析工具
    - Cytoscape_3_8_2_windows_64bit.exe：网络分析安装包
    - epp510_1828_64bit.exe：文本编辑器
    - FileZilla_3.49.1_win64_sponsored-setup.exe：文件上传下载
    - gephi-0.9.2-windows.exe：网络图绘制工具
    - Git-2.30.2-64-bit.exe：提供Git bash环境
    - iqtree.exe：进化树构建
    - jdk-11.0.7_windows-x64_bin.exe：Java运行环境
    - libiomp5md.dll：动态库，运行中提示缺少时可添加至系统目录
    - muscle.exe：多序列比对工具
    - npp.7.8.9.Installer.x64.exe：文本编辑器NotePad++安装包
    - R-4.0.4-win.exe：R语言安装包
    - RStudio-1.4.1106.exe：RStudio安装包
    - rtools40-x86_64.exe：R源码安装时的编绎工具
    - rush.exe：并行管理工具
    - seqkit.exe：序列处理工具
    - taxonkit.exe：NCBI分类处理工具
    - usearch.exe：扩增子分析流程
    - vsearch.exe：扩增子分析流程(免费64位版usearch)
    - wget.exe：命令行下载工具

## 数据库

- gg：GreenGenes细菌16S数据库
    - gg_13_8_otus.tar.gz：13年8月更新OTU数据库，用于usearch有参定量和PICRUSt/BugBase功能预测、QIIME 2制作分类器
- kegg：KEGG数据库描述信息整理
    - KO_description.txt：KO编号对应的功能描述
    - KO_path.list：KO对应通路(Pathway)
    - ko00001.tsv：KO对应描述、通路、超级通路和分类信息
- usearch：usearch/vsearch物种分类sintax命令使用数据库
    - rdp_16s_v16_sp.fa.gz：16S的RDP16数据库，usearch作者整理，更16S、ITS和18S数据库见 http://www.drive5.com/usearch/manual/sintax_downloads.html
    - rdp_16s_v18.fa.gz：16S的RDP18数据库，易生信团队2021年基于RDP数据库整理
    - utax_reference_dataset_all_04.02.2020.fasta.gz：ITS注释数据库，可从UNITE下载

## 脚本 

- 使用说明：分析常用脚本类型
    - .R文件为R脚本，使用Rscript命令执行；
    - .sh为Shell脚本，使用/bin/bash命令执行；
    - .pl为Perl脚本，使用perl命令执行；
    - .py为Python脚本，使用python执行，注意还分为python2和python3两种

- script：微生物组数据分析
    - BugBase：16S扩增子表型预测R脚本和数据库
    - FAPROTAX_1.2.4：16S扩增子元素循环预测Python脚本和数据库
    - table2itol：iTOL进化树注释文件制作R脚本
    - alpha_barplot.R：Alpha多样性指数柱状图+标准差图绘制
    - alpha_boxplot.R：Alpha多样性指数箱线图+统计绘制
    - alpha_rare_curve.R：usearch计算稀释曲线可视化
    - beta_cpcoa.R：基于距离矩阵开展限制性PCoA分析及可视化散点图+分组着色+置信椭圆，要求至少3个分组
    - beta_pcoa.R：基于距离矩阵的主坐标PCoA分析及可视化散点图+分组着色+置信椭圆+组间两两统计
    - BetaDiv.R：更多Beta多样性分析，如PCA、PCoA、NMDS、LDA、CCA、RDA等
    - compare.R：两组比较，支持t.test、wilcox、edgeR三种方法
    - compare_heatmap.R/sh：基于两组比较结果绘制热图
    - compare_manhattan.sh：基于两组比较结果绘制曼哈顿图
    - compare_volcano.R：基于两组比较结果绘制火山图
    - faprotax_report_sum.pl：FARPROTAX分析结果报告整理
    - filter_feature_table.R：按频率过滤OTU表
    - format_dbcan2list.pl：dbcan数据库注释结果整理
    - format2lefse.R：OTU表和物种注释生成LEfSe输入文件
    - format2stamp.R：OTU表和物种注释生成STAMP输入文件
    - kegg_ko00001_htext2tsv.pl：KEGG注释结果整理
    - kraken2alpha.R：Kraken2结果整理、抽平和alpha多样性指数计算
    - mat_gene2ko.R：按类型折叠表格
    - metaphlan_boxplot.R：metaphalan2结果可视化为箱线图
    - metaphlan_hclust_heatmap.R：metaphalan2结果可视化为聚类热图
    - metaphlan_to_stamp.pl：metaphalan2结果转换为STAMP格式
    - otu_mean.R：OTU表统计各组均值
    - otutab_filter_nonBac.R：16S的OTU表按sintax注释结果选择细菌、古菌且过滤叶绿体和线粒体
    - otutab_filter_nonFungi.R：ITS的OTU表选择真菌
    - otutab_freq2count.R：转换频率为伪整数，用于要求整型输入的分析，如多样性、edgeR差异分析等
    - otutab_rare.R：OTU表抽平
    - plot_metagenome_contributions.R：PICRUSt结果物种的功能组成绘制
    - sp_pheatmap.sh：绘制热图
    - sp_vennDiagram.sh：绘制维恩图
    - summarizeAbundance.py：按类型折叠大表，如基因按KEGG的KO合并
    - tax_circlize.R：物种组成圈图
    - tax_maptree.R：物种组成气泡图
    - tax_stackplot.R：物种组成堆叠柱状图