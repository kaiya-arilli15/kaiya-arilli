# Kitchen Utensil AI
This project shows the detection of 10 different kitchen utensils. It helps people identify the most common different utensils and cooking ware. There are 10 different kitchenm utensils used: a cheese grater, ladle, large spoon, meat tenderizer, pie server, slotted spoon, spaghetti server, spatula, tongs, and a whisk. This AI was created because I struggled with differentiating the names of a couple of kitchen utensils, this AI helps me do that.

# The Algorithm
My program utilizes imagenet and resnet-18. It uses imagenet to views the live video feed and train the images. Resnet-18 is the base of the AI program. After taking all the pictures and training the dataset, start the live video feed and classifying the images. It uses torch and torchvision to train the model, resnet-18 as the base for my network, and the live video feed to run the imagenet program to classify the utensils.

# Running the Program
1. Login into your nano
2. Click on code and download as a .zip file, upload and unzip in nano under the jetson-inference/python/training/classification directory
3. cd back to jetson-inference
4. Run the docker using docker/run.sh
5. cd into python/training/classification
6. Train the data by using: python3 train.py --model-dir=models/kitchen --batch-size=4 --workers=1 data/kitchen
7. To run the code, type: imagenet --model=models/kitchen/resnet18.onnx --labels=data/kitchen/labels.txt --input-blob=input_0 --output-blob=output_0 /dev/video0
8. Show one of the 10 following items:
    1. cheese grater
    2. ladle
    3. large spoon
    4. meat tenderizer
    5. pie server
    6. slotted spoon
    7. spaghetti server
    8. spatula
    9. tongs
    10. whisk

Required Libraries Needed
1. resnet-18
2. imagenet

View a Video Demonstration Here
