![[Pasted image 20251107210206.png]]
1首次发表SENet，用于CV领域；2首次应用到推荐系统；
SENet网络结构：
![[Pasted image 20251107211337.png]]
m个离散特征映射为k维embedding；
r>1，为压缩比例；
ReLU激活函数：
![[Pasted image 20251107211358.png]]
![[Pasted image 20251107211604.png]]
![[Pasted image 20251107211947.png]]
SENet：根据全局，对离散特征做加权，重要的特征权重高，不重要的特征权重低；
Field特征交叉：
![[Pasted image 20251107212239.png]]
哈达玛乘积得到的m^2个向量规模太大，一般不会全部计算；
![[Pasted image 20251107212429.png]]
![[Pasted image 20251107212554.png]]
xi和xj之间交换位置是一个参数矩阵；
![[Pasted image 20251107212717.png]]
![[Pasted image 20251107212742.png]]
[[3 FiBiNet]]
