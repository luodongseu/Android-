#Bug汇总
##错误1：
###ListView加了HeaderView后在OnItemClick中的position不正确
####原因：用于设置数据的adapter和在ListView加载后的adapter有差别
####解决方案：将position替换成parent.getAdapter().getItemId(position)即可获得正确的位置
