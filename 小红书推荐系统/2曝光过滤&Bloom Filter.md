![[Pasted image 20251107110027.png]]
![[Pasted image 20251107110149.png]]
![[Pasted image 20251107110404.png]]
用m维向量 表示所有物品（用户的物品曝光向量），1个Bit为一个物品/几个Bit为一个物品；每个用户有个物品曝光向量；
![[Pasted image 20251107110644.png]]
![[Pasted image 20251107110713.png]]
k的值为物品映射的bit数目/哈希函数的个数；
![[Pasted image 20251107110905.png]]
![[Pasted image 20251107111558.png]]
已曝光的物品，用实时流处理（快速），经过bloom filter写入用户曝光物品向量，再用作到召回当中：对于考虑召回的物品，hash函数计算其bit表示，在用户曝光向量中看此物品是否曝光过；
![[Pasted image 20251107111956.png]]
如何移除大于1个月？按时间滑动窗口；![[Pasted image 20260114131411.png]]
若将某bit置0，则有可能将很多物品都删除；
