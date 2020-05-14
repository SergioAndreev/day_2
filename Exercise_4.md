# Day_2
You will need the following for sure =)

### Exercise 4: Converting Tensorflow Model

1. Navigate to `/home/sensors/Downloads`
2. Create here the folder `TF`
3. Go inside the `TF` folder
4. Download `MobileNet SSD` from the website. To do that type `wget _link_` (instead of `_link_` paste this: http://download.tensorflow.org/models/object_detection/ssd_mobilenet_v2_coco_2018_03_29.tar.gz). 

*Remember, that you need to use `Ctrl+Shift+V` combination to be able to paste the link to the terminal.*
5. After completing the download, use `tar -xvf _the_name_of_the_archive_` to unpack it. (instead of `_the_name_of_the_archive_` use `ssd_mobilenet_v2_coco_2018_03_29.tar.gz`). 

*Remember that you do not need to copy the name of the archive from here! Just type* `tar -xvf ssd` *and then press Tab to autofill*
6. To convert this model from Tensorflow model to Intermediate Representation, use the command: `python /opt/intel/openvino/deployment_tools/model_optimizer/mo.py --input_model frozen_inference_graph.pb --tensorflow_object_detection_api_pipeline_config pipeline.config --reverse_input_channels --tensorflow_use_custom_operations_config /opt/intel/openvino/deployment_tools/model_optimizer/extensions/front/tf/ssd_v2_support.json`

*Remeber to listen to me =) I will describe you this gigantic command in Zoom!*
