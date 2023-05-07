Download Link: https://assignmentchef.com/product/solved-operatingsystems-problem-4-address-spaces-in-a-paging-system
<br>



<table width="572">

 <tbody>

  <tr>

   <td width="437"><strong>Problem 4.1: </strong><em>address spaces in a paging system</em></td>

  </tr>

 </tbody>

</table>

Consider a operating system that uses paging for memory management with a page size of 1024 bytes. (The smallest addressable memory unit is a byte consisting of 8 bits.) The logical address space of processes is limited to a maximum of 64 pages. The physical memory has a size of 256 kilobytes.

<ol>

 <li>How many frames has the physical memory?</li>

 <li>How many bits has an address in the logical address space?</li>

 <li>How many bits has an address in the physical address space?</li>

 <li>How many bits are used for the page number?</li>

 <li>How many bits are used for the offset within a page?</li>

</ol>

<strong>Problem 4.2: </strong><em>page replacement algorithms                                                   </em>

An operating system uses demand paging to implement virtual memory. A user-space process uses four pages, numbered 1 to 4. The pages are accessed in the following order (reference string): 1, 2, 3, 4, 1, 1, 4, 2, 1, 2. None of the pages used by the user-space process are resident when the process starts and the frames allocated to the process are unused. Fill out the following tables by writing page numbers into the cells. Each number indicates which page a frame holds after accessing the page indicated by the reference string. Write down the number of page faults for each scenario.

Hint: Do not move pages between frames except when necessary.

<ol>

 <li>Show how the pages are mapped to two frames using the First-In-First-Out (FIFO) page replacement algorithm.</li>

 <li>Show how the pages are mapped to three frames using the First-In-First-Out (FIFO) page replacement algorithm.</li>

</ol>

reference string       1     2      3     4     1      1     4     2      1     2

frame 0

<table width="233">

 <tbody>

  <tr>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

  </tr>

  <tr>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

  </tr>

  <tr>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

  </tr>

 </tbody>

</table>

frame 1

frame 2

<ol>

 <li>Show how the pages are mapped to two frames using Belady’s Optimal (BO) page replacement algorithm.</li>

 <li>Show how the pages are mapped to three frames using Belady’s Optimal (BO) page replacement algorithm.</li>

</ol>

reference string       1     2      3     4     1      1     4     2      1     2

frame 0

<table width="233">

 <tbody>

  <tr>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

  </tr>

  <tr>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

  </tr>

  <tr>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

  </tr>

 </tbody>

</table>

frame 1

frame 2

<ol>

 <li>Show how the pages are mapped to two frames using the Least Recently Used (LRU) page replacement algorithm.</li>

 <li>Show how the pages are mapped to three frames using the Least Recently Used (LRU) page</li>

</ol>

replacement algorithm.

reference string       1     2      3     4     1      1     4     2      1     2

<table width="233">

 <tbody>

  <tr>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

  </tr>

  <tr>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

  </tr>

  <tr>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

   <td width="23"> </td>

  </tr>

 </tbody>

</table>

frame 0 frame 1 frame 2

<strong>Problem 4.3: </strong><em>working set vs least recently used                                                                                  </em>

Consider the design of a paging system that tracks the working set of all processes and aims at keeping the working sets of the processes resident. If pages are removed from the working set of a process, then these pages are removed from the resident set of pages and the frames get marked as unused. In other words, only pages that are part of the working set are resident, all other pages are not.

Assume the working set is calculated over the last <em>N </em>memory accesses for every process. Compare this system with a system that uses the least recently used (LRU) page replacement strategy for each process with <em>N </em>pages allocated to each process. What can you say about the pages that are resident in both systems at any point in time?

Which system do you think is preferable? Can you suggest further improvements?