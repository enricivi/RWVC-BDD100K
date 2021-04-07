# RWVC-BDD100K
Currently under review

## Dataset
BDD100K \[1\] is a large scale driving video dataset, which comprises different scenes types, such as city, street, residential areas and highways. Moreover, it has been captured under various weather conditions and time of the day.
The dataset contains 100K videos, each of which has been annotated at the 10-th frame, resulting in a total of 100K images manually annotated for a number of different tasks, including object detection or image segmentation.
Each annotated image includes a label about the atmospheric weather condition (snowy, rainy, clear), but it does not identify the actual road  weather status (snow, wet, dry); many images marked as rainy or snowy do not show wet or snowy road, as reported by \[2\]. Furthermore, BDD100K does not provide any label on general visibility. Thus, we selected a subset of 13.3K images captured at different times of the day and we manually annotated them. We refer to this subset of BDD100K as the RWVC-BDD dataset.

The selected images are split into training (8.8K images), validation (2.5K) and test (2K). On each slice we keep roughly the same distribution of road, visibility, weather and time of the day annotations.

We describe in detail the annotations in the following subsections, while in the histograms below we report the distributions of the different annotations of the RWVC-BDD dataset.

### Road condition
We identify three different categories for road condition: *wet*, *dry* and *snowy*. *Dry* label identifies a totally dry road. *Wet* and *snowy* labels denote a drivable area, which is partially or totally characterized by the presence of water or ice/snow respectively. In case both water and snow are present in the drivable area, we decided to annotate the road as *snowy*.

### Weather
Weather annotations are the original BDD100K annotations and they identify the current scene weather without taking into account the road condition. In the original dataset, the climate conditions are identified by *clear*, *overcast*, *snowy*, *rainy*, *cloudy* and *foggy* tags. We selected a subset of BDD100K with the labels *clear*, *rainy* and *snowy*.

### Visibility
We define two different categories for visibility: *poor* indicates that rain drops, snowflakes or dirt on the windshield are deteriorating the visibility; if that's not the case, the visibility is marked as *good*. In addition to the cases described above, we annotate with visibility *poor* all the images with visible windshield wipers, since wipers in action are a good proxy to determine that the general visibility for the driver is compromised.

## Histograms
Road | Weather | Visibility
---- | ------- | ----------
![road](/images/road.png) | ![weather](/images/weather.png) | ![visibility](/images/visibility.png)

## Main References
\[1\] Yu Fisher, Haofeng Chen, Xin Wang, Wenqi Xian, Yingying Chen, Fangchen Liu, Vashisht Madhavan, and Trevor Darrell. "BDD100K: A Diverse Driving Dataset for Heterogeneous Multitask Learning", 2020 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), Seattle, WA, USA, 2020, pp. 2633-2642, doi: [10.1109/CVPR42600.2020.00271](https://doi.org/10.1109/CVPR42600.2020.00271).

\[2\] Tobias Weber, E. Ercelik, M. Ebert and A. Knoll, "Recognition & Evaluation of Additional Traffic Signs on the example of '80 km/h when wet'", 2019 IEEE Intelligent Transportation Systems Conference (ITSC), Auckland, New Zealand, 2019, pp. 4134-4139, doi: [10.1109/ITSC.2019.8916950](https://doi.org/10.1109/ITSC.2019.8916950). 
