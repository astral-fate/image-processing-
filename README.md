# image-processing



         BufferedImage bi = new BufferedImage(500, 400, BufferedImage.TYPE_INT_BGR);

        Graphics2D imgx = (Graphics2D) (bi.createGraphics());

        g2.drawImage(bi, 0, 0, this);

        try {

            bi = ImageIO.read(new File("D:\\New folder\\Skel\\src\\skel\\sun.jpg"));
           // ImageIO.read(bi, "jpg", bi);

        } catch (IOException ex) {

        }
        
        
