
算子( 输入图形变量: 输出图形变量: 输入数据变量: 输出数据变量)



- dev_open_window( : : Row, Column, Width, Height, Background: WindowHandle)      在指定位置打开指定宽高和颜色的窗口并返回窗口句柄
- dev_open_window_fit_image( Image: : Row, Column, WidthLimit, HeightLimit: WindowHandle)      在指定位置打开指定图片并限制宽高的窗口并返回窗口句柄
- dev_close_window( : : : )         关闭当前活跃的窗口
- dev_get_window( : : : WindowHandle)       获取当前活跃窗口的句柄
- ( : : : )
- ( : : : )
- ( : : : )
- dev_set_colored( : : ColorNumber: )              设置输出区域颜色个数
- dev_set_color( : : ColorName: )           设置单个输出的颜色，视窗上分割某个区域时使用的颜色
- ( : : : )
- dev_set_line_width( : : : )
- dev_set_draw( : : DrawMode: )             设置区域填充的模式，fill为填充，margin为只取边缘
- ( : : : )
- ( : : : )
- ( : : : )
- dev_desplay( Object: : : )        将一个图形或区域展示在当前活跃的窗口
- ( : : : )
- ( : : : )
- dev_set_lut( : : LutName : )          设置颜色速查表(look up table),可用于共生矩阵的彩色显示
- ( : : : )
- ( : : : )



- read_image( : Image: FileName: )                              读取文件




- get_image_size( Image : : : Width, Height)                获取图片的宽高
- get_image_time(Image : : : MSecond, Second, Minute, Hour, Day, YDay, Month, Year)   获取图片的创建时间
- get_image_type(Image : : : Type)                          获取图片的类型
- get_image_pointer1(Image : : : Pointer, Type, Width, Height)           获取单通道图片的c指针
- get_image_pointer3(ImageRGB : : : PointerRed, PointerGreen, PointerBlue, Type, Width, Height)   获取三通道图片的c指针
- decompose3(MultiChannelImage : Image1, Image2, Image3 : : )       将三通道图片分解为三个颜色的灰度图
- compose3(Image1, Image2, Image3 : MultiChannelImage : : )    将三个颜色的灰度图合成三通道图片
- rgb1_to_gray( RGBImage: GrayImage: : )                        转化为灰度图，灰度由rgb各乘一定比例来算
- rgb3_to_gray( RedImage, GreenImage, BlueImage: GrayImage: : )   转化为灰度图，输入参数为单色图片，注意顺序



- ( : : : )
- ( : : : )
- ( : : : )

- threshold( Image: Region: MinGray, MaxGray: )              阈值分割，生成中间灰度值的区域

- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )


- boundary(Region : RegionBorder : BoundaryType : )             提取区域的边界
- fill_up(Region : RegionFillUp : : )                           填充所有内部空洞
- fill_up_shape(Region : RegionFillUp : Feature, Min, Max : )   根据条件填充内部空洞


- connection( Region : ConnectedRegions : : )            将整个区域分成的不连通的区域数组
- union1(Region : RegionUnion : : )             将不连通的区域数组合成整个区域
- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )
- concat_obj(Objects1, Objects2 : ObjectsConcat : : )         将两个对象(可以是区域)合并成一个新的数组对象
- tile_images(Images : TiledImage : NumColumns, TileOrder : )       将图像数组拼接成一个大图像



- select_shape(Regions : SelectedRegions : Features, Operation, Min, Max : )       通过条件选择区域
- select_gray( : : : )                  根据灰度值筛选区域
- ( : : : )
- ( : : : )
- ( : : : )



- sobel_dir( Image: EdgeAmplitude, EdgeDirection: FilterType, Size: )  边缘检测???
- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )
- edges_image(Image : ImaAmp, ImaDir : Filter, Alpha, NMS, Low, High : )    边缘检测???



- hough_lines( : : : )
- ( : : : )
- ( : : : )
- ( : : : )
- hough_circles( : : : )
- ( : : : )



- area_center( Regions: : : Area, Row, Column)            输出区域的面积和中心点的横纵坐标数组, 注意: `|Area|`可获取区域个数
- area_holes( : : : )                       输出孔洞的大小
- area_center_gray( Regions, Image: : : Area, Row, Column)     输出区域的灰度体积和体积中心点的横纵坐标数组
  - 灰度体积: 灰度的面积x灰度，灰度中心点: 灰度体积的重心横纵坐标
