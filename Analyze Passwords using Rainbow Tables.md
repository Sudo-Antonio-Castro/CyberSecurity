# Analyze Passwords using Rainbow Tables

In this video, we will use the Terminal to Analyze Passwords using a Rainbow Table.



https://github.com/user-attachments/assets/1c650077-e9aa-475f-b28a-59b6733a0161



## Password Requirements:
1. Eight or more characters in length.
2. Must include at least one upper and lower case letter.
3. Must have one special character.
4. All passwords are encrypted using md5 or sha1.
5. *We are using **/usr/share/rainbowcrack/charset.txt** to determine which charset to use*.

## Questions
1. Which charset supports the password requirements?
2. What is the password for hash **202cb962ac59075b964b07152d234b70**?
3. What is the password for hash **400238780e6c41f8f790161e6ed4df3b**?
4. What is the password for hash **89BF04763BF91C9EE2DDBE23D7B5C730BDD41FF2**?
5. Which of the passwords fail to meet our requirements?

### Walkthrough

1. Open **Terminal**.
2. Use **cat /usr/share/rainbowcrack/charset.txt** to view the **Charset.txt** file.
3. Use **rtgen md5 ascii-32-95 1 20 0 1000 1000 0** to create an md5 rainbow crack table.
4. Use **rtgen sha1 ascii-32-95 1 20 0 1000 1000 0** to create an sha1 rainbow crack table.
5. Use **rtsort .** to sort the rainbow tables.
6. Use **rcrack . -l /root/captured_hashes.txt** to view passwords.

**Commands**

[**cat**](https://phoenixnap.com/kb/linux-cat-command)
: command in Linux displays file contents.

[**rtgen**](http://www.cs.csi.cuny.edu/~zhangx/papers/P_2018_Sarnoff_McMahon_Zhang.pdf)
: Generates table.

[**rtsort**](http://www.cs.csi.cuny.edu/~zhangx/papers/P_2018_Sarnoff_McMahon_Zhang.pdf)
: Sorts table.

[**rcrack**](http://www.cs.csi.cuny.edu/~zhangx/papers/P_2018_Sarnoff_McMahon_Zhang.pdf)
: Runs a comparison between extracted password hashes and rainbow tables.

[**1 20 0 1000 1000 0**](http://project-rainbowcrack.com/generate.htm):
1. plaintext_len_min = **1** *Limits the plaintext length range of the rainbow table*.
2. plaintext_len_max = **20** *Limits the plaintext length range of the rainbow table*.
3. table_index = **0** *Selects the reduction function*
4. chain_len = **1000** *Rainbow chain length, longer chain stores more plaintexts and requires longer time to generate*
5. chain_num = **1000** *Rainbow chains to generate*
6. part_index = **0** *To store a large rainbow table in many smaller files, use different number in this parameter for each part and keep all other parameters identical*
