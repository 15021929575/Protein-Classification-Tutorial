

# �����ʷ���̳̣���cytokineΪ����
version 0.1

##һ�����̸������£�

![](/img/001.jpg)

##��������FASTA���ݣ���������ʶ��������ԣ�PFAM��

ʶ�𵰰��ʼ������Եķ����кܶ࣬�ͳ�ķ�������ĳ�����������ݿ⣨���磺Uniport�����ҵ����ֵ����ʣ���������ԣ�PFAM����һĿ��Ȼ�� ���μ���http://datamining.xmu.edu.cn/~wangzhen/cytokine/���� ��Ȼ�����ַ���ֻ�ʺ�С������ѯ������д��СJava����ʵ����Ϣץȡ���ٸ����ӣ��������һ���������ǲ���cytokine (ϸ������)���������£����Ա����ӣ��� 

####1. �ҳ�Ŀǰ��֪��cytokine����googleһ����û����֪��database�����û�п���ȥUniprot���ݿ⣨[����](http://www.uniprot.org/ "Title")��������cytokine��Ȼ����FASTA��ʽdownload���ؽ���� 

![](/img/002.jpg)

####2. ������ϣ���ѹ���ļ��󣬽�FASTA���ݸ�ʽ���ļ���Notepad++�򿪣����Կ������¸�ʽ�����У��ú�ɫ����Ȧ�����Ĳ����ǵ����ʵ�UniportID��
 
![](/img/003.jpg)

####3. ����UniportID��ѯ�����ʵ�PFAM���塣

���ȣ�������վhttp://www.programmableweb.com/

Ȼ�󣬲���PFAM��Ӧ��API��

![](/img/004.jpg)

![](/img/005.jpg)

####4. �����API��վ�����ǿ��Կ����������ķ���XML��ʽ��API���ӷ��صļ�XML�������ȡPFAM���ٶȸܸܵģ�
```
api��http://pfam.xfam.org/protein/{PFAM}?output=xml��
```

 ![](/img/006.jpg)


####5. �����ϲ�����ʵ��

����Դ���벿����Github��https://github.com/ShixiangWan/Get-PFAM-of-cytokine


##����ȥ�ظ�����ȡ����

������Ҫ֪������ʱ����cytokine�ĵ������о���������������Ƿ�����ÿ�����ж�������һ��PFAM���壬�������л�����ͬһ�����塣

���ҳ�cytokine��������������PFAM�������Ҫɾ���ظ���PFAM�õ����ظ����������壨txt��ʽ������ȫ��������ɾ��������Ŷ�Ӧ�ļ�����ô�ҳ����з����ļ��壬����ÿ������������һ����ĵ���������Ϊ��ȡ���ķ�����

����Դ���벿����Github��https://github.com/ShixiangWan/Get-PFAM-of-cytokine

##�ġ�CH-HIT����ȥ����

���ú��ʵľ�����ֵ���ֱ��ǰ��õ���������fasta�����ļ����о��࣬ȥ�����࣬�������и��������������е�������ȡ����

CD-HIT��ַ��http://weizhong-lab.ucsd.edu/public/

ʹ�÷����ǳ��򵥣����ú������ļ�����������ֵ������70%��������ļ������ɡ�

##�塢��ȡ��������

ǰ���ķ����Ѿ��õ���Ϊ�����fasta�����������ļ���weka�޷�������з����������Ҫ����ֱ���ȡ����������������csv��arff��weka�ܹ�������ļ���ʽת����
��ȡ���������ķ����ǳ��࣬����ڵ��������У���188ά��Pse-in-one��Pseb��K-skip��n-gram��protrweb�ȡ�

һ��ȫ����ܽ�����http://malab.cn/forum.php?mod=viewthread&tid=926&extra=page%3D1

* 188ά��ַ�����ܽ���
* Pse-in-one��ַ��http://bioinformatics.hitsz.edu.cn/Pse-in-One/
* Pseb��ַ�����ܽ���
* n-gram��ַ�����ܽ���
* protrweb��ַ��http://protrweb.scbdd.com/

##�����Ը�ά����������ά

N-Gram�����У����nȡֵΪ3�����ݵ����ʰ���������Ϊ20����ô���õ�20*20*20=8000ά�������������ڷ����Ԥ���ǧ�������������ʱ����Ȼ�����˸�ά���ѣ��������о����С���ά����Ҳ�кܶ࣬����mRMR��mRMD�ȵȡ�

* mRMR��ַ��http://penglab.janelia.org/proj/mRMR/
* mRMD��ַ��http://datamining.xmu.edu.cn/~zjcdm/data/MRMD_CH.html

##�ߡ�weka������֤������Ԥ��

1. ���ȣ�Ҫ��ǰ���õ����������������ļ����и�ʽ���������Ϊarff��libsvm��csv�ļ����ɣ�arff�ļ���weka֧�ֵı�׼��ʽ��libsvm�Ǻܶ���ȡ���������㷨�õ�������ļ���ʽ��csv�洢����Ŀռ���С����򵥣�ǽ���Ƽ�����

2. �������������ļ���������ǩ������1�����������ķ����ļ��ӷ�����ǩ������0�������ϲ���һ�����ļ�����������ļ�����weka������������LibSVM��LibD3C��LibLinear��Bagging��Randomforest��IBK��J48,�ȵȣ�����5�ۻ�10�۽�����֤�����������õ�����׼ȷ���Լ���������������ָ���������ָ�ꡣ

3. ע�⣺LibD3C�������ھ�ʵ���ҿ�������ַ���£�http://datamining.xmu.edu.cn/~gjs/project/LibD3C.html

 ![](/img/007.jpg)

###�ο���վ��
[1] http://datamining.xmu.edu.cn/~wangzhen/cytokine/

[2] http://malab.cn/forum.php?mod=viewthread&tid=926&extra=page%3D1

