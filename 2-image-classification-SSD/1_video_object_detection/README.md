# 1_video_object_detection

The neural network model currently loaded is trained on both the 2007 and 2012 datasets of the [PASCAL visual object classes](http://host.robots.ox.ac.uk/pascal/VOC/). As a result, this model is able to detect the following items, among others:
- Person: person
- Animal: bird, cat, cow, dog, horse, sheep
- Vehicle: aeroplane, bicycle, boat, bus, car, motorbike, train
- Indoor: bottle, chair, dining table, potted plant, sofa, tv/monitor

#### To run this implementation:
1. Install the environment based on the `README.md` file from one directory up
1. Download [the neural network weights file](https://1drv.ms/u/s!AhJlq_oIk6K6ghw6CmlowvwwpWSb) to this directory, this file did not fit on Github
1. Run `ssd_detect_objects.py`
1. This will take the `input.mp4` video and classify the objects of every frame.  The output will then be generated as `output.mp4` with the objects labeled.
1. See `input_extra_example.mp4` and `output_extra_example.mp4` for extra examples on how this works.
