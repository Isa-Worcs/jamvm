# jamvm

JamVM is an open-source Java Virtual Machine and the last official release of jamvm is 2.0.0 released on 30th July 2014.

A few modifications are needed for it to be compatible with the latest
Amazon Corretto Java8, as of June 2025.

To achieve the best memory footprint, I have tested it out on linux x86 (32-bit) and its start-up performance is also significantly better.

32 bit applications run well on linux x86\_64, and are useful for those with
limited memory.
Naturally, it is necessary to install any missing 32-bit libraries. Most
linux distributions include tyhem in their repositories.

Configure with: ./configure --build=i386-unknown-linux-gnu --with-java-runtime-library=openjdk8 CFLAGS='-m32 -O2'

and then 'make'.

Simply replace the libjvm.so in the corretto jre, with the jamvm version
(found in src.libs/libjvm.so)

That's it !
