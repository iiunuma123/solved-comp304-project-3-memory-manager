Download Link: https://assignmentchef.com/product/solved-comp304-project-3-memory-manager
<br>
In this project, you will get more familiar with the concepts of virtual memory.

<h2>Part I</h2>

In this part, you will implement a virtual memory manager similar to the one described in Programming Projects in page 447 in Chapter 9 in 9<em><sup>th </sup></em>edition of the book (in Page 458 in Chapter 9 in the online version of the book, also provided on Blackboard).

The first version of the memory manager will be implemented with the assumption that physical address space is the same size as the virtual address space. Therefore you will not implement any page-replacement policy. You are given the base source code for the virtual memory manager in the ”virtmem.c” file and you will complete its implementation by filling in the missing parts marked by <strong>TODO </strong>comments.

The virtual memory manager will use a TLB (Translation Lookaside Buffer) and a page table. You are required to use a FIFO replacement policy for the TLB. Differently from the specification in Programming Projects, you will use 20 bits addresses instead of 16 bits. The address bits will be divided into a 10-bit page number and a 10-bit page offset, which are also specified in ”virtmem.c”. In order to test your implementations, ”addresses.txt” and ”BACKING STORE.bin” files are provided in the project folder.

<h2>Part II</h2>

The implementation in Part I assumes that physical memory is the same size as the virtual address space. In practice, physical memory (PM) is typically smaller than virtual memory (VM). Part II will implement the case when VM is larger than PM.

1

COMP 304 ( Spring 2021): Project 3 Virtual Memory Manager         <em>DELIVERABLES</em>

Your implementation for Part II will use 256 page frames rather than 1024 for physical memory. This change will require modifying the provided program so that it keeps track of free page frames as well as implementing a page-replacement policy. We are asking you to implement both FIFO and LRU replacement policies. Add a command line argument to select a policy such as -p 0 for FIFO and -p 1 for LRU.

Compare these two policies with the address streams provided in the project folder.