- ( : : : )
- get_string_extents( : : WindowHandle, Values : Ascent, Descent, Width, Height)    似乎是获取显示字符的空间大小
- ( : : : )
- ( : : : )
- disp_message( : : : )             似乎是显示文字
- ( : : : )
- ( : : : )
- ( : : : )





- vector_to_rigid( : : Px, Py, Qx, Qy : HomMat2D)       仿射变换矩阵???
- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )


- inner_circle( : : : )             计算内接圆
- smallest_rectangle1( : : : )      计算最小外接矩形( 不可旋转)
- smallest_rectangle2( : : : )      计算最小外接矩形( 可旋转)
- ( : : : )
- ( : : : )

- gray_features( Regions, Image: : Features: Value)          计算灰度特征值
- intensity( Regions, Image: : : Mean, Deviation)             计算平均值和偏差
- min_max_gray( Regions, Image: : Percent: Min, Max, Range)    计算区域的最大最小灰度值
- ( : : : )
- ( : : : )


- gen_rectangle1( : Rectangle : Row1, Column1, Row2, Column2 : )        生成长方形
- ( : : : )
- ( : : : )
- gen_ellipse( : Ellipse : Row, Column, Phi, Radius1, Radius2 : )       生成椭圆，Phi为倾斜角度
- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )
- gen_cross_contour_xld( : Cross : Row, Col, Size, Angle : )        生成十字标
- ( : : : )
- ( : : : )
- ( : : : )
- skeleton(Region : Skeleton : : )


- reduce_domain( : : : )                似乎是从图上截取对应区域的部分生成新的图像
- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )


- regiongrowing( : : : )
- ( : : : )
- ( : : : )
- ( : : : )
- ( : : : )


- gen_cooc_matrix(Regions, Image : Matrix : LdGray, Direction : )              创建共生矩阵
- cooc_feature_matrix(CoocMatrix : : : Energy, Correlation, Homogeneity, Contrast)      生成共生矩阵的4个灰度特征值
- cooc_feature_image(Regions, Image : : LdGray, Direction : Energy, Correlation, Homogeneity, Contrast)     直接生成共生矩阵的四个灰度特征值，相当于前两个算子合并
- ( : : : )
- ( : : : )
- ( : : : ) 

- gen_disc_se( : SE : Type, Width, Height, Smax : )


# 形状的腐蚀，膨胀，开闭运算，击中运算
>开运算：先腐蚀后膨胀，闭运算：先膨胀后腐蚀，开运算处理外部噪音和毛刺，闭运算处理内部空洞
- erosion_circle(Region : RegionErosion : Radius : )                  以给定半径的圆进行腐蚀
- erosion_rectangle1(Region : RegionErosion : Width, Height : )         以给定长宽的长方形进行腐蚀
- erosion1(Region, StructElement : RegionErosion : Iterations : )       以给定结构进行腐蚀，Iterations代表重复腐蚀的次数
- erosion2(Region, StructElement : RegionErosion : Row, Column, Iterations : )  以给定形结构进行腐蚀，并将结果移到参考点位置

- dilation_circle(Region : RegionDilation : Radius : )                  以给定半径的圆进行膨胀
- dilation_rectangle1(Region : RegionDilation : Width, Height : )         以给定长宽的长方形进行膨胀
- dilation1(Region, StructElement : RegionDilation : Iterations : )         以给定结构进行膨胀，Iterations代表重复膨胀的次数
- dilation2(Region, StructElement : RegionDilation : Row, Column, Iterations : )  以给定形结构进行膨胀，并将结果移到参考点位置

- opening_circle(Region : RegionOpening : Radius : )                以给定半径的圆进行开运算
- opening_rectangle1(Region : RegionOpening : Width, Height : )           以给定长宽的长方形进行开运算
- opening(Region, StructElement : RegionOpening : : )               以给定结构进行开运算

- closing_circle(Region : RegionClosing : Radius : )                以给定半径的圆进行闭运算
- closing_rectangle1(Region : RegionClosing : Width, Height : )             以给定长宽的长方形进行闭运算
- closing(Region, StructElement : RegionClosing : : )               以给定结构进行闭运算

