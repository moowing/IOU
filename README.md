# IOU
Intersection over Union是一种测量在特定数据集中检测相应物体准确度的一个标准。
我们可以在很多物体检测挑战中，例如PASCAL VOC challenge中看多很多使用该标准的做法。

通常我们在 HOG + Linear SVM object detectors 和 Convolutional Neural Network detectors (R-CNN, Faster R-CNN, YOLO, etc.)中使用该方法检测其性能。注意，这个测量方法和你在任务中使用的物体检测算法没有关系。

IoU是一个简单的测量标准，只要是在输出中得出一个预测范围(bounding boxex)的任务都可以用IoU来进行测量。为了可以使IoU用于测量任意大小形状的物体检测，我们需要： 
1、 ground-truth bounding boxes（人为在训练集图像中标出要检测物体的大概范围）； 
2、我们的算法得出的结果范围。

也就是说，这个标准用于测量真实和预测之间的相关度，相关度越高，该值越高。

ground-truth和predicted的结果，绿色标线是人为标记的正确结果，红色标线是算法预测出来的结果，IoU要做的就是在这两个结果中测量算法的准确度

很简单，IoU相当于两个区域重叠的部分除以两个区域的集合部分得出的结果。 
一般来说，这个score ＞ 0.5 就可以被认为一个不错的结果了。


python程序

