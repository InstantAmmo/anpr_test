SSD-MobileNet model based off of detectnet here: https://github.com/dusty-nv/jetson-inference/blob/master/docs/pytorch-ssd.md

You can downlaod a base model (without the number plates trained, here):

$ cd jetson-inference/python/training/detection/ssd

$ wget https://nvidia.box.com/shared/static/djf5w54rjvpqocsiztzaandq1m3avr7c.pth -O models/mobilenet-v1-ssd-mp-0_675.pth

$ pip3 install -v -r requirements.txtYou can find docs for the original detectnet/SSD-MobileNet model that I am here: https://github.com/dusty-nv/jetson-


detectnet --model=models/fruit/ssd-mobilenet.onnx --labels=models/fruit/labels.txt \
          --input-blob=input_0 --output-cvg=scores --output-bbox=boxes \
            csi://0
