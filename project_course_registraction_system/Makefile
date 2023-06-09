
all: serverM.cpp serverC.cpp serverCS.cpp serverEE.cpp client.cpp
g++ -o serverM serverM.cpp
g++ -o serverC serverC.cpp
g++ -o serverCS serverCS.cpp
g++ -o serverEE serverEE.cpp
g++ -o client client.cpp

serverM: serverM.o
./serverM

serverC: serverC.o
./serverC

serverCS: serverCS.o
./serverCS

serverEE: serverEE.o
./serverEE

client: client.o
./client


