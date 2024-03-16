1. **Convolutional Layer (First Convolutional Layer)**:
   - The first convolutional layer has a kernel size of 7x7, operates on 3 input channels, and produces 64 output channels.
   - Parameters are calculated using the formula: `(kernel_height * kernel_width * input_channels + 1) * output_channels`.
   - Total parameters: `(7 * 7 * 3 + 1) * 64`

2. **Residual Blocks**:
   - Each residual block consists of two convolutional layers, each with a kernel size of 3x3 and producing 64 output channels. Additionally, there's a 1x1 convolutional layer for the shortcut connection.
   - Parameters are calculated for each block using the formula: `((kernel_height * kernel_width * input_channels + 1) * output_channels * 2) + ((1 * 1 * input_channels + 1) * output_channels)`.
   - Since there are 4 residual blocks in total, the parameters for all blocks are multiplied by 4.
   - Total parameters for all blocks: `((3 * 3 * 64 + 1) * 64 * 2 + (1 * 1 * 64 + 1) * 64) * 4`

3. **Global Average Pooling Layer**:
   - The global average pooling layer does not have any parameters associated with it.
   - Total parameters: `0`

4. **Fully Connected Layer (Dense Layer)**:
   - The dense layer for binary classification has 512 input units and 1 output unit.
   - Parameters are calculated using the formula: `(input_units + 1) * output_units`.
   - Total parameters: `(512 + 1) * 1`

Finally, the total number of parameters is obtained by summing up the parameters from all layers.

These calculations yield a total of 11,191,425 trainable parameters in the ResNet model.
