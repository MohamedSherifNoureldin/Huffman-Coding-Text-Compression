# Huffman Coding Text Compression
A C++ program that compresses text files using the Huffman Coding algorithm. This program was written as a final project for my Data Structures and Algorithms class (CSCE2202). For a detailed report on the project and the Huffman coding algorithm, see the "Report.pdf" file

## Features
- Compress and decompress ASCII text files using Huffman Coding
- Store the Huffman Coding tree in a file for later decompression
- Store both the Huffman Coding tree and the compressed data in a single file to be decompressed later or in a seperate files

## Usage
```bash
./huffman command input_file
```
Command can either be compress_multi or compress_single or decompress_multi or decompress_single. The input_file is the file to be compressed or decompressed. 

### Commands:
- compress_multi: Compresses the input file and stores the compressed data and the Huffman Coding tree in a seperate files. The output file name is the same as the input file name with the new extension ".compressed" and the huffman coding table in a file with the same name and the new extension ".table".
- compress_single: Compresses the input file and stores the compressed data and the Huffman Coding tree in a single file. The output file name is the same as the input file name with the new extension ".single".
- decompress_multi: Decompresses the input file (the .compressed file)and stores the decompressed data in a file. The output file name is the same as the input file name with the new extension ".txt". For this command to correctly work the .table file must be in the same directory as the .compressed file.
- decompress_single: Decompresses the input file and stores the decompressed data in a file. The output file name is the same as the input file name with the new extension ".txt".

### Example:
#### Compressing a file
```bash
./huffman compress_multi input.txt
```
or 
```bash
./huffman compress_single input.txt
```
#### Decompressing a file
```bash
./huffman decompress_multi input.compressed
```
or 
```bash
./huffman decompress_single input.single
```

## Test Cases
In the TestCases Folder there are 2 sample text files that can be used to test the program.
- File1.txt: A short text file with 57 characters
- File2.txt: A long text file with 100,000 characters
