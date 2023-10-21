# How to make pain.py work?
![image](https://github.com/CaptnClementine/test/assets/131146976/9be07b5d-485f-464e-9ef7-d58dfb02aa3b)


This README.md will be very useful to answer this question! If you prefer to use environment.yml, do not forget to make sure to follow additional steps carefully.

Don't forget to install mamba if you don't have it! The solution could be sensitive to the operating system type. This project was developed using a virtual machine with Ubuntu (64-bit) on Windows.

## Environment Setup Instructions

1. **Create Mamba Environment:**

   - Create a Conda environment named 'hw_7_env' with Python 3.12:
     ```
     mamba create -n hw7_mamb
     ```

3. **Activate Mamba Environment:**

   - Activate the 'hw7_mamb' environment:
     ```
     mamba activate hw7_mamb
     ```

4. **Install Python:**

   - Install Python 3.12 within the 'hw7_mamb' environment:
     ```
     mamba install python=3.12
     ```

5. **Install Python Packages:**

   - Install required Python packages:
     ```
     pip install google
     pip install --upgrade google-api-python-client
     pip install biopython==1.78
     pip install pandas
     ```

6. **Install OpenCV:**

   - Install OpenCV from the conda-forge channel and required Python package:
     ```
     mamba install -c conda-forge opencv
     pip install opencv-python
     
     ```

7. **Install PyArrow:** 

   - Please use mamba to install PyArrow since it may not work with conda. 😥
   - Install PyArrow:
     ```
     mamba install pyarrow
     ```

8. **Edit 'dtypes.py' File:** ❗ ❗ ❗ 

   - Open the 'dtypes.py' file and import 'pyarrow' as 'pa':
     ```
     nano /home/anastasia/miniforge3/envs/hw7_mamba/lib/python3.12/site-packages/pandas/core/dtypes/dtypes.py
     ```
     Check your path! It might be different from this one

   - Insert the following line as the second line in the file, right after the first 'from' statement:
     ```python
     import pyarrow as pa
     ```

   - Save and close the file.

9. **Install 'libutf8proc':**

   - Install 'libutf8proc':
     ```
     mamba install libutf8proc
     ```

10. **Install 'libutf8proc2' Using apt-get:**

    - Install 'libutf8proc2' using apt-get:
      ```
      sudo apt-get install libutf8proc2
      ```
 
11. **Edit 'frame.py' File:** ❗ ❗ ❗ 

    - Open the 'frame.py' file and comment out the problematic lines (line 700):
      ```
      nano +700 /home/anastasia/miniforge3/envs/hw7_mamba/lib/python3.12/site-packages/pandas/core/frame.py
      ```
      Check your path! It might be different from this one
    - Comment out the lines as follows:
![image](https://github.com/CaptnClementine/test/assets/131146976/40d30123-065b-4cc7-9874-58aba8c899b7)


    - Save and close the file.


## How to use environment.yml
To create a conda environment using an environment.yml file, use the following command:
```
mamba env create -f environment.yml
```
Afterward, make sure to follow these additional steps carefully. They are marked with ❗ ❗ ❗ for your convenience

That's all! I hope you were able to complete it quickly, and that working with 'pain.py' wasn't too painful for you at all!

## By the way
Good luck!

And don't forget to take some time to rest, as I did this week! 
The best rest is a quality sleep (just like me and python on the picture)
![image](https://github.com/CaptnClementine/test/assets/131146976/ce5e52e6-aeff-426b-a76d-850cc4f08253)

And chill with chinchilla
![image](https://github.com/CaptnClementine/test/assets/131146976/54c96382-0cc8-4b58-859d-ff3f04e74c10)

If you have any questions, suggestions, or encounter any issues while using the amino-analyzer tool, feel free to reach out [CaptnClementine](https://github.com/YourGitHubUsername) 💛
