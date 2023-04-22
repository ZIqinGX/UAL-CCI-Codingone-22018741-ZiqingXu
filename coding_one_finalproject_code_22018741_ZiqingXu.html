<html><html>

<head>
</head>

<style>

    /*
        This is to make sure
        the canvas is in the right position
        on all browsers lllll
    */

    canvas {
        position: absolute;
        top:0;
        left:0;
    }

</style>

<body>
<canvas id="canvas1"> </canvas>//give id to canvas
<canvas id="myCanvas"></canvas>
<canvas id="myCanvas2"></canvas>
<canvas id="canvas3"></canvas>
<script>

    var canvas1 = document.getElementById("canvas1");//get theeemnet by Id names canvas1    
var canvas2 = document.getElementById("canvas2");//get the elemnet by Id names canvas312
    var canvas3 = document.getElementById("canvas3");//get the elemnet by Id names canvas3
    var width = window.innerWidth;
    var height = window.innerHeight;
    create(canvas1,0,100)//the first canvas is positioned on the left side of screen,which has dim=100;
    create(canvas3,width*2/3,200)//second canvas is positioned on 2/3 width away form screen,which has dim 200;
    createCanvas2();

    function create(input_canvas,left,dim1) {
        var canvas = input_canvas;
        var fov = 800;//field of view
        var context = canvas.getContext("2d");

        canvas.style.left = left;
        canvas.style.border = "1px solid rgb(203,23,103)";
        canvas.setAttribute("width", width/3);
        canvas.setAttribute("height", height);
        canvas.addEventListener('mousemove',getMouse,false);
        var mouseX=0;
        var mouseY=0;
// This array is used to create an individual 3D vertex, represented by a 3D vector xyz
        var point = [];
      // This is where we stash all the vertices
        var points = [];
      //// This is temp storage for when we draw each 3D vertex
        var point3d = [];

        var angleX = 0;
        var angleY = 0;
        var HALF_WIDTH = width/3;
        var HALF_HEIGHT = height/2;

        var x3d = 0;
        var y3d = 0;
        var z3d = 0;

        var lastScale = 0;
        var lastx2d = 0;
        var lasty2d = 0;

        // The below code creates a sphere of points
        var dim = dim1; // This is the number of rings
        // Each ring has as many points as there are rings
        // This is the spacing for each ring
        var spacing = ((Math.PI*2 ) / dim);

        // This is the total number of points
        var numPoints = dim * dim;

        // This is how big the sphere is.
        var size = 100;

        // Now we build the sphere
        for (var i = 0; i < dim ; i++) {

// Calculate the depth spacing

            // Divide spacing in half to make sure cosine and sine keep positive 
          //in order to calculate the depth spacing
           // We only need the positive bit
            
            var z = size * Math.cos(spacing / 2 * i);

// Calculate the size of the current ring
            var s = size * Math.sin(spacing / 2 * i*2);

// For each ring..

            for (var j = 0; j < dim; j++ ) {

// ...create the next point in the circle at the current size s, at the current depth z

                point = [Math.cos(spacing * j) * s,Math.sin(spacing * j) * s,z];

// Add the point to the geometry.

                points.push(point);

            }
        }

        //
        console.log(points.length);

        function draw() {

            context.fillStyle = "rgb(203,23,103)";
            context.fillRect(0, 0, width, height);

            angleX=((mouseX/width)-0.5)/4;
            angleY=((mouseY/height)-0.5)/4;

// Here we run through each point and work out where it should be drawn

            for (var i = 0; i < numPoints; i++) {
                point3d = points[i];
                z3d = point3d[2];

// This is the speed of the z
// It moves the points forwards in space
// We don't need it for the pure rotate
                // z3d -= 1.0;

// Check that the points aren't disappearing into space and if so push them back
// This also stops them stretching
// When they get too close
                if (z3d < -fov) z3d += 0;

                point3d[2] = z3d;

                // Calculate the rotation

                rotateX(point3d,angleX);
                rotateY(point3d,angleY);

                // Get the point in position

                x3d = point3d[0];
                y3d = point3d[1];
                z3d = point3d[2];
// Convert the Z value to a scale factor
// This will give the appearance of depth
                var scale = (fov / (fov + z3d));

// Store the X value with the scaling
// FOV is taken into account
// (just pushing it over to the left a bit too)
                var x2d = (x3d * scale) + HALF_WIDTH / 2;

// Store the Y value with the scaling
// FOV is taken into account

                var y2d = (y3d * scale) + HALF_HEIGHT;

// Draw the point

// Set the size based on scaling
                context.lineWidth = scale;

                context.strokeStyle = "rgb(255,255,255)";
                context.beginPath();
                context.moveTo(x2d, y2d);
                context.lineTo(x2d + scale, y2d);
                context.stroke();
            }
            requestAnimationFrame(draw);
        }

        requestAnimationFrame(draw);

        function rotateX(point3d,angleX) {
            var	x = point3d[0];
            var	z = point3d[2];

            var	cosRY = Math.cos(angleX);
            var	sinRY = Math.sin(angleX);

            var	tempz = z;
            var	tempx = x;

            x= (tempx*cosRY)+(tempz*sinRY);
            z= (tempx*-sinRY)+(tempz*cosRY);

            point3d[0] = x;
            point3d[2] = z;

        }

        function rotateY(point3d,angleY) {
            var y = point3d[1];
            var	z = point3d[2];

            var cosRX = Math.cos(angleY);
            var sinRX = Math.sin(angleY);

            var	tempz = z;
            var	tempy = y;

            y= (tempy*cosRX)+(tempz*sinRX);
            z= (tempy*-sinRX)+(tempz*cosRX);

            point3d[1] = y;
            point3d[2] = z;

        }
    }

    //here's our function 'getMouse'.
    function getMouse (mousePosition) {
//for other browsers..
        if (mousePosition.layerX || mousePosition.layerX === 0) { // Firefox?
            mouseX = mousePosition.layerX;
            mouseY = mousePosition.layerY;
        } else if (mousePosition.offsetX || mousePosition.offsetX === 0) { // Opera?
            mouseX = mousePosition.offsetX;
            mouseY = mousePosition.offsetY;
        }
    }

    function createCanvas2() {
      var mouseX = 1;
        var mouseY = 1;
        var imageObj = new Image();
        imageObj.src = "Painting.jpg";

        var canvas = document.getElementById('myCanvas');
        var canvas2 = document.getElementById('myCanvas2');
        canvas.addEventListener('mousemove', getMouse, false);
        canvas.setAttribute("width",window.innerWidth/3);
         canvas.setAttribute("height",window.innerHeight/2);
      
         canvas2.setAttribute("width",window.innerWidth/3);//divide our screen into 3 parts 
                                           //and one gives canvas2
         canvas2.setAttribute("height",window.innerHeight/2);//divide the middle canvas into 2
        canvas.style.left=window.innerWidth/3;
        canvas2.style.left=window.innerWidth/3;
      canvas2.style.top=window.innerHeight/2;
      
        var context = canvas.getContext('2d');
        var context2 = canvas2.getContext('2d');
        var imageWidth = imageObj.width;
        var imageHeight = imageObj.height;

        context2.drawImage(imageObj, 0, 0);

        var imageData = context2.getImageData(0, 0, imageWidth, imageHeight);//get image data 
                                                      //from picture uploaded
        var data = imageData.data;
        var imageData2 = context.getImageData(0, 0, imageWidth, imageHeight);
        var imageData3 = context.getImageData(0, 0, imageWidth, imageHeight);
        //var imageData2 = imageData;
      
   
       var draw = function() {
       var mouseMod = mouseX - imageWidth/2;//change contrast
        var mouseMod2 = mouseY + imageHeight/2;//change contrast
        for(var i = 1; i < imageHeight-1; i++) {
            
            // This is the row above
            var collm1=(i-1)*imageWidth;
            // This is the row below
            var collp1=(i+1)*imageWidth;
            var position=(i*imageData.width+j)*4
                   // loop through each row
          for(var j = 1; j < imageWidth-1; j++) {
 if (data[((imageWidth * i) + j) * 4] < 2*mouseY-mouseX) {
 // convolution,get new Red value          
            imageData2.data[((imageWidth * i) + j) * 4] = 1*(data[(collm1 + j-1) * 4]) + (-1*(data[(collm1 + j) * 4]))+(0*(data[(collm1 + j+1) * 4]))+(-1*data[((i*imageWidth)+(j-1))*4])+(-1*data[((imageWidth * i) + j+1) * 4])+(2*data[((imageWidth * i) + j) * 4]) + (0*(data[(collp1 + j-1) * 4]))+(-1*(data[(collp1 + j) * 4]))+ 0*(data[(collp1 + j+1) * 4])+2*mouseMod2;
   //convolution,get new Green value
            imageData2.data[((imageWidth * i) + j) * 4+1] = 0*(data[(collm1 + j-1) * 4+1]) + (-2*(data[(collm1 + j) * 4+1]))+(0*(data[(collm1 + j+1) * 4+1]))+(-1*data[((i*imageWidth)+(j-1))*4+1])+(-1*data[((imageWidth * i) + j+1) *4+1])+(6*data[((imageWidth * i) + j) * 4+1]) + (0*(data[(collp1 + j-1) * 4]))+(-2*(data[(collp1 + j) * 4+1]))+ 0*(data[(collp1 + j+1) * 4+1])+0.1*mouseMod2;
   //convolution,get new Blue value
            imageData2.data[((imageWidth * i) + j) * 4+2] = -2*(data[(collm1 + j-1) * 4+2]) + (-1*(data[(collm1 + j) * 4+2]))+(0*(data[(collm1 + j+1) * 4+2]))+(0*data[((i*imageWidth)+(j-1))*4+2])+(-1*data[((imageWidth * i) + j+1) * 4+2])+(5*data[((imageWidth * i) + j) * 4+2]) + 2*(data[(collp1 + j-1) * 4+2])+(-1*(data[(collp1 + j) * 4+2]))+ 4*(data[(collp1 + j+1) * 4+2])+0.2*mouseMod;
   // Alpha
            imageData2.data[((imageWidth * i) + j) * 4+3] = mouseX/mouseY*255;
            

            
} 

           
            else {
                
            imageData2.data[((imageWidth * i) + j) * 4] = -1*(data[(collm1 + j-1) * 4]) + (-1*(data[(collm1 + j) * 4]))+(-1*(data[(collm1 + j+1) * 4]))+(-1*data[((i*imageWidth)+(j-1))*4])+(8*data[((imageWidth * i) + j) * 4])+(-1*data[((imageWidth * i) + j+1) * 4])+ ((-1)*(data[(collp1 + j-1) * 4]))+(-1*data[((imageWidth * i) + j) * 4]) + (-1)*(data[(collp1 + j) * 4])+ (-1)*(data[(collp1 + j+1) * 4])+0.5*mouseMod2;
            imageData2.data[((imageWidth * i) + j) * 4+1] = -1*(data[(collm1 + j-1) * 4+1]) + (-1*(data[(collm1 + j) * 4+1]))+(-1*(data[(collm1 + j+1) * 4+1]))+(-1*data[((i*imageWidth)+(j-1))*4+1])+(8*data[((imageWidth * i) + j) * 4])+(-1*data[((imageWidth * i) + j+1) * 4+1])+ (-1)*(data[(collp1 + j-1) * 4])+(-1)*(data[(collp1 + j) * 4+1])+(-1)*(data[(collp1 + j+1) * 4+1])+(-1)*mouseMod2+ 0.125*mouseMod2;
            imageData2.data[((imageWidth * i) + j) * 4+2] = -1*(data[(collm1 + j-1) * 4+2]) + (-1*(data[(collm1 + j) * 4+2]))+(-1*(data[(collm1 + j+1) * 4+2]))+(-1*data[((i*imageWidth)+(j-1))*4+2])+(8*data[((imageWidth * i) + j) * 4])+(-1*data[((imageWidth * i) + j+1) * 4+2])+(-1*data[((collp1 + j) + j-1) * 4+2]) + (-1)*(data[(collp1 + j) * 4+2])+ (-1)*(data[(collp1 + j+1) * 4+2])+0.1*mouseMod;
            imageData2.data[((imageWidth * i) + j) * 4+3] = mouseX/mouseY*255;
            
                
            }           }
        }
           
        context.putImageData(imageData2,0,0);//put new data into canvas
		requestAnimationFrame(draw);
      };
 
 
      
		requestAnimationFrame(draw);
 
          function getMouse(mousePosition) {
                mouseX = mousePosition.layerX;
                mouseY = mousePosition.layerY;
        }     
    }

</script>

</body>

</html></html>
