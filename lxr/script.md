图片边界问题解决办法
===============
问题描述
-------
在svg图片边界地方弹出的菜单不能完整显示，部分菜单显示在图片范围之外。
问题分析
-------
svg代码中，生成菜单的脚本代码在处理边界问题时有问题，在节点和边的弹出菜单分别修改边界值。
解决方法
-------
script文件中  
####144～147行：
  if(posY>(0-64))  
  {  
    posY=posY-64  
  }  
######改为:
  if(posY>(0-128))  
  {  
    posY=0-128  
  }  
####229～232行：
  if(posY>(0-64))  
  {  
    posY=posY-64  
  }  
######改为: 
  if(posY>(0-96))  
  {  
    posY=0-96  
  }  
