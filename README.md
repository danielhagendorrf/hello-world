# load and show an image
int captureImage()
{
	IplImage *img = cvLoadImage("C:\\masa.jpg");
	Mat image(img);
	if (image.empty()) 
	{
		cout << "Error : Image cannot be loaded..!!" << endl;
		return -1;
	}
	namedWindow("MyWindow", CV_WINDOW_AUTOSIZE);
	imshow("MyWindow", image); 
	destroyWindow("MyWindow"); 
	return 0;
}
