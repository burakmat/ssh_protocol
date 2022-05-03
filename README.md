# SSH (Secure Shell)
SSH is a cryptographic network protocol which is used to control a server over an unsecured network.
A client can generate a new ssh key and create a secure connection by providing the key to the server.
## Creating a new SSH key
You can create a new key by typing following command in your terminal:
```
ssh-keygen
```
If there is a no problem with your ssh packages, your computer is going to create a new rsa key pair with a private and a public key.

The output should be like this:
```
Generating public/private rsa key pair.
Enter file in which to save the key (/home/<your_username>/.ssh/id_rsa):
```
Here, [RSA](https://en.wikipedia.org/wiki/RSA_(cryptosystem)) stands for the names of founders, Rivest-Shamir-Adleman, who described the encryption algorithm. This method is used in SSH protocol.

As you can see, after generating the keys, it will ask for a file name to write the keys into. You can just hit enter to use default name which is 'id_rsa'.

Then, you will be asked for a password.
```
Enter passphrase (empty for no passphrase):
```
You can again just hit enter and not give it a password. It doesn't mean that your connection will be unsecure but an extra precaution. This password will be asked while you're trying to make connection using this key.

You should confirm your password.
```
Enter same passphrase again:
```
After you set your password up, you will be informed about that your keys are saved to your computer.
```
Your identification has been saved in /home/<your_username>/.ssh/id_rsa
Your public key has been saved in /home/<your_username>/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:s6N0OwlTDKjDez98kZRwUGZbTYaQUArv+EYC6sigFwA <your_username>@<host_name>
The key's randomart image is:
+---[RSA 2048]----+
|E   ..o=*o.+o    |
|.   .oo+oo...    |
|....  o=..       |
| o+. o  =        |
|o .oo ooS.       |
|* ...+o oo       |
|oo.. o+o+o       |
| .   o+o+o       |
|      .o..       |
+----[SHA256]-----+
```
In addition to this information, you will get the key fingerprint and its randomart image. 

Key fingerprint is a short sequence of bytes used to identify a longer key. It can also be displayed as follows:
```
43:51:43:a1:b5:fc:8b:b7:0a:3a:a9:b1:0f:66:73:a8 <your_username>@<host_name>
```
Since it is not easy for humans to validate this complicated fingerprint, it is better to make it easy to understand by visualizing it. So, key's randomart image simply visualize the fingerprint with a certain manner.

