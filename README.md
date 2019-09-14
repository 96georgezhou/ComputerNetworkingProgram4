# ComputerNetworkingProgram4
The purpose of spoofcheck is to let the server running spoofcheck to check the integrity of a client connection by looking for IP Address spoofing.
It performs this integrity check by using DNS to authenticate a client that has established a connection to the server. The spoofcheck implementation references the advertised IP Address against the client's official host name, aliases, and registered IP Address addresses.
A client must only establish a TCP connection with the spoofcheck server as no other protocol is used. After establishing a connection, the spoofcheck server checks if the client is spoofing the IP address or if it is an honest connection, then it immediately ends the connection.
Note that client connections are subject to be reported as spoofing if no DNS mapping exists for a client IPAddress, even if connections are actually authentic. For this reason, spoofcheck is not a sophisticated method of checking for actual IP Address spoofing.
The spoofcheck server will remain running until manually shut down. Multiple connections can be established through threaded operation on the supplied port number while the server is running.
