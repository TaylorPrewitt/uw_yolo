# Results

The Object Detection project showed that increasing batch inference sizes boosts throughput and yields approximately a 4.5% increase in energy efficiency for each integer increase, resulting in 54% lowered costs, 63% energy savings, and 81% increase in GPU utilization.  

![result_table](https://user-images.githubusercontent.com/80305894/131535780-6c34acd4-d9d1-462a-8f6f-3e54b312ff8d.png)
<sup><i>*Uses NVIDIA T4 GPU</i></sup>
<br>
<sup><i>**CPMI: Cost per million inferences</i></sup>


While batch size was observed reducing overall energy consumption and increasing operational throughput, batching has a mandatory latency requirement.  Without batching, the model can infer detections as soon as the single image is available (real-time), while batching needs to wait for its equivalent number of images to be available (ex: batch size = 8 needs to wait for 8 images to be available).  
 
