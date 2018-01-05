# training-classes
training-class

#!/bin/bash

for ip in $(seq 200 ); do
ping -c 1 192.168.31.$ip | grep "bytes from" | cut -d" " -f 4 | cut -d":" -fl &
done
