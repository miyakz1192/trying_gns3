# GNS3を使ってみた

https://www.miraclelinux.com/tech-blog/6lmepn

miyakz@gns3:~$ cat /etc/issue
Ubuntu 22.04.3 LTS \n \l

miyakz@gns3:~$ 
   10  sudo apt install python3-dev
miyakz@gns3:~$ sudo apt install python3-pyqt5
miyakz@gns3:~$ sudo apt install python3-pip


miyakz@gns3:~$ pip3 install gns3-server
Defaulting to user installation because normal site-packages is not writeable
Collecting gns3-server
  Downloading gns3-server-2.2.44.1.tar.gz (11.6 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 11.6/11.6 MB 10.4 MB/s eta 0:00:00
  Preparing metadata (setup.py) ... done
Collecting aiohttp-cors<0.8,>=0.7.0
  Downloading aiohttp_cors-0.7.0-py3-none-any.whl (27 kB)
Collecting async-timeout<4.1,>=4.0.2
  Downloading async_timeout-4.0.3-py3-none-any.whl (5.7 kB)
Collecting distro>=1.8.0
  Downloading distro-1.8.0-py3-none-any.whl (20 kB)
Collecting platformdirs>=2.4.0
  Downloading platformdirs-4.0.0-py3-none-any.whl (17 kB)
Collecting psutil==5.9.6
  Downloading psutil-5.9.6-cp36-abi3-manylinux_2_12_x86_64.manylinux2010_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (283 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 283.6/283.6 KB 5.7 MB/s eta 0:00:00
Collecting py-cpuinfo<10.0,>=9.0.0
  Downloading py_cpuinfo-9.0.0-py3-none-any.whl (22 kB)
Collecting sentry-sdk<1.35,==1.34.0
  Downloading sentry_sdk-1.34.0-py2.py3-none-any.whl (243 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 243.9/243.9 KB 9.3 MB/s eta 0:00:00
Collecting aiohttp<3.9,>=3.8.5
  Downloading aiohttp-3.8.6-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (1.0 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.0/1.0 MB 15.5 MB/s eta 0:00:00
Collecting truststore>=0.8.0
  Downloading truststore-0.8.0-py3-none-any.whl (16 kB)
Collecting Jinja2<3.2,>=3.1.2
  Downloading Jinja2-3.1.2-py3-none-any.whl (133 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 133.1/133.1 KB 3.1 MB/s eta 0:00:00
Collecting aiofiles<23.3,>=23.2.1
  Downloading aiofiles-23.2.1-py3-none-any.whl (15 kB)
Collecting jsonschema<4.18,>=4.17.3
  Downloading jsonschema-4.17.3-py3-none-any.whl (90 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 90.4/90.4 KB 5.0 MB/s eta 0:00:00
Collecting setuptools>=60.8.1
  Downloading setuptools-68.2.2-py3-none-any.whl (807 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 807.9/807.9 KB 21.4 MB/s eta 0:00:00
Requirement already satisfied: certifi in /usr/lib/python3/dist-packages (from sentry-sdk<1.35,==1.34.0->gns3-server) (2020.6.20)
Collecting urllib3>=1.26.11
  Downloading urllib3-2.1.0-py3-none-any.whl (104 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 104.6/104.6 KB 3.6 MB/s eta 0:00:00
Collecting aiosignal>=1.1.2
  Downloading aiosignal-1.3.1-py3-none-any.whl (7.6 kB)
Collecting multidict<7.0,>=4.5
  Downloading multidict-6.0.4-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (114 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 114.5/114.5 KB 4.7 MB/s eta 0:00:00
Collecting frozenlist>=1.1.1
  Downloading frozenlist-1.4.0-cp310-cp310-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (225 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 225.7/225.7 KB 10.3 MB/s eta 0:00:00
Requirement already satisfied: attrs>=17.3.0 in /usr/lib/python3/dist-packages (from aiohttp<3.9,>=3.8.5->gns3-server) (21.2.0)
Collecting charset-normalizer<4.0,>=2.0
  Downloading charset_normalizer-3.3.2-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (142 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 142.1/142.1 KB 6.2 MB/s eta 0:00:00
Collecting yarl<2.0,>=1.0
  Downloading yarl-1.9.2-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (268 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 268.8/268.8 KB 11.3 MB/s eta 0:00:00
Requirement already satisfied: MarkupSafe>=2.0 in /usr/lib/python3/dist-packages (from Jinja2<3.2,>=3.1.2->gns3-server) (2.0.1)
Requirement already satisfied: pyrsistent!=0.17.0,!=0.17.1,!=0.17.2,>=0.14.0 in /usr/lib/python3/dist-packages (from jsonschema<4.18,>=4.17.3->gns3-server) (0.18.1)
Requirement already satisfied: idna>=2.0 in /usr/lib/python3/dist-packages (from yarl<2.0,>=1.0->aiohttp<3.9,>=3.8.5->gns3-server) (3.3)
Building wheels for collected packages: gns3-server
  Building wheel for gns3-server (setup.py) ... done
  Created wheel for gns3-server: filename=gns3_server-2.2.44.1-py3-none-any.whl size=12541544 sha256=5927f11f1280e3fe1ac490f4fa6285fef194cb157ffd6290380be2ef1d4c823a
  Stored in directory: /home/miyakz/.cache/pip/wheels/e2/c2/de/4bc6bc1d68e971ac4ef60ff1b97705c72beef5a12a2019f23d
Successfully built gns3-server
Installing collected packages: py-cpuinfo, urllib3, truststore, setuptools, psutil, platformdirs, multidict, jsonschema, Jinja2, frozenlist, distro, charset-normalizer, async-timeout, aiofiles, yarl, sentry-sdk, aiosignal, aiohttp, aiohttp-cors, gns3-server
  WARNING: The script cpuinfo is installed in '/home/miyakz/.local/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
  WARNING: The script jsonschema is installed in '/home/miyakz/.local/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
  WARNING: The script distro is installed in '/home/miyakz/.local/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
  WARNING: The script normalizer is installed in '/home/miyakz/.local/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
  WARNING: The scripts gns3loopback, gns3server and gns3vmnet are installed in '/home/miyakz/.local/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
Successfully installed Jinja2-3.1.2 aiofiles-23.2.1 aiohttp-3.8.6 aiohttp-cors-0.7.0 aiosignal-1.3.1 async-timeout-4.0.3 charset-normalizer-3.3.2 distro-1.8.0 frozenlist-1.4.0 gns3-server-2.2.44.1 jsonschema-4.17.3 multidict-6.0.4 platformdirs-4.0.0 psutil-5.9.6 py-cpuinfo-9.0.0 sentry-sdk-1.34.0 setuptools-68.2.2 truststore-0.8.0 urllib3-2.1.0 yarl-1.9.2
miyakz@gns3:~$ 

miyakz@gns3:~$ pip3 install gns3-gui 
Defaulting to user installation because normal site-packages is not writeable
Collecting gns3-gui
  Downloading gns3-gui-2.2.44.1.tar.gz (4.9 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 4.9/4.9 MB 17.5 MB/s eta 0:00:00
  Preparing metadata (setup.py) ... done
Requirement already satisfied: sentry-sdk<1.35,==1.34.0 in ./.local/lib/python3.10/site-packages (from gns3-gui) (1.34.0)
Requirement already satisfied: psutil==5.9.6 in ./.local/lib/python3.10/site-packages (from gns3-gui) (5.9.6)
Requirement already satisfied: distro>=1.8.0 in ./.local/lib/python3.10/site-packages (from gns3-gui) (1.8.0)
Requirement already satisfied: truststore>=0.8.0 in ./.local/lib/python3.10/site-packages (from gns3-gui) (0.8.0)
Requirement already satisfied: jsonschema<4.18,>=4.17.3 in ./.local/lib/python3.10/site-packages (from gns3-gui) (4.17.3)
Requirement already satisfied: setuptools>=60.8.1 in ./.local/lib/python3.10/site-packages (from gns3-gui) (68.2.2)
Requirement already satisfied: urllib3>=1.26.11 in ./.local/lib/python3.10/site-packages (from sentry-sdk<1.35,==1.34.0->gns3-gui) (2.1.0)
Requirement already satisfied: certifi in /usr/lib/python3/dist-packages (from sentry-sdk<1.35,==1.34.0->gns3-gui) (2020.6.20)
Requirement already satisfied: pyrsistent!=0.17.0,!=0.17.1,!=0.17.2,>=0.14.0 in /usr/lib/python3/dist-packages (from jsonschema<4.18,>=4.17.3->gns3-gui) (0.18.1)
Requirement already satisfied: attrs>=17.4.0 in /usr/lib/python3/dist-packages (from jsonschema<4.18,>=4.17.3->gns3-gui) (21.2.0)
Building wheels for collected packages: gns3-gui
  Building wheel for gns3-gui (setup.py) ... done
  Created wheel for gns3-gui: filename=gns3_gui-2.2.44.1-py3-none-any.whl size=3716344 sha256=6e9fe19f9eb6227498894f0cb52f079151a123c704628cb092754604566db9f8
  Stored in directory: /home/miyakz/.cache/pip/wheels/2c/14/ab/af54b1cb1a18591d9199762e363f48549ae29570196a4f16b4
Successfully built gns3-gui
Installing collected packages: gns3-gui
Successfully installed gns3-gui-2.2.44.1
miyakz@gns3:~$ 

miyakz@gns3:~$ gns3
Please install the PyQt5.QtSvg module
miyakz@gns3:~$ 

miyakz@gns3:~$ sudo apt install python3-pyqt5.qtsvg 

miyakz@gns3:~$ gns3
Please install the PyQt5.QtWebSockets module
miyakz@gns3:~$ 

miyakz@gns3:~$ sudo apt install python3-pyqt5.qtwebsockets 



