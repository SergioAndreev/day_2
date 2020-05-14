### Exercise 5: Converting Caffe Model to Intermediate Representation

1. Navigate to `/home/sensors/Downloads/
2. Create new directory `Caffe`
3. Download the SqueezeNet model from [here](https://github.com/forresti/SqueezeNet) using the following command:

`git clone https://github.com/DeepScale/SqueezeNet`

<details><summary>git clone log</summary>
<p>

```python
Cloning into 'SqueezeNet'...
remote: Enumerating objects: 107, done.
remote: Total 107 (delta 0), reused 0 (delta 0), pack-reused 107
Receiving objects: 100% (107/107), 8.83 MiB | 0 bytes/s, done.
Resolving deltas: 100% (49/49), done.
Checking connectivity... done.
```

</p>
</details>

4. Now let’s find SqueezeNet V1.1 model’s .caffemodel file and a .prototxt file which need to feed into the Model Optimizer. Just type `ls`

<details><summary>git clone log</summary>
<p>

```python
deploy.prototxt - please take a look this file using cat, you see about a hundred of layers which is considered as a deploy-ready prototxt file that contains a topology structure and layer attributes
Reference: Converting a Caffe* Model

solver.prototxt - additional training details (we don’t need it here)

README.md - A README.md is a reference for other users visiting a repository and documents steps for them to get a model up and running.
Reference: What is README.MD file and why do I need it?

solver.prototxt - additional training details (learning rate schedule, etc.) (we don’t need it here)

squeezenet_v1.1.caffemodel - pretrained model parameters

train_val.prototxt - model architecture (we don’t need it here)

Reference: SqueezeNet
```

</p>
</details>
