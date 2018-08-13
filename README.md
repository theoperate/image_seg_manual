# Image segmentation manual
# for conv_ocr_v3

## Library
- Use pip install
  - cv2 (pip install opencv-python)
  - numpy (pip install numpy)
  - collections (build in module, Don't need to install)
  - imutils (pip install imutils)
  - matplotlib (pip install matplotlib)
  - pytesseract (pip install pytesseract)

## How install tesseract (for ubuntu)
- Use terminal
  - sudo apt update sudo apt install tesseract-ocr
  - sudo apt-get install tesseract-ocr-all
- Or use this guide
  - https://www.howtoforge.com/tutorial/tesseract-ocr-installation-and-usage-on-ubuntu-16-04/
 
## How install tesseract (for window)
- Use this website
  - https://github.com/UB-Mannheim/tesseract/wiki
  - Download tesseract-ocr-setup-3.05.02-20180621.exe
  - Install tesseract-ocr-setup-3.05.02-20180621.exe
  - go to pytesseract.py in python libraly
  - Change path of tesseract_cmd to tesseract.exe
  
## How to use conv_ocr_v3
Main

    path_to_image = 'path_to_image'

    image = cv2.imread(path_to_image)

    img_list, bnd_list = cha_segment(image)

    num = 0

    for i in img_list:

        for data in bnd_list[num]:
  
            print(data[0],data[1],data[2],data[3])
    
        cv2.imshow('marked areas', j)
  
        cv2.waitKey(0)
  
        num += 1
