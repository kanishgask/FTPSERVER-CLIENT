# FTPSERVER-CLIENT
# File Transfer Application using TCP Sockets in Java

## 📌 Project Overview

A simple Java-based file transfer application that demonstrates how to send a text file from a server to a client over a TCP socket connection. The client requests a filename, the server reads that file (if it exists) and streams its contents line-by-line, and the client writes the received data into a new local file.

---

## 🎯 Aim

To implement a file transfer application using TCP sockets in Java, where the server sends a file’s contents to the client upon request.

---

## 🔁 Algorithm

### FTP Server
1. Start the program.  
2. Import `java.io.*` and `java.net.*`.  
3. Create a `ServerSocket` on port 1024.  
4. Wait for and accept a client connection (`accept()`).  
5. Read the desired filename from the console.  
6. If the file exists, open it with a `BufferedReader` and send each line to the client via a `PrintStream`.  
7. Close streams and socket.

### FTP Client
1. Start the program.  
2. Import `java.io.*` and `java.net.*`.  
3. Obtain the server address (`InetAddress.getLocalHost()`) and connect via a `Socket` on port 1024.  
4. Read the local filename to save as from the console.  
5. Read incoming lines from the server via a `BufferedReader` and write them to the new file with a `PrintWriter`.  
6. Close streams and socket.

---

## 📂 Project Files

- `FTPServer.java` – Server-side code that streams file contents.  
- `FTPClient.java` – Client-side code that receives and saves file contents.  
- `README.md` – This documentation.

---

## 💻 How to Compile & Run

1. **Compile** both classes:
   ```bash
   javac FTPServer.java
   javac FTPClient.java

**   OUTPUT:**

   ServerSocket generated on port 1024...
Client connected: /127.0.0.1
Enter a file name to send: sample.txt
File transfer complete.
Connected to server: 127.0.0.1
Enter a new file name to save received data: received_sample.txt
File received and saved as: received_sample.txt