- hit_or_miss(Region, StructElement1, StructElement2 : RegionHitMiss : Row, Column : )  击中与击不中运算，StructElement1和StructElement2进行腐蚀的交集，StructElement1和StructElement2为互补的区域即可匹配相同的图形

# 灰度的腐蚀，膨胀，开闭运算，顶帽、底帽运算
>灰度开运算处理消除亮区域,灰度闭运算处理消除暗区域
>顶帽运算：原图-开运算，底帽运算：闭运算-原图，白顶帽，黑底帽
- gray_erosion(Image, SE : ImageErosion : : )
- gray_erosion_rect(Image : ImageMin : MaskHeight, MaskWidth : )
- gray_erosion_shape(Image : ImageMin : MaskHeight, MaskWidth, MaskShape : )

- gray_dilation(Image, SE : ImageDilation : : )
- gray_dilation_rect(Image : ImageMax : MaskHeight, MaskWidth : )
- gray_dilation_shape(Image : ImageMax : MaskHeight, MaskWidth, MaskShape : )

- gray_opening(Image, SE : ImageOpening : : )
- gray_opening_rect(Image : ImageOpening : MaskHeight, MaskWidth : )
- gray_opening_shape(Image : ImageOpening : MaskHeight, MaskWidth, MaskShape : )

- gray_closing(Image, SE : ImageClosing : : )
- gray_closing_rect(Image : ImageClosing : MaskHeight, MaskWidth : )
- gray_closing_shape(Image : ImageClosing : MaskHeight, MaskWidth, MaskShape : )







# 模板匹配，ncc模板，形状特征模板
- create_ncc_model(Template : : NumLevels, AngleStart, AngleExtent, AngleStep, Metric : ModelID)    创建ncc匹配模板，NumLevels为金字塔层级，AngleStart, AngleExtent, AngleStep为旋转的开始弧度，弧度范围，单步弧度，Metric为是否匹配的前后景相反的图形
- find_ncc_model(Image : : ModelID, AngleStart, AngleExtent, MinScore, NumMatches, MaxOverlap, SubPixel, NumLevels : Row, Column, Angle, Score)         根据ncc模板查找并返回匹配的位置，MinScore为最小匹配度，NumMatches为匹配数量(0表示所有匹配都保留)，MaxOverlap表示不同匹配的最大重叠区域(超出则表示为同一匹配)
- clear_ncc_model( : : ModelID : )
- clear_all_ncc_models( : : : )

- ( : : : )
- ( : : : ) 
- ( : : : )
- ( : : : )




- ( : : : ) 
- create_shape_model(Template : : NumLevels, AngleStart, AngleExtent, AngleStep, Optimization, Metric, Contrast, MinContrast : ModelID)
- create_scaled_shape_model(Template : : NumLevels, AngleStart, AngleExtent, AngleStep, ScaleMin, ScaleMax, ScaleStep, Optimization, Metric, Contrast, MinContrast : ModelID)
- create_aniso_shape_model(Template : : NumLevels, AngleStart, AngleExtent, AngleStep, ScaleRMin, ScaleRMax, ScaleRStep, ScaleCMin, ScaleCMax, ScaleCStep, Optimization, Metric, Contrast, MinContrast : ModelID)
- ( : : : )
- ( : : : )
- ( : : : ) 



- find_shape_model(Image : : ModelID, AngleStart, AngleExtent, MinScore, NumMatches, MaxOverlap, SubPixel, NumLevels, Greediness : Row, Column, Angle, Score)
- get_shape_model_contours( : ModelContours : ModelID, Level : )


- inspect_shape_model(Image : ModelImages, ModelRegions : NumLevels, Contrast : )















- ( : : : )
- ( : : : )
- ( : : : ) 
- ( : : : )
- ( : : : )
- ( : : : ) 
- ( : : : )
- ( : : : )
- ( : : : ) 
- ( : : : )
- ( : : : )
- ( : : : ) 

- ( : : : )
- ( : : : )
- ( : : : ) 
- ( : : : )
- ( : : : )
- ( : : : ) 
- ( : : : )
- ( : : : )
- ( : : : ) 
- ( : : : )
- ( : : : )
- ( : : : ) 



# 设备

- open_framegrabber( : : Name, HorizontalResolution, VerticalResolution, ImageWidth, ImageHeight, StartRow, StartColumn, Field, BitsPerChannel, ColorSpace, Generic, ExternalTrigger, CameraType, Device, Port, LineIn : AcqHandle)             打开设备
- close_framegrabber( : : AcqHandle : )         关闭设备

