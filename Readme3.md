Max pooling, average pooling, and min pooling are techniques used in convolutional neural networks (CNNs) to downsample feature maps. Each method aggregates information differently, which affects the output feature maps. Below are detailed explanations and examples for each pooling method.

## Max Pooling

**Process:**
Max pooling selects the maximum value from a specified window (or kernel) as it slides over the input feature map. This technique helps to retain the most significant features while reducing dimensionality.

**Example:**
Consider a 4x4 input matrix:

```
Input Matrix:
[[1, 3, 2, 4],
 [5, 6, 1, 2],
 [9, 7, 8, 3],
 [4, 0, 2, 1]]
```

Using a 2x2 max pooling filter with a stride of 2:

1. **First Position (Top-Left):**
   - Covered values: 
     ```
     [[1, 3],
      [5, 6]]
     ```
   - Max value = **6**

2. **Second Position (Top-Right):**
   - Covered values:
     ```
     [[2, 4],
      [1, 2]]
     ```
   - Max value = **4**

3. **Third Position (Bottom-Left):**
   - Covered values:
     ```
     [[9, 7],
      [4, 0]]
     ```
   - Max value = **9**

4. **Fourth Position (Bottom-Right):**
   - Covered values:
     ```
     [[8, 3],
      [2, 1]]
     ```
   - Max value = **8**

The output matrix after max pooling is:

```
Output Matrix:
[[6, 4],
 [9, 8]]
```

For a visual representation of max pooling, refer to this image: [Max Pooling Example](https://www.digitalocean.com/community/tutorials/pooling-in-convolutional-neural-networks).

## Average Pooling

**Process:**
Average pooling computes the average of all values within the specified window as it slides over the input feature map. This method retains more information than max pooling by considering all values.

**Example:**
Using the same input matrix:

```
Input Matrix:
[[1, 3, 2, 4],
 [5, 6, 1, 2],
 [9, 7, 8, 3],
 [4, 0, 2, 1]]
```

With a 2x2 average pooling filter and a stride of 2:

1. **First Position (Top-Left):**
   - Covered values:
     ```
     [[1, 3],
      [5, 6]]
     ```
   - Average = (1 + 3 + 5 + 6) / 4 = **3.75**

2. **Second Position (Top-Right):**
   - Covered values:
     ```
     [[2, 4],
      [1, 2]]
     ```
   - Average = (2 + 4 + 1 + 2) / 4 = **2.25**

3. **Third Position (Bottom-Left):**
   - Covered values:
     ```
     [[9, 7],
      [4, 0]]
     ```
   - Average = (9 + 7 + 4 + 0) / 4 = **5.00**

4. **Fourth Position (Bottom-Right):**
   - Covered values:
     ```
     [[8, 3],
      [2, 1]]
     ```
   - Average = (8 + 3 + 2 + 1) / 4 = **3.50**

The output matrix after average pooling is:

```
Output Matrix:
[[3.75, 2.25],
 [5.00, 3.50]]
```

For a visual representation of average pooling, refer to this image: [Average Pooling Example](https://www.digitalocean.com/community/tutorials/pooling-in-convolutional-neural-networks).

## Min Pooling

**Process:**
Min pooling selects the minimum value from the specified window as it slides over the input feature map. This method is less common but can be useful in specific contexts where retaining lower values is important.

**Example:**
Using the same input matrix:

```
Input Matrix:
[[1, 3, 2, 4],
 [5, 6, 1, 2],
 [9, 7, 8, 3],
 [4, 0, 2, 1]]
```

With a similar setup using a min pooling filter with a size of $$2 \times 2$$ and stride $$=2$$:

1. **First Position (Top-Left):**
   - Covered values:
     ```
     [[1, 3],
      [5, 6]]
     ```
   - Min value = **1**

2. **Second Position (Top-Right):**
   - Covered values:
     ```
     [[2, 4],
      [1, 2]]
     ```
   - Min value = **1**

3. **Third Position (Bottom-Left):**
   - Covered values:
     ```
     [[9, 7],
      [4,0]]
     ```
   - Min value = **0**

4. **Fourth Position (Bottom-Right):**
   - Covered values:
     ```
     [[8 ,3],
      [2 ,1]]
     ```
   - Min value = **1**

The output matrix after min pooling is:

```
Output Matrix:
[[1 ,1 ],
 [0 ,1 ]]
```

For a visual representation of min pooling and its applications in CNNs refer to this image: [Min Pooling Example](https://www.digitalocean.com/community/tutorials/pooling-in-convolutional-neural-networks).

Citations:
[1] https://www.fynd.academy/blog/pooling-layers-in-cnn
[2] https://www.nature.com/articles/s41598-024-51258-6
[3] https://www.digitalocean.com/community/tutorials/pooling-in-convolutional-neural-networks
[4] https://www.youtube.com/watch?v=gNRVTCf6lvY
[5] https://www.geeksforgeeks.org/cnn-introduction-to-pooling-layer/
[6] https://www.almabetter.com/bytes/articles/an-introduction-to-pooling-layers-for-convolutional-neural-networks
[7] https://www.educative.io/answers/what-are-some-deep-details-about-pooling-layers-in-cnn
[8] https://www.sciencedirect.com/topics/computer-science/average-pooling
