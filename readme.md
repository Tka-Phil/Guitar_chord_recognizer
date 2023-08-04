# Guitar chord recognizer
![IMG_6660](https://github.com/Tka-Phil/Guitar_chord_recognizer/assets/141285613/5354979f-ba7e-4d90-bd27-419129004686)

This progect uses AI ti recognize guitar chords by looking at fingers position. It can be very helpful for begginer guitar palyers who want to learn basic chords. 
## Hardware requierments
To repeat this project you will need Jetson-Nano( https://www.amazon.com/NVIDIA-Jetson-Nano-Developer-945-13450-0000-100/dp/B084DSDDLT/ref=sr_1_3?crid=NIGDWOZSZ9E7&keywords=jetson+nano&qid=1691096626&sprefix=jetson+nano+%2Caps%2C145&sr=8-3 ) and a webcam ( https://www.amazon.com/Webcam-Streaming-Recording-Built-Correction/dp/B07M6Y7355/ref=sr_1_3?crid=3Q0Z371SBVH59&keywords=webcam&qid=1691096724&sprefix=webcam%2B%2Caps%2C153&sr=8-3&th=1 ).

## How does the algorithm work?
![IMG_6661](https://github.com/Tka-Phil/Guitar_chord_recognizer/assets/141285613/129513ff-683f-4d16-8b34-1a0ddc77de2a)

My project uses Imagnet to detect different guitar chords. The model receives video frames as input and outputs the probability of each chord.
![IMG_6662](https://github.com/Tka-Phil/Guitar_chord_recognizer/assets/141285613/2c183fc1-33c0-4065-8024-d2d663b850e0)
![IMG_6663](https://github.com/Tka-Phil/Guitar_chord_recognizer/assets/141285613/dd5054f0-7314-4a0b-929e-19678ce202d3)

## Running this project

1. As it was mentioned my project uses Imagnet to detect chords, so to run the chord recognizer, you will need to download it. Use this link to download Imagnet: https://github.com/dusty-nv/jetson-inference/blob/master/docs/building-repo-2.md 
2. After copy my code: git clone git@github.com:raiwal/chords.git
3. Go to chords ( cd chords )
4. Run this comand: python3 src/main.py --model=model/resnet18.onnx  --input_blob=input_0 --output_blob=output_0 --labels=labels.txt  /dev/video0

where:
  " --model=model/resnet18.onnx "  - specifies path to network file that will be used to identify the image.
  " --labels=labels.txt "  - sets the chord labels.
  " /dev/video0 "  - shows the video from camera 0. 

  ## Suppored chords
  Am
  C
  Em
  Dm
  F
  

[View a video explanation here](video link)
