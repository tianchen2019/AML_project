# 健康数据集的整理
## 所有细胞类型的数据集
### 使用原始的NBT文章数据跑archR得到的proj，以及peak matrix文件，合并fragment文件
代码: 
#### 加上了GMP的代码文件
1. 使用文章初始的fragment文件，选出NBT文章中有的细胞建立archR proj: 
C:\Users\18821\Desktop\AML数据分析\补测之后的代码\step0_healthy\ArchR创建healthy的peakmatrix\healthy_NBT_mulitiGMPcell.r
2. 用peak matrix建立所有细胞的proj，且proj带有fragment文件：
C:\Users\18821\Desktop\AML数据分析\补测之后的代码\step0_healthy\ArchR创建healthy的peakmatrix\healthyfragment文件输出及重新callpeak_output_fragmentfile_peak_NBT_mulitiGMPcell.r代码的前半段
4. 去除批次: 加了GMP的结果:
C:\Users\18821\Desktop\AML数据分析\补测之后的代码\step0_healthy\movebatch
最后选的批次有变化:
5. 去除批次后的proj建立的archR文件: 坐标换成了去除了批次的坐标：
C:\Users\18821\Desktop\AML数据分析\补测之后的代码\step0_healthy\ArchR创建healthy的peakmatrix\addmuliti_neu_archrproj.r

文件：
#### 1. 未加上GMP的文件:
healthy未去除批次的数据:
/home/tianchen/AML_project/step0_healthy_analysis/healthy_human/no_moverbatch/
 healthy去除了批次的数据: 
 ~/AML_project/step0_healthy_analysis/healthy_human/move_batch/
 
 
####  2. 加上了GMP的数据:
healthy未去除批次的数据: 
~/AML_project/step0_healthy_analysis/healthy_human/no_moverbatch/new_healthy
healthy去除批次的数据:
~/AML_project/step0_healthy_analysis/healthy_human/move_batch/new_healthy/rerun/integrated_filtercell.rdata
去除批次后的proj建立的archR文件: 坐标换成了去除了批次的坐标
~/AML_project/step0_healthy_analysis/healthy_human/no_moverbatch/new_healthy/ArchR_file/1_proj

## 髓系细胞的文件
1. 髓系细胞首先从总细胞中选出来，然后分细胞类型重新call peak，得到一个mye文件:
代码:C:\Users\18821\Desktop\AML数据分析\补测之后的代码\step0_healthy\建立mye的细胞聚类以及重新callpeak，去除批次等\mye_peak_proj.r
文件:
~/AML_project/step0_healthy_analysis/healthy_human/trajectory/mye.peaks.rdata
2. 髓系细胞单独去除批次:
容器集群
~/AML_project/step0_healthy_analysis/healthy_human/trajectory/mye_movebatch.r
![5d6d6dadc495cd86df036395d8c3d57](https://user-images.githubusercontent.com/46451175/171596058-5d1d84de-7065-49d4-8bdf-c8e4374cb6bb.png)

文件: 
~/AML_project/step0_healthy_analysis/healthy_human/trajectory/mye_integratedfinal.rdata
3. 髓系去除批次后的细胞，建立archR proj，且添加降维信息按照去除批次的坐标，同时加上了trajectory坐标（monocyte太多，选取1000 cells）：
代码: /home/tianchen/AML_project/step0_healthy_analysis/healthy_human/no_moverbatch/new_healthy/ArchR_file/get_proj_mye.r
文件: ~/AML_project/step0_healthy_analysis/healthy_human/no_moverbatch/new_healthy/ArchR_file/proj_mye1
4. 修改archR，peak用自己call的，并且得到motif矩阵:
代码: ~/hsc_differentiation/human_hsc/2_paper_merge/motif_mye.r
文件: ~/hsc_differentiation/human_hsc/2_paper_merge/motif_myeproj

4. 添加每个细胞map的情况代码:
C:\Users\18821\Desktop\AML数据分析\补测之后的代码\step0_healthy\建立mye的细胞聚类以及重新callpeak，去除批次等\mye_添加trajory值_LJJ.r
