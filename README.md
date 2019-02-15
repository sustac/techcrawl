SearchCrawl

The SearchCrawl repository contains a scrapy webcrawler, a program to convert website links into a graph and view various graph metrics and a mongoDB database to store webcrawler data. This collection allows the utilization
of search queries of the data. This can be used as a personal search engine. 

Has only been tested on Ubuntu 18.04

To start you need to install python3 and then install virtualenv.
sudo apt-get install python3-pip and then pip3 install virtualenv.
After installation move to directory where you want the project to be located and run virtualenv env.
This will create a python virtual envireonment called env.
This is where you will place the techcrawl project files.
A python virtual environment prevents the project's python dependencies from conflicting with the system's.
Before running any executables you need to type the command source bin/activate from the env directory(starts environment).

Then chmod 755 prereq_outside.sh and ./prereq_outside.sh and then ./prereq_inside.sh.
prereq_outside installs the dependencies for mongodb and creates a data folder for it in the root directory(needed).
prereq_inside installs all of the python modules needed.

Once everything has been installed, simply type ./run.sh.

This will display a menu for index, crawl, and graph. You must run index first to create mongoDB collection and index it
to enable text searching. After you have indexed a collection you may run the crawl program. After the crawl you will be
able to search the results or you will be able to see various graph metrics and view a basic visualization of the crawl. This can be constantly done on the same collection or you may create others. The index program allows you to create, index, remove duplicates and completley remove collections. 

You dont have to use run.sh. You can run the programs on the command line.

When done using the project, to deactivate virtual environment just simply type in deactivate in terminal.


Some examples websites to try to see the difference in metrics:

https://www.theguardian.com/us/technology
https://www.slashdot.org
https://www.linuxinsider.com
