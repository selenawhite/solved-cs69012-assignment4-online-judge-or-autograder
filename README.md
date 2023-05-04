Download Link: https://assignmentchef.com/product/solved-cs69012-assignment4-online-judge-or-autograder
<br>
<strong>Online Judge​</strong> – It will take codes , compile it, check for compilation errors, execute your code by providing some secret inputs and collect your code’s output, check for runtime errors, and finally match your output with its hidden test outputs.

In this assignment you need to implement file transfer protocol on top of TCP sockets and you will implement a console based Online Judge. There will be a server and multiple clients communicating with the server. Each client process will open a new connection with the server. Use select to handle multiple client requests.

Each client can send a c/c++ file to the server through CODEJUD command and the server will reply to the client whether the given code is successful or giving error at any point of time during execution of code. If execution is successful then the server will also check and reply to the client about the acceptance of the c/c++ file.

<h1>Problem :-</h1>

<ul>

 <li>Write two separate C programs one for TCP server (handles requests from multiple servers) and one for client.</li>

 <li>Multiple clients should be simultaneously able to communicate with the server.</li>

 <li>Server accepts connections from clients.</li>

 <li>Server receives control information like FTP commands over this connection.</li>

 <li>Server checks for valid commands, and executes them if there is no error.</li>

 <li>In order to transfer files etc. you can use ftp. And you can reuse your previous ftp setup. – Handle corner cases.</li>

</ul>




In Addition of previous ftp commands (RETR, STOR etc.) From assignment number 3.

You have to implement and design the CODEJUD command.

“CODEJUD” – This command will take a c/c++ file from client and server will compile , execute and match the output with given test cases and will notify back to client about any error or correctness of c/c++ file.




<strong>Working of server and client is as follows:- </strong>

*After successful connection-

<h1>Three features to be added at server side- (CODEJUD​ )​</h1>

<ol>

 <li><strong>Compilation Phase – </strong>This phase ​ will take a String that contains the source code and​      coding language (c/c++).This is the file client wants to test. This phase will compile the input and send compilation error messages to clients if any. Else it will create an o​bject file and send a compilation success message to the client.</li>

 <li><strong>Execution Phase​</strong> – This phase will take object file , time Limit(1sec). This phase will execute your code by providing some secret inputs if required. This phase will decide if the input file has any error (TLE or Runtime error). If it succeeds then it will create a new output.txt file and send an execution success message to the client.</li>

</ol>




<ol start="3">

 <li><strong>Matching Phase​</strong> – This phase will compare Correct testcase.txt file with the actual output.txt file, if it is matched then the successful message will be passed to client, else the wrong output message will be passed to client.</li>

</ol>




<strong>Your final program will able to perform these ftp commands -: </strong>

<ol>

 <li>RETR &lt;filename&gt;</li>

 <li>STOR &lt;filename&gt;</li>

 <li>LIST</li>

 <li>ABOR (Optional).</li>

 <li>QUIT</li>

 <li>DELE &lt;filename&gt;</li>

 <li><strong>​</strong>CODEJUD &lt;filename&gt; &lt;ext(c/c++)&gt;</li>

</ol>


