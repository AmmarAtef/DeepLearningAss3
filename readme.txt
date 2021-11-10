Q1).
A Convolutional Neural Network (ConvNet/CNN) is a Deep Learning algorithm which can take in an input image,
 assign importance (learnable weights and biases) to various aspects/objects in the image and be able to differentiate one from the other.

 Q2).
 - Stride of 1 and 2
     - In training  data from plottings they get  the same accuracy.
     - Validation Data, in stride 2 it's working a little better I think, but it's very close to each other.
     - stride 1: Test accuracy 0.99200000
       stride 2: Test accuracy 0.99100000
       stride 1 is better by a little 

 - params in each case:
    --in stride 1 :
 the number of params to kernel with 5 size and number of filters 32  get by this equation 
 --> (kernel size^2 + bias)*number of Filters = (5*5 +1)*32 =832) 
 and below you can find the params for all layers 
 +-----------------+------------+
|     Modules     | Parameters |
+-----------------+------------+
|  conv_1.weight  |    800     |
|   conv_1.bias   |     32     |
|  conv_2.weight  |   51200    |
|   conv_2.bias   |     64     |
| linear_1.weight |   204800   |
|  linear_1.bias  |    128     |
| linear_2.weight |    1280    |
|  linear_2.bias  |     10     |
+-----------------+------------+
Total Trainable Params: 258314



    --in stride 2:
 
 the number of params to kernel with 5 size and number of filters 32  get by this equation 
 --> (kernel size^2 + bias)*number of Filters = (5*5 +1)*32 =832) 
 and below you can find the params for all layers 
 +-----------------+------------+
|     Modules     | Parameters |
+-----------------+------------+
|  conv_1.weight  |    800     |
|   conv_1.bias   |     32     |
|  conv_2.weight  |   51200    |
|   conv_2.bias   |     64     |
| linear_1.weight |    8192    |
|  linear_1.bias  |    128     |
| linear_2.weight |    1280    |
|  linear_2.bias  |     10     |
+-----------------+------------+
Total Trainable Params: 61706


Q3) until now the results  tell us that the differance between Test accuracies is 0.001 for stride 1,
 I think it's a small number to build something on it but stride 1 work better than stride 2 by a little,
 but stride 2 has less computations  to do less than stride 1 because it has less Parameters.


 Q4) True, softmax is invariant under translation by the same value in each coordinate: softmax(x) = softmax(x + c)
where x + c means adding the constant c to every dimension of x.
