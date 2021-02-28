import os
import datetime
import shutil

x = datetime.datetime.now()

# define the name of the directory to be created
dirName = 'C:\\Users\\Revathee Sabapathee\\Desktop\\anglo african\\PROJECT REVATHEE\\absa\\MI\\developMI\\MI\\'+ x.strftime('%m%Y')

try:
    # Create target Directory
    os.mkdir(dirName)
    print("Directory " , dirName ,  " Created ") 
except FileExistsError:
    print("Directory " , dirName ,  " already exists")

directoryMI = 'C:\\Users\\Revathee Sabapathee\\Desktop\\anglo african\\PROJECT REVATHEE\\absa\\MI\\developMI\\MI files'
for filename in os.listdir(directoryMI):
    if filename.endswith(".xlsx") or filename.endswith(".xls") or filename.endswith(".xlsb"):
        #Copy a file to other Directory
        shutil.copy(os.path.join(directoryMI, filename), dirName)
    
