a. Siting Lu

b. 8532084591

c. What I have done in the assignment?
1. Accomplished all the functions of the course registration system except the optional part.
2. Built the client.cpp, serverM.cpp, serverC.cpp, serrverCS.cpp, serverEE.cpp in order to implement the function of the main server, Credential server, EE
Department server, CS Department server and Client.
3. Built TCP and UDP connection between client and servers, made the backend server read and store the files, encrypt the information follow the rules, compare the information, etc.
4. Well-defined data format, and accomplished the TCP and UDP message exchange.

d.What my code files are and what each one of them does?

client.cpp: 1 TCP socket is created in this file. The client getinformation from user's inputs and send it to Main Server, then wait for answer from Main Server.
serverM.cpp: 1 UDP socket and 1 TCP socket was created in this file. The TCP socket is responsible for connecting with client, get the input and send the result back to client. The UDP socket is responsible for connecting with backend-servers to get information.
serverC.cpp: 1 UDP socket was created, which is responsible for connnecting with Main Server, and the file include a function for encrypting the information follow the rules.
serverCS.cpp: 1 UDP socket is created in this file. The backend-serverCS read file and compare the information of file and input information, then send back result to Main Server.
serverEE.cpp: 1 UDP socket is created in this file. The backend-serverEE read file and compare the information of file and input information, then send back result to Main Server.

e. The format of all the message exchanged

In client.cpp:   user_info: string username; string password; query_info: string course; string query_item; char recv_user_info_buf[BUFSIZE]: "0"/"1"
In serverM.cpp:        string course; string category; char* username; char buf[MAXBUFSIZE]
In serverC.cpp:         char verify_result[1]
In serverCS.cpp   string course; string category; string result;
In serverEE.cpp string course; string category; string result;

f. Idiosyncrasy of my project
abnormal interruption of the server process may cause the socket continue occupying the port. Thus the server is not available until the zombie process is killed.

g. Reused Code
I use sample code from "Beej's Guide to Network Programming" as template. The copy part of his code is commentted in the code file.
