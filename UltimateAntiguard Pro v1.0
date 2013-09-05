#!/usr/python
#This is the basic console program developed in python ,
#Ultimate antiguard is a greate to tool to remove one type of purticular virus ,
#this virus is execute/spread when we double click on the 'foldername.link' file , 
#so our tool will remove the all .link folder available in the usb drive and it also delete the 'autorun files, 
#it set the folder attributes such as +H +s to all folder ,it realy makes all folder in unhide mode. 


import os
def space_adjust(n):
   print ""
   print ""
   print ""
space_adjust(5)
print "         ULTIMATE ANTIGUARD PRO v1.0"
print "    *************************************"
print ""

#function to choose the drive( here imagine the folders "/home/rakesh/.." as several drives) .

def choose_drive(n):
   print "Choose the drive[create the following folders in home directory]  that you want to clean "
   print "    Menu"
   print "   -------"
   print "     1   -> /home/rakesh/folder1/trial/"
   print "     2   -> /home/rakesh/Documents/trial/"
   print "     3   -> /home/rakesh/folder3/trial/ "
   print "     4   -> /home/rakesh/Desktop/trial/"
   print "     5   -> /home/rakesh/folder4/trial/"
   space_adjust(1)
   #drive letter user input
   opt = input("      Enter option (1-5) DRIVE=> : ")
   
   if opt==1:
# change the drive address manually before executing (edit the path according to the directory available in your linux ,then copy the trial folder in different folders), linux not support the drive letter such as 'C://'  linux support '/media/some drive address'
      drive="/home/rakesh/folder1/trial/" 
      scan_files(drive)
   elif opt==2:
# change the drive address manually
      drive="/home/rakesh/Documents/trial/"
      scan_files(drive)
   elif opt==3:	 
# change the drive address manually 
      drive="/home/rakesh/folder3/trial/"
      scan_files(drive)
   elif opt==4:	 
# change the drive address manually
      drive="/home/rakesh/Desktop//trial/"
      scan_files(drive)
   elif opt==5:	 
# change the drive address manually
      drive="/home/rakesh/folder4//trial/"
#calling scan_files() function to retreive .link files
      scan_files(drive)
   else: 
      print "Invalid entry "
      print "-------[ *  thanks for using UAG PRO V1.0  *]------ "
      print "__________________exit_________________"
#end of choose_drive()



#function to retreive the shortcut folders and the Super hidden files 
def scan_files(rtrv_drive):
   space_adjust(1)
   print "----------------scaning and deletion started-----------------"  
   #code to list out folders and it finding out the shortcut files 
   try:
      #list out the .lnk files available
      import glob
      import os
      os.chdir(rtrv_drive)
      counter=0
      for files in glob.glob("*.lnk"):
         os.remove(files)
         counter=counter+1
         print counter,") ",files," = > Deleted"
   except:
      print "just check the path variable entered in the program"
   print "_______________scaning and deletion completed________________"  
   #For unhide the folder super_attribute_set()
   super_attribute_set(rtrv_drive)
#end of scan_files()

#function to set the attribute +s +h
def super_attribute_set(attr_path):
   space_adjust(1)
   print "----------------Retrievel of files started--------------------"
   import glob,os
   os.chdir(attr_path)
   counter=0
   for filename in os.listdir("."):
      if filename.startswith("."):
         counter=counter+1
         os.chdir(attr_path)
         os.rename(filename,filename[1:])
         print counter,")", filename," = > Retrieved "
   print "_______________Retrievel of files completed___________________ "
   space_adjust(1)
   delete_autorun(attr_path)
#end of super_attribute_set()

#function to delete the shortcut folder 'calling from inside of the scan_files()
def delete_autorun(delfolder):
   space_adjust(1)
   print "----------------Autorun scanning started ---------------------"
   try:
      #list out the .lnk files available
      import glob
      import os
      os.chdir(delfolder)
      counter=0
      for files in glob.glob("*.inf"):
         os.remove(files)
         counter=counter+1
         print counter,") ",files," = > Deleted"
      print "_______________Autorun scanning completed_____________________"
      print ""
      print "Drive is safe for use"
      print "thanks for using UAG PRO V1.0"
   except:
      print "No autorun.inf  Detected"
      print "Drive is safe for use"
      print "-------[ *  thanks for using UAG PRO V1.0  *]------ "
   
#end of delete_links()

choose_drive(1)




	




