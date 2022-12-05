# UAL-CCI-Codingone-22018741-ZiqingXu
This is my final project for Element 1: Project

Background 

This project is an interactive computational design work based on Java script and html. It is inspired from classical oil painting and artworks such as Campbell's Soup Cans created by Andy Warhol who is one of the leading artists of visual pop art movement. 

Technology part

On the screen, there are mainly three parts. First, two concise geometric cone looks like hourglass which is simply consist of random points. They represent the passing of time. To draw these two images on screen, knowledge about drawing 3D on canvas were used. The 3D projection is done by scale: scale= fov/fov+z3d.The order is First scale, rotate, then translate.The process is similar to and based on the steps of drawing a sphere on canvas. First step is draw circles. The difference is all vertices should be connected into single vertex which has same x,y coordinates and different z coordinate.

Second part is one piece of classical oil painting with complicated skills which refers to traditional arts. To show this picture on screen need basic canvas drawing skills and here is used
var imageData = context2.getImageData(0, 0, imageWidth, imageHeight);
var imageData2 = context.getImageData(0, 0, imageWidth, imageHeight);

to get image data from picture that author uploaded.
To get pictures, this code were used:

context.putImageData(imageData2,0,0);

The third part is one copy of this painting which is produced by programming and convolution. It will change its color, brightness, contrast with mouse movement and simulate the rusty corruption and decay process in an art way. In the tutorial of this term, the way of producing convolution effect is using a 'kernel' of -1 0 1 in only one dimension and it can be used in either x or y dimension. However, In this program, according to the principle and examples from Utkarsh Sinha and Victor Powell, author tried to use 3x3 kernels to produce convolution. For each 3x3 pixels from the original pictures, each of the single pixel will multiply the kernel of corresponding position and then get the total sum of nine numbers. After this process, new pixel of new canvas is produced. This is why the processed picture looks more vague. This is the basic logic of how this author learn to make convolution and the real process is little more complex. First, to store the pixel information and manage them, the R,G,B and alpha numbers needed. Here author used this formula: 

position=(j+i*imageData.width)*4;
imageData.data[position] = c%255;
imageData.data[position+1] = c%255;
imageData.data[position+2] = c%255
imageData.data[position+3] = 255;

Author used this formula to get pixels of 3x3 blocks and get new Red value:
imageData2.data[((imageWidth * i) + j) * 4] = 
1*(data[(collm1 + j-1) * 4]) + (-1*(data[(collm1 + j) * 4]))+(0*(data[(collm1 + j+1) * 4]))+(-1*data[((i*imageWidth)+(j-1))*4])+(-1)*data[((imageWidth * i) + j+1) * 4])+(2*data[((imageWidth * i) + j) * 4]) + (0*(data[(collp1 + j-1) * 4]))+(-1*(data[(collp1 + j) * 4]))+ 0*(data[(collp1 + j+1) * 4])


// This is the row above
            var collm1=(i-1)*imageWidth;
// This is the row below
            var collp1=(i+1)*imageWidth;


To get new Green, Blue value, the only thing need to do is plus 1 and 2 after “4”. This formula actually used ‘kernel’ in both x and y coordinates.
The number before ‘data’ can be changed whatever viewer like, and this change will lead to different brightness.
This project also used Mousemod which is 
‘mouseMod = mouseX - imageWidth/2’  
and Mousemod2 which is
 ‘mouseMod2 = mouseY + imageHeight/2;’ 
to change contrast.

Summary

This project used mainly two things: 2D picture processing and 3D object drawing. The idea of this design work is trying to express the worries about the traditional art are in decline with the time passing (infinite rotating hourglass), and even the newest thing in today will be out of fashion one day because the development of technology never ends, meanwhile, it shows good expectation that even though everything has a gradual decline process, at the same time new things will emerge. 

Reference

https://mimicproject.com/code/7d7536ae-5b21-b5ee-262f-198400c09c60
https://aishack.in/tutorials/image-convolution-examples/ 
https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/filter
https://setosa.io/ev/image-kernels/ 
https://github.com/ual-cci/MSc-Coding-1/blob/master/session4.md 
https://github.com/ual-cci/MSc-Coding-1/blob/master/session5.md 

