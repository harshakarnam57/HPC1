#  Parallel coding using OpenMP 
### Different types of Matrix Multiplication
##### 1. Ordinary Matrix Multiplication (OMM).
##### 2. Block Matrix Multiplication (BMM) using block sizes: 4,8,16,32,64.
##### 3. Tranpose of A to find nth Power using OMM.
##### 4. Tranpose of A to find nth Power using BMM.
### Graphs the different types of Multiplications
##### a. Runtime vs. Matrix Sizes by fixing number of threads
##### b. Runtime vs. Threads by fixing the Matrix Size.
***
### 1. Ordinary Matrix Multiplication (OMM).
Code Description
- Initializes matrices A and B with random values.
- Allows us to specify the number of threads for parallelization.
- Uses OpenMP to parallelize the matrix multiplication.
- Measures the elapsed time for the multiplication process.
- Outputs the elapsed time in seconds.
### Graphs
a. Runtime vs. Threads by fixing the Matrix Size. (Threads varies as 1,2,4,6,8,10,12,14,16)

![image](https://github.com/harshakarnam57/HPC1/assets/64098766/0f683e52-c70e-489d-9149-eab2acec4333)

![image](https://github.com/harshakarnam57/HPC1/assets/64098766/61a14512-29a4-4c15-bac1-28b8ca75b696)

![image](https://github.com/harshakarnam57/HPC1/assets/64098766/f06fc3ea-9167-4c0a-9013-9ce527b9fe5b)

b. Runtime vs. Matrix Sizes by fixing number of threads (Matrix Sizes - 512, 1024, 2048)
 
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/2719071c-2a32-4bf4-885f-aa4b4d3ce334)

![image](https://github.com/harshakarnam57/HPC1/assets/64098766/a71bab12-19bf-4248-a2d7-22ca0b82a97f)

![image](https://github.com/harshakarnam57/HPC1/assets/64098766/22be9028-a58e-4f35-9e51-330c97482599)

![image](https://github.com/harshakarnam57/HPC1/assets/64098766/7ffb151f-853e-488b-9490-1f0ce04cdd1e)

![image](https://github.com/harshakarnam57/HPC1/assets/64098766/1c13d9f1-9573-4d5c-a034-d88d02ec241c)

![image](https://github.com/harshakarnam57/HPC1/assets/64098766/4e50f790-c617-411a-bac6-307a50c56ad5)

![image](https://github.com/harshakarnam57/HPC1/assets/64098766/0636973f-73c0-4203-8324-1310b4ba213c)

![image](https://github.com/harshakarnam57/HPC1/assets/64098766/c06a3c68-55aa-4d11-a2d2-52f6c355c9ed)
***
### 2. Block Matrix Multiplication (BMM) using block sizes: 4,8,16,32,64.
- Initialization of Matrices A and B:

We start by initializing matrices A and B with random values. This step ensures that our matrices have valid data for multiplication.
User-Defined Thread Count:

We give you the flexibility to specify the number of threads to be used for parallelization. This allows you to optimize performance based on the number of available CPU cores or other considerations.

- Parallel Matrix Multiplication with OpenMP:

The core of our implementation lies in parallelizing the matrix multiplication using OpenMP. OpenMP allows us to harness the power of multiple threads and divide the workload efficiently.
To achieve this, we break the matrix into smaller blocks and distribute these blocks among the threads for simultaneous computation.

- Exploring Block Sizes:

We understand that different block sizes can have varying impacts on performance. Therefore, our program lets you specify the block size.
Matrix multiplication is carried out by taking into account these block sizes, allowing you to experiment and analyze the effects on execution time.

- Timing the Process:

To evaluate the efficiency of our BMM implementation, we measure the elapsed time for the entire matrix multiplication process.
We utilize functions like gettimeofday() to ensure accurate timing and capture the start and end times.

- Outputting Elapsed Time:

After completing the matrix multiplication, we provide you with the elapsed time in seconds.
This information is invaluable for assessing the efficiency of our BMM algorithm under different configurations.


### Graphs
a. Runtime vs. Threads by fixing the Matrix Size. (Threads varies as 1,2,4,6,8,10,12,14,16)
- For Matrix odf size 2048 and blocks size varies as 4,8,16,32,64

![image](https://github.com/harshakarnam57/HPC1/assets/64098766/d9884930-bda5-45b0-afff-3ef2b5894b7a)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/961990ce-9aa1-404b-9de6-25b4d46223d2)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/bdae1934-be0b-446d-b1f7-a7d73b20492c)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/95bda829-006e-482e-bbf3-f21b0431d139)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/a54e8c52-aff2-40e2-9eeb-49aec048bd0a)

- For Matrix odf size 1024 and blocks size varies as 4,8,16,32,64
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/e9b5eb6d-d7da-4500-82bc-13ac7be2ee6d)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/abed6242-3016-48a4-a1dd-e3596bdcf1d3)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/191ad723-f49e-496b-b802-6e85a1159d1c)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/d96c4990-d6b9-4a52-9128-fd50e096d190)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/a3b08745-8a32-4a6b-9f22-cd1e7c4e0fe8)

- For Matrix odf size 512 and blocks size varies as 4,8,16,32,64
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/cde150fb-fc1a-4472-a205-0cd58dba21da)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/9b529772-2695-459c-a6d3-23201d2333ad)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/eeb0792e-e213-46cd-823f-1a491a0b33e8)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/a0681ea8-d7b9-4fc3-825c-6b295cff5b21)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/33d03831-9e77-4440-903d-8698f9fab9c8)

