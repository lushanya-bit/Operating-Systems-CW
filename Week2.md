# Week 2 - Security Planning and Testing Methodology

## Overview
The activities completed in this lab were based on the week 5 lab and provied experience with using pipes,FIFOs and communication through files. This explores the communication mechanisms within the environment.

## Pipes and Redirection
Pipes and redirection allow processes to communicate by passing the ouptut of one command directly to the other, and reducing the need for intermediate files [4].

### Standard Output and Redirection
Standard output redirection was demonstrated using:

echo "Hello World" > output.txt
echo "Second line" >> output.txt
cat output.txt

It was tested using:
ls /nonexistent 2> error.txt

These techniques are used mainly for logging and error handling in Linux systems [8].

## Using Pipes
The screenshot below demonstrates
