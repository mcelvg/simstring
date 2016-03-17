#
#       SWIG make file for OSX
#

all:
	/usr/local/bin/g++-4.2 -arch i386 -arch x86_64 -fPIC -c export.cpp -I/System/Library/Frameworks/JavaVM.framework/Versions/Current/Headers
	/usr/local/bin/g++-4.2 -arch i386 -arch x86_64 -fPIC -c export_wrap.cpp -I/System/Library/Frameworks/JavaVM.framework/Versions/Current/Headers
	/usr/local/bin/g++-4.2 -arch i386 -arch x86_64 -dynamiclib export.o export_wrap.o -o libSimString.dylib -liconv -L/usr/include

sample:
	javac simstring/*.java
	javac Sample.java

clean:
	rm -rf *.o *.dylib *.cpp *.class export.* simstring

purge:
	rm -rf *.o *.dylib *.cpp export.* simstring
