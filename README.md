# girthy
might be slim but a lot goes through

### Step-by-step Instructions for Running the GPU-accelerated SHA-256 Hashing Script ###

1. **Setup**:
   - Ensure you have the NVIDIA drivers and CUDA toolkit (version 12.0.1 or compatible) installed on your Ubuntu 20.04 machine.
   - Ensure you have Python 3.x installed.

2. **Extract the ZIP Archive**:
   - Extract the provided ZIP archive to a directory of your choice.

3. **Replace CSV Files**:
   - Substitute `input.csv` and `compare.csv` in the extracted directory with your own CSV files.

4. **Compile the CUDA Code**:
   - Open a terminal and navigate to the directory containing the extracted files.
   - Run the following command to compile the CUDA code:
     ```bash
     ./compile_cuda.sh
     ```
   - This will produce a shared library named `sha256.so` which contains the compiled CUDA functions.

5. **Run the Python Script**:
   - In the terminal, execute the following command:
     ```bash
     python3 optimized_cuda_script.py
     ```
   - This will start processing the data from `input.csv`, perform GPU-accelerated SHA-256 hashing, and compare the results with the entries in `compare.csv`.
   - Any matches found will be printed to the terminal.

Note: The provided CUDA and Python scripts have placeholders for the GPU-accelerated SHA-256 hashing. Once you have the complete CUDA hashing implementation, you can replace the placeholders in `sha256.cu` and recompile.


