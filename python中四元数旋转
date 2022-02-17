
# 利用pyquaternion进行3d世界坐标和局部坐标的转换

世界坐标中的一个点a（1，2，3），相机坐标为b（1，0，0），相机四元数为c(0.71,0,0,0.71)，相当于绕着z轴旋转90°，

# 则世界坐标转化为局部坐标为

  quaternion(c).rotate_matrix @ a - b
  
  结果为d（-3，1，3）
  
# 将局部坐标转化为世界坐标
  
  quaternion(c).rotate_matrix.T @(d + b)