b. Runtime vs. Matrix Sizes by fixing number of threads (Matrix Sizes - 512, 1024, 2048)
- in this we kept thread number as constant in each case and changed the matix sizes
  
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/808f3c2c-ee65-4032-8fcd-8f8a34c852da)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/e1478f3e-251e-42cd-a5c0-e3ac17e7a443)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/016c792e-8ea4-4549-bc76-c723b6f0e1f3)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/090b7698-005c-4f5a-a38e-6636002d9876)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/cb56c506-e4be-4ea4-bfb8-f06eb9a0d1fe)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/d33216a6-8224-4582-a7c0-e0b5070afbd2)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/811fb373-f4cf-4e0d-9c96-c5e0023cd723)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/a706c173-3e4a-4d3b-a47b-5f1fb5f715a1)

***
##### 3. Tranpose of A to find nth Power using OMM.
- Initialization of Matrix A :

We start by initializing matrices A with random values. This step ensures that our matrices have valid data for multiplication.

-User-Defined Thread Count:

We give you the flexibility to specify the number of threads to be used for parallelization. This allows you to optimize performance based on the number of available CPU cores or other considerations.

- Transpose of A
  - In the regular matrix multiplication, basically we multply row of one matrix with column of another 
    matrix, instead in this transpose approach if we transpose atleast one matrix in matrix multiplication 
    process we can directly multply row with row, this helps to reduce the run time.
  - in oue approach we varied n between 2-16 where N is exponent of Am A is the matrix with order varies 
    between 512 & 2048.
  - Here exponent implies number of times of multiplication of matrix A with itself.  

- Parallel Matrix Multiplication with OpenMP:

The core of our implementation lies in parallelizing the matrix multiplication using OpenMP. OpenMP allows us to harness the power of multiple threads and divide the workload efficiently.
To achieve this, we break the matrix into smaller blocks and distribute these blocks among the threads for simultaneous computation.

- Outputting Elapsed Time:

After completing the matrix multiplication, we provide you with the elapsed time in seconds.
This information is invaluable for assessing the efficiency of our BMM algorithm under different configurations.

### Graphs
a. Runtime vs. Threads by fixing the Matrix Size. (Threads varies as 1,2,4,6,8,10,12,14,16)

- EXPONENTS i.e, no of Matrixes being multiplied in an itreation will be from 2 to 10.
  
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/291524fc-f608-4a18-bed0-946d516ac623)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/018987df-18a3-43f5-99b7-562416ea8a25)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/d9db996e-361d-4dd2-a7c9-d147f5620fb1)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/ade2b64e-31a4-4485-a45b-37cc2e8172c3)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/773bf764-65f4-4bfd-9fce-c4340c0c04ea)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/cfb2de6d-f0ef-46de-988b-6be95e0543b9)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/2f9cee48-3af7-4dd9-bda4-1fb7ae2482f6)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/0c688239-2c17-4ef2-8499-0f4ef7af29b7)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/cef33792-95e7-4949-b46d-ec5215c35d0b)



##### 4. Tranpose of A to find nth Power using BMM.

