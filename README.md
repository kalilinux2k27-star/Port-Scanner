#!/bin/python

import sys
import socket
from datetime import datetime

if len(sys.argv)-2:
         target=socket.gethostbyname(sys.argv[1])

else:
     print("invalid amount of argument")

print("-"*50)
print("scanning target "+target)
print("time started"+ str(datetime.now()))
print("-"*50)

try:S
      for port in range(1,50):
               s=socket.socket(socket.AF_INET, socket.SOCK_STREAM)
               socket.setdefaulttimeout(1)
               result=s.connect_ex((target,port))
               print("checking port{] is open".format(port))
               if result == 0:
                        print("Port {) is open" .format(port))
               s.close()
 
except KeyboardInterrupt:
        print("\nexiting program")
        sys.exit()
except socket.gaierror:
        print ("hostname could not be resolved")
        sys.exit()
except socket.error:
        print("couldnt connect to server") 
        sys.exit()
