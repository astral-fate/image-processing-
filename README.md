# image-processing



we were so far learning how to deal and manpulate shapes, lines and fonts. Now another advanced topic of java2D is image processing.
just as how we dealt with fonts as characters, or glyph vectors. In order to processing images, we have to define them as components of
Graphics2D by creating a new graphic2d object then casting it, to the new BufferedImage that we have created as follows:



         BufferedImage bi = new BufferedImage(500, 400, BufferedImage.TYPE_INT_BGR);

        Graphics2D imgx = (Graphics2D) (bi.createGraphics());
        
        
        
        
        
        
        
now for drawing the x, and y cordinates that we have assosiate it with the image space, we use a drawImage function.
the parameter of this object is the cordinates of (x,y) and the observer value; which will refer to the same buffered 
image we defined. Hence, we will use (this) on the drawImage parameter. 

        g2.drawImage(bi, 0, 0, this);'
        
        
        
        
now that we have created the space pbject for the image, we want to read, or display an image from the PC. 
by that, we will define a new file that reads an image as follows:

we will define a new bufferedImage as we did beforem but this time we won't assosiate it with any parameter, but we will leave it empty as follows:


          BufferedImage readImage = null;
          
  
  then we will define a new file that reads from the pc, using IOimage as follows:
  
  
          readImage = new IOimage.read (new file("d//sun.jpg"));
          
          
 now since I/O requires certain handling from the cpu, we have to define try catch statment for it, so we affoid errors as follows:
 
           
           
           
           try (){
           readImage = new IOimage.read (new file("d//sun.jpg"));
           
           }
           
           catch (IOexeption ex) {
           }
           
           
  
  then after that, we can print, or display the image we just created by using drawImage as follows:
  
  
                 g2.drawImage(readImage, 0,0 this);
                 
                 
                 
                 
   
   
   hence, the overall code will be like:
   
   
                BufferedImage readImage = null;
         
                        
                try (){
                readImage =  ImageIO.read  (new File("d//sun.jpg"));
           
                 }
           
                 catch (IOException ex) {
                 }
                 g2.drawImage(readImage, 0,0 this);
          




the output will be as follows:


![image](https://user-images.githubusercontent.com/63984422/145833524-1dee434a-c657-4a11-a8e1-e73058947eb3.png)




now for creating an image, and saving it into a file we use the same try catch method, but we use write, instead of read as follows:


        try {

            bi = ImageIO.write(new File("D:\\New folder\\Skel\\src\\skel\\sun.jpg"));
    
        } catch (IOException ex) {

        }
        
        
