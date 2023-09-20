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
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/21872f44-2312-4372-9fe4-ad18682e0093)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/84e49297-26a3-48c1-8a29-6485f254f0ad)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/090a70d4-5ab6-4f89-8a5c-c2907ad62dab)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/b9562132-182f-411a-9884-a9166e49f043)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/e8c07ea9-5329-4369-8891-13389327dbc9)


EXPONENT - 8 & MATRIX SIZE - 512
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/55bfa326-e5aa-429e-a13c-ae508d99e7c7)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/e72fe264-b7c8-49f8-aa69-1f588a4b177f)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/1ad07c6e-4fb1-43e6-982f-d8945bf0300d)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/73d8252f-3cdb-4280-9655-70fd9dac7161)

EXPONENT - 8 & MATRIX SIZE - 1024
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/30a9d681-5aaf-41af-9da4-1fbb2ec09004)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/4a5beaa0-e36a-4f8e-a817-130620591f2a)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/7114edd4-42da-40b8-8242-143b550ec804)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/0a3fa688-9f90-451d-bb72-e7d4b957b8ab)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/e63a565d-c3f2-4bcc-9861-a5a1bda5a105)

EXPONENT - 8 & MATRIX SIZE - 2048
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/389a29aa-ae5f-4242-b033-c9a5bf3763e5)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/6c1ffb6b-8bf2-46e0-81d7-a5ce923e7bb7)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/1b242326-b127-46da-8424-ce935693721d)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/1ed68716-e54b-4154-8c57-ef23fc8e262b)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/bf7c7fad-6bc3-492c-ad4e-99430323c068)

b. Runtime vs. Matrix Sizes by fixing number of threads (Matrix Sizes - 512, 1024, 2048)
- in this we kept thread number as constant in each case and changed the matix sizes
- Block size varies between 4,16,32
Threads constant as 8
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/a761fe56-8692-4fe8-9b9d-1c4c1f7a561c)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/1fd77cbe-c46b-4d05-9714-ee615412c35a)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/88d206cb-3c13-43df-9262-7b656ee3825b)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/ac8312f0-ca17-4074-902f-86e8368d235d)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/5c5da6c7-8809-49d6-9bc6-c7f0c74723c1)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/5f90c542-d2db-47d7-b54a-112924d19076)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/e2d2bdb6-aba2-48e2-9664-940f50cc7a10)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/0d7f0ac2-6c39-4b7c-9686-fb28f6e52c7c)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/8cf1453a-4afa-4b8c-9f9a-61a88612b13a)


Threads constant as 16
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/4c443e0d-6e95-4093-a278-f2051f885434)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/cecef442-1160-4a10-94ce-71b811030e17)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/1c50ae59-1103-47de-a649-0cd0c91b7b34)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/2c9094c4-9d66-4a30-82e7-4cc2d2eb3d2e)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/3e21827c-df79-40c7-b5a4-efe7b8b80a5b)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/66b200e1-54e7-4ee4-8218-396bbbaf10e7)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/83aebb8a-86e6-4ffb-aeba-cf35950c5ed0)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/8bf57882-c7fc-4c31-a47b-9fdf6fa21463)
![image](https://github.com/harshakarnam57/HPC1/assets/64098766/a969e931-025b-4f1b-b136-ce384edf4ddb)
