Let's calculate the output size of the convolutional layer step by step for both height and width.

### Given Parameters:
- **Input size (height, width, channels)**: \(32 \times 32 \times 3\)
- **Filter size**: \(5 \times 5\)
- **Number of filters**: 10
- **Stride**: 2
- **Padding**: 2
- **Pooling size**: \(2 \times 2\)

### Step 1: Calculate Convolutional Layer Output Size
To calculate the output size for height and width after the convolutional layer, we use the formula:

\[
\text{Output size} = \frac{(\text{Input size} - \text{Filter size} + 2 \times \text{Padding})}{\text{Stride}} + 1
\]

#### For Height:
1. **Input height**: 32
2. **Filter height**: 5
3. **Padding**: 2
4. **Stride**: 2

Now apply the formula:

\[
\text{Output height} = \frac{(32 - 5 + 2 \times 2)}{2} + 1
\]
\[
\text{Output height} = \frac{(32 - 5 + 4)}{2} + 1 = \frac{31}{2} + 1 = 15.5 + 1 = 16.5 \approx 16
\]

#### For Width:
1. **Input width**: 32
2. **Filter width**: 5
3. **Padding**: 2
4. **Stride**: 2

Now apply the same formula for width:

\[
\text{Output width} = \frac{(32 - 5 + 2 \times 2)}{2} + 1
\]
\[
\text{Output width} = \frac{(32 - 5 + 4)}{2} + 1 = \frac{31}{2} + 1 = 15.5 + 1 = 16.5 \approx 16
\]

So, the output size after the convolutional layer is \(16 \times 16 \times 10\) (height \(\times\) width \(\times\) number of filters).

### Step 2: Apply Pooling Layer
The pooling layer reduces the spatial dimensions by using a pooling size of \(2 \times 2\) and stride of 2.

The output size after pooling is:

\[
\text{Output size after pooling} = \frac{\text{Convolutional output size}}{\text{Pooling size}}
\]

#### For Height:
\[
\text{Output height after pooling} = \frac{16}{2} = 8
\]

#### For Width:
\[
\text{Output width after pooling} = \frac{16}{2} = 8
\]

So, the output size after the pooling layer is \(8 \times 8 \times 10\).

### Step 3: Calculate Total Number of Parameters
The total number of parameters in the convolutional layer is given by:

\[
\text{Total parameters} = (\text{Filter height} \times \text{Filter width} \times \text{Number of input channels} + 1) \times \text{Number of filters}
\]

- **Filter height**: 5
- **Filter width**: 5
- **Number of input channels**: 3
- **Number of filters**: 10

Substitute the values:

\[
\text{Total parameters} = (5 \times 5 \times 3 + 1) \times 10
\]
\[
\text{Total parameters} = (75 + 1) \times 10 = 760
\]

### Final Output:
- **Convolutional layer output size**: \(16 \times 16 \times 10\)
- **Pooling layer output size**: \(8 \times 8 \times 10\)
- **Total parameters**: 760

This is the step-by-step calculation for both the height and width of the convolutional and pooling layers, along with the number of parameters.
