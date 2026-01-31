![[Pasted image 20251106220814.png]]
outline：
![[Pasted image 20251106220849.png]]
==索引：==
![[Pasted image 20251106221132.png]]
![[Pasted image 20251106221219.png]]
多对多关系；
==预估模型：预估用户对路径的兴趣==
![[Pasted image 20251106221631.png]]
![[Pasted image 20251106222610.png]]
pi向量的k个元素 为神经网络对第i层的 k个节点的评分；每次选出分数最高的节点；
==线上召回==
![[Pasted image 20251106225001.png]]
![[Pasted image 20251107094521.png]]
beam size为召回的路径数目，其越大，计算量越大；
![[Pasted image 20251107094647.png]]![[Pasted image 20251107094829.png]]
beamSearch（束搜索）总结：通过 贪心算法和兴趣公式 召回路径：每层只保留beam size个节点；选下一层时计算beam size* beam size个节点，但只保留beam  size个；
线上召回总结：
![[Pasted image 20251107095225.png]]
==训练==
![[Pasted image 20251107095452.png]]
学习兴趣-路径表示；学习路径-物品对应关系；
只需正样本，用户点击过的物品即为正样本；
![[Pasted image 20251107095857.png]]
目标：让j条路径上的 最后一层的可能性之和变大；
![[Pasted image 20251107100700.png]]
![[Pasted image 20251107100936.png]]
![[Pasted image 20251107101147.png]]
训练总结：
![[Pasted image 20251107103430.png]]
初始时，物品-路径任意初始化；根据用户点击的物品，使得该路径上的p（用户兴趣分数）变大；
再根据p和物品点击，更新物品-路径对应关系；不断更更新；
deep retrieval总结：
![[Pasted image 20251107103800.png]]
离线训练：
![[Pasted image 20251107104049.png]]