We start by initializing matrices A with random values. This step ensures that our matrices have valid data for multiplication.
- Transpose of A
  - In the regular matrix multiplication, basically we multply row of one matrix with column of another 
    matrix, instead in this transpose approach if we transpose atleast one matrix in matrix multiplication 
    process we can directly multply row with row, this helps to reduce the run time.
  - in oue approach we varied n between 2-16 where N is exponent of Am A is the matrix with order varies 
    between 512 & 2048.
  - Here exponent implies number of times of multiplication of matrix A with itself.
 
- Exploring Block Sizes:

We understand that different block sizes can have varying impacts on performance. Therefore, our program lets you specify the block size.
Matrix multiplication is carried out by taking into account these block sizes, allowing you to experiment and analyze the effects on execution time.

- Timing the Process:

To evaluate the efficiency of our BMM implementation, we measure the elapsed time for the entire matrix multiplication process.
We utilize functions like gettimeofday() to ensure accurate timing and capture the start and end times.

- Outputting Elapsed Time:

After completing the matrix multiplication, we provide you with the elapsed time in seconds.
This information is invaluable for assessing the efficiency of our BMM algorithm under different configurations.


### Graphs
a. Runtime vs. Threads by fixing the Matrix Size. (Threads varies as 1,2,4,6,8,10,12,14,16)
- For Matrix odf size 2048 and blocks size varies as 4,8,16,32,64
  
EXPONENT - 2 & MATRIX SIZE - 2048

![image](https://github.com/harshakarnam57/HPC1/assets/64098766/352c646d-b233-464e-aecc-b05ae4708faf)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/8462ca81-d903-4612-8298-ea2fcd4547b7)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/68da22ab-b9c4-4581-9863-f573d4d5a325)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/a5248019-515e-409a-b94c-35473cd532a3)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/5c61037a-39d4-4a2c-ad4a-706f464bff40)

EXPONENT - 2 & MATRIX SIZE - 1024
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/11ba449d-a2e5-4856-88e6-b4644f81a5e1)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/d5e9f58a-7f2d-4efe-87d3-b48d2107203b)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/d24597fa-5ec8-4c2e-ae89-43d5c636da36)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/4b404246-7d7a-471c-b1e6-64f426e8ac29)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/9781f57b-a083-4c2b-9e1f-ccff9d7a5f35)

EXPONENT - 2 & MATRIX SIZE - 512
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/5c3e81a9-126a-4b79-b521-d29de35d4b34)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/a157785f-0436-4760-8bac-6da8093b57ce)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/96e42d8b-5b69-457c-9311-c765d0b2263a)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/48233d44-2d7f-4a6e-91e3-fd837dc0775e)

EXPONENT - 8 & MATRIX SIZE - 512
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/341ea1f7-43d0-4eda-9e64-11d7a47fa4ea)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/c2152df6-b9d3-4769-ac32-4182d8f9bf51)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/ceb805e3-efbb-4eff-82c5-6b6b32fd549a)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/ea84b3c3-3a28-4bbb-8e4f-1d6016c778d4)

EXPONENT - 8 & MATRIX SIZE - 1024
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/87b792a1-1760-4a2a-9e8f-c93744717013)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/5e9e1a2e-0a2f-4ea2-9f99-e4f0ed834105)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/0b7865ac-7c39-43cb-b5c3-46acf1508e8f)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/13d2ec77-8e0c-4b72-8d15-1a7818da472c)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/7c1873d4-e09f-488e-a06c-e51f9641ff9a)

EXPONENT - 8 & MATRIX SIZE - 2048
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/6840c506-ce62-4310-a5e4-7aee0ab1f548)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/8cf20c33-02e5-43f7-8f21-81bdf35c1814)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/c835c586-be55-4283-9f5b-c4413ba63e99)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/6ba4f24d-a67b-4e2a-8cb4-809e04bd9e20)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/14b75724-837a-4aa7-a71c-be90649f4f24)

b. Runtime vs. Matrix Sizes by fixing number of threads (Matrix Sizes - 512, 1024, 2048)
- in this we kept thread number as constant in each case and changed the matix sizes
- Block size varies between 4,16,32
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/47bd9cbe-5024-4da0-8ed3-6e6990de2bf8)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/ac9471b9-3bae-4889-bb5d-2afad02a8ab7)
![image](https://github.com/chaitanyabalajireddy/HPC_Assignment-_1/assets/91625648/faf2e964-963d-4776-b67f-d503e4369b42)

Threads constant as 8 

