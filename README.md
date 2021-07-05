

# LFI Suite

![alt tag](https://github.com/D35m0nd142/LFISuite/blob/master/screen.png)

<h3> What is LFI Suite? </h3>

LFI Suite is a totally <b>automatic</b> tool able to scan and exploit Local File Inclusion vulnerabilities using many different methods of attack, listed in the section `Features`.

* * * 
Now a days we are facing a big problem that is,when we try to user lfisuit tool in our kali machine(version 2020 or 2021) we can see "ImportError: no module named termcolor".That why we can't use this tool in our kali machine.I will give yo some soluation for that.

step 1:Check your python version>>python --version(not python3 --version) or also you can check how many version of python do you have in your kali machine for that you can execute these command>>cd /usr/lib <br>then>>ls | grep -i python

Now you can see how many version of python do you have in your kali machine.

step 2:If you have Python 2 and 3 installed, specify it, as pip works for Python2, and pip3 works for Python 3:>>>>>>>>>>pip3 install termcolor

step 3:If you have only Python3, or in simple words only one version of Python You will execute the command>>pip install termcolor

step 4:if step 2 and step 3 falied for you,this is the final step and I think it will work 100%.if you already have termcolor installed to Python3.x(means 3.1,3.2,3.3....). Simply just copy the termcolor.py file from /usr/lib/python3/dist-packages to /usr/lib/python2.x(means 2.1,2.2,2.3...check step 1)

Example:For my cases,step 1:python --version <br>
                            Python 2.7.18

                  step 2:pip3 install termcolor
                  Requirement already satisfied
                  
                  step 3:Now qualified,because i have installed python version 2.7.18 and Python 3.9.2
                  
                  step 4:sudo cp /usr/lib/python3/dist-packages/termcolor.py /usr/lib/python2.7
Then run the command >>python lfisuite.py I think your problem is solved.