- set_framegrabber_param( : : AcqHandle, Param, Value : )       设置设备参数，如延时
- get_framegrabber_param( : : AcqHandle, Param : Value)       获取设备参数

- grab_image( : Image : AcqHandle : )         从设备中获取图片

- grab_image_start( : : AcqHandle, MaxDelay : )
- grab_image_async( : Image : AcqHandle, MaxDelay : )




# 3D


- read_object_model_3d( : : FileName, Scale, GenParamName, GenParamValue : ObjectModel3D, Status)   读取点云

- surface_normals_object_model_3d( : : ObjectModel3D, Method, GenParamName, GenParamValue : ObjectModel3DNormals)   在点云句柄上添加的法向量???

- visualize_object_model_3d( : : WindowHandle, ObjectModel3D, CamParam, PoseIn, GenParamName, GenParamValue, Title, Label, Information : PoseOut)   显示点云图(函数)
  - GenParamName、GenParamValue两个数组一一对应，为控制显示的参数和值

- triangulate_object_model_3d( : : ObjectModel3D, Method, GenParamName, GenParamValue : TriangulatedObjectModel3D, Information)    将点云图进行三角曲面重建

- write_object_model_3d( : : ObjectModel3D, FileType, FileName, GenParamName, GenParamValue : )     保存3d图

- get_object_model_3d_params( : : ObjectModel3D, GenParamName : GenParamValue)      获取3d点云的参数，如点云点数、坐标

- select_object_model_3d( : : ObjectModel3D, Feature, Operation, MinValue, MaxValue : ObjectModel3DSelected)        筛选点云

- moments_object_model_3d( : : ObjectModel3D, MomentsToCalculate : Moments)
  - MomentsToCalculate可选值: 
    1. mean_points：均值，结果为点云在x,y,z轴的均值
    2. central_moment_2_points： 二阶矩（方差），结果为点云在x、y、z方差和x-y、x-z 和 y-z 轴的协方差
    3. principal_axes：结果为当前模型的刚性转换位姿(刚性转换到中心需要将此值反转)

- pose_invert( : : Pose : PoseInvert)   反转位姿

- rigid_trans_object_model_3d( : : ObjectModel3D, Pose : ObjectModel3DRigidTrans)   对模型刚性转换


- pose_to_hom_mat3d( : : Pose : HomMat3D)     将位姿信息转化为3D仿射变换的矩阵

- affine_trans_object_model_3d( : : ObjectModel3D, HomMat3D : ObjectModel3DAffineTrans)     对模型进行3D仿射变换

- gen_plane_object_model_3d( : : Pose, XExtent, YExtent : ObjectModel3D)    创建平面
  - XExtent, YExtent    [,,,]四个值分别代表平面四个顶角的x和y坐标(位姿调整前的)
- intersect_plane_object_model_3d( : : ObjectModel3D, Plane : ObjectModel3DIntersection)    获取和平面的交线

- create_surface_model( : : ObjectModel3D, RelSamplingDistance, GenParamName, GenParamValue : SurfaceModelID)       创建表面模型

- find_surface_model( : : SurfaceModelID, ObjectModel3D, RelSamplingDistance, KeyPointFraction, MinScore, ReturnResultHandle, GenParamName, GenParamValue : Pose, Score, SurfaceMatchingResultID)   根据表面模型进行表面匹配
  - 注意多个匹配项时位姿信息在同一个数组中

- get_surface_matching_result( : : SurfaceMatchingResultID, ResultName, ResultIndex : ResultValue)      获取表面匹配的结果

- ( : : : )

- ( : : : )

- ( : : : )

- ( : : : )

- ( : : : )

- ( : : : )

- ( : : : )

- ( : : : )

- ( : : : )

- ( : : : )

- ( : : : )

- ( : : : )

- ( : : : )

- ( : : : )

- ( : : : ) 
- ( : : : )
- ( : : : )
- ( : : : ) 
- ( : : : )
- ( : : : )
- ( : : : ) 
- ( : : : )
- ( : : : )
- ( : : : ) 






运算相关：

- `|数组|`会获取数组的长度
  - 循环语句: `for xxx: =0 to n by 1    ...    endfor`

- `数组[x:y]`获取数组中从x到y的一段

































