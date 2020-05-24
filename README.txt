DATA COMPRESSOR USING ZLIB LIBRARY
Author: Vivian Liu


This project uses zlib.h (from the zlib library) to create a simple compressor/decompressor which takes a filename and mode (comp/decomp) as arguments and compress/decompresses the given file.


To run my program, follow these instructions:

1. Clone the zlib GitHub repository. Link:
	https://github.com/madler/zlib

2. Clone my Data-Compression-Zlib Github repository. Link:
	https://github.com/vliu5163/Data-Compression-Zlib

3. In terminal, navigate to the directory with the zlib repo.

4. Replace the Makefile in zlib repo with the Makefile in Data-Compression-Zlib.

5. Place zlib_compressor.c from Data-Compression-Zlib into the "examples" folder in the zlib repo.

6. Take tester.txt and dork.jpg and from Data-Compression-Zlib and place into zlib folder (I used those for testing).

3. In zlib directory, type: 
	make test
   This will make the files in the folder according to MAKEFILE and build the library.

4. If you would like to include files to test, add them into the folder. I have included two files that I used to test (test.txt and dork.jpg)

5. You are now ready to run zlib_compress.c. To compress a file, type:
	./zlib_compress filename comp
   To decompress a file, type:
	./zlib_compress filename decomp
	

My main challenge in this project was figuring out how zlib worked—it's a pretty big library. I spent the first few days reading a lot of the documentation and online resources regarding zlib. A secondary challenge was detangling the Makefile and understanding how the different files in the directory fit together. In retrospect, I should have started with reading the code since I found that zpipe.c (given in library) provided much of the code needed to complete zlib_compressor.c. In addition, I made slight modifications to the Makefile to run zlib_compressor.c. However, I now have a deeper understanding of one of the seminal works in data compression! 


This was a really fun project to work on! Thanks to Jean-loup Gailly Mark Adler for providing the open source zlib library. Special thanks to Nicolas Dupont and Alexandre Helle for assigning this unique project. 


Online sources that I found very useful to understand zlib (and C in general):
- https://www.euccas.me/zlib/
- https://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/
- https://zlib.net/zlib_how.html
- https://towardsdatascience.com/how-data-compression-works-exploring-lz77-3a2c2e06c097
- https://cs.stanford.edu/people/eroberts/courses/soco/projects/data-compression/lossless/lz77/index.htm
