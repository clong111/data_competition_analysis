这次比赛诈骗数据特征非常明显，但在线下取得高分的情况下，线上表现不佳，重点在于分析训练集和测试集的差异所在。
探索数据有以下几个值得注意的地方：
1.数据集最重要的特征是mff,而训练集和测试集差距最大的特征也是mff.
2.mff=24是诈骗明显的特征。
3.训练集的数据是1,2月，测试集的特征是3,4月。其中1月和3月分布接近，2月和4月分布接近，强烈怀疑人工数据！
4.其中2月和4月存在细微但关键的差距，2月mff=16和mff=24的比例，在4月的表现刚好相反。初步怀疑将两个数据误标。
5.继续探索，发现如果用第一个月的gam和第二个月mff相加，能够消除两个数据集分布差异。
结论：两个数据集差异的原因在于第二个月mff特征的细微差异，但并不是误标数据，而是需要将两个特征结合，才能还原数据集在第二个的真实分布。 