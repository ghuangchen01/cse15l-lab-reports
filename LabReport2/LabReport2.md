<p>By Guan Hao Huang Chen</p>
<b>Part 1:</b>
<p>My codes:</p>

![Image](StringServer.png)


<br/>
<p>ScreenShot 1:</p>
![Image](hello.png)
<b>Which methods in your code are called?</b>
<p>When I make a request to the local host url, I call the method Server.start(port, new Handler()) which is handleRequest(URI url) in my Handler class.</p>
<b>What are the relevant arguments to those methods, and the values of any relevant fields of the class?</b>
<p>For the handlerRequest(URI url) method, the argument URI represents the link "http://localhost:2048/add-message?s=hello". The relevant fields of the Handler class would be String st which is set to be " " and int num which is set to 1.</p>
<b>How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.</b>
<p>The given request url path is with /add-message with query s=hello. The code first check if the path is / and it is not so it go to else. The code checks if the path contains /add-messageand it does. So the code proceeds inside this block and splits the query using = sign, and safe result into array parameters with value {"s", "hello"}. It checks if parameters[0] = "s", and it does, so parameters[1] would update to String st which now st is "1. hello\n" and num increases to 2 for the next term needed.</p>

<br/>
<p>ScreenShot 2:</p>
![Image](world.png)
<b>Which methods in your code are called?</b>
<p>When I make a request to the local host url, I call the method Server.start(port, new Handler()) which is handleRequest(URI url) in my Handler class.</p>
<b>What are the relevant arguments to those methods, and the values of any relevant fields of the class?</b>
<p>For the handlerRequest(URI url) method, the argument URI represents the link "http://localhost:2048/add-message?s=world". The relevant fields of the Handler class would be String st which is having the value of "1. hello\n" which is set before and int num that is increamented to 2.</p>
<b>How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.</b>
<p>The given request url path is with /add-message with query s=world. The code first check if the path is / and it is not so it go to else. The code checks if the path contains /add-messageand it does. So the code proceeds inside this block and splits the query using = sign, and safe result into array parameters with value {"s", "world"}. It checks if parameters[0] = "s", and it does, so parameters[1] would update to String st which now st is "1. hello\n2. world\n" and num increases to 3 for the next term needed.</p>
<b>Part 2:</b>
<b>Private key:</b>
<br/>
![Image](private.png)
<br/>
<b>Public key:</b>
<br/>
![Image](public.png)
<br/>
<b>Login to ieng6 without password</b>
<br/>
![Image](ieng6.png)
<br/>
<b>Part 3:</b>
<p>I think from the lab in week 2 and 3, I learn about ieng6 which is really interesting to me. I haven't seen anything like this before, and from these labs I figure out how important it is to know how to use the command lines and terminal.</p>
