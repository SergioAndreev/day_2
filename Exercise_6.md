### Exercise 6: Converting ONNX model to Intermediate Representation

1. Navigate to `/home/sensors/Downloads`
2. Create new folder `ONNX`
3. Go inside it
4. Now download the bvlc_alexnet model from https://s3.amazonaws.com/download.onnx/models/opset_8/bvlc_alexnet.tar.gz with wget:

` wget https://s3.amazonaws.com/download.onnx/models/opset_8/bvlc_alexnet.tar.gz`

5. Now extract the compressed file: `tar -xvf bvlc_alexnet.tar.gz`
6. Change a directory to an extracted folder, `bvlc_alexnet` and check inside with `ls` command:

`cd bvlc_alexnet`

7. Using the `mo_tf.py` script, convert `AlexNet` model to an IR model.

`python3 /opt/intel/openvino/deployment_tools/model_optimizer/mo.py \
  --input_model /home/workspace/bvlc_alexnet/model.onnx`

<details><summary>Details about the command</summary>
<p>

`/opt/intel/openvino/deployment_tools/model_optimizer/mo.py` - Run `mo.py` python script of Model Optimizer

`--input_model /home/workspace/bvlc_alexnet/model.onnx` - Feed in the ONNX model to the Model Optimizer using `--input_model option`.

</p>
</details>

8. Expected log:
```python
# omitted ... 
[ SUCCESS ] Generated IR model. 
[ SUCCESS ] XML file: /home/sensors/Downloads/ONNX/bvlc_alexnet/./model.xml
[ SUCCESS ] BIN file: /home/sensors/Downloads/ONNX/bvlc_alexnet/./model.bin
```

9. Check, that you have converted the model to `model.xml` and `model.bin` files.
