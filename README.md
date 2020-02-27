Mytget
======================

Mytget is a muti-thread downloader accelerator for GNU/Linux.

It forks from http://myget.sourceforge.net/

Current Features
------------

* Supports HTTP, HTTPS, FTP protocols
* Supports HTTP-GET proxy
* Resumes the aborted downloads
* Supports directory download
* Can accelerates downloading through using muti-connections
* Supports large file( > 4G )


Install in Linux/Mac OS
------------

Install the necessary compile dependencies:

Archlinux:

    sudo yaourt -Syu myget
    
CentOS:

	sudo yum install git cmake gcc-c++ openssl-devel -y	

Ubuntu:

	sudo apt-get install git cmake g++ libssl-dev -y

macOS:

	brew install openssl

fixed it on macOS when cmake：

	cmake -DOPENSSL_ROOT_DIR=/usr/local/opt/openssl -DOPENSSL_LIBRARIES=/usr/local/opt/openssl/lib

Make sure your cmake version >= 2.6
	
	git clone https://github.com/lytsing/Mytget.git
	cd Mytget/
	cmake .
	make && sudo make install


Usage
------------

	$ mytget -h
	Mytget 1.12: A download accelerator for GNU/Linux
	Usage: mytget [options]... [URL]...
	Options:
	  -A,  --user-agent=UA  Set the user agent [UA]
	  -b,  --debug          Show the debug message
	  -c,  --count=num      Set the retry count to [num], no limit when "0", the default is "99"
	  -d,  --directory=dir  Set the local direcotry to [dir], the default is "."
	  -f,  --file=file      Rename the file to [file]
	  -H,  --host=host      Modify `Host: [host]' header in HTTP request.
	  -h,  --help           A brief summary of all the options
	  -i,  --interval=num   Set the ftp retry interval to [num] seconds, the default is "5"
	  -n,  --number=num     Use [num] connections instead of the default (4)
	  -r,  --referer=URL    Include `Referer: [URL]' header in HTTP request.
	  -t,  --timeout=num    Set the connection timeout to [num] seconds, the default is "30"
	  -v,  --version        Show the version of the myget and exit
	  -x,  --proxy=URL      Set the proxy [URL]
