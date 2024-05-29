# Securing Accounts
we all have so many accounts now days, google, twitter, many many more.. so we look what are some defensive and treath agaist these types of accoutns. to keep these accounts secure.

so let's take this analogy first of all, at home.. we have a door right?? lol.. we lock these dors using our secrete key.. right? so inorder to get in.. we must have that secret keys.. otherwise we will forced to break.. which is what we call "pentration testing" in security... more on later.. but.. this is what we call account in security world.

also remeber.. if someone gets our keys he can also use that key to get into our home.

So in digital world there is waht we call
## Authentication
Authentication or what we call in short term in bug bounty world "Auth" is the process of proving to another person that you are who you say you are. 

It's an important process in modern computer networks, especially when you're sharing sensitive information like your social security number, passwords, or bank account login information. 

Auth is done by using a combination of factors, such as password, biometric data (like fingerprints or iris scans), and multi-factor authentication (such as a code sent to your phone or email). 

So, in short, authentication is the process of verifying your identity to prevent unauthorized access to your account or system.

## Authorization
there is also realted concpet beside auth.. and it is what we call Authorization or AuthZ in short.. so this is the process of give privialdge.. I mean once you authenticated using your password lets.. then the next step is are you normal user? or admin? this is done using what we call Authorization.

So these all done using username and passowrd.. but the thing when we create our user, pass.. we need to make it strong enough so that attackers can't brutforce it.. or use the method what we call "Dictionary attaks"

## Dictionary Attacks
this attack is .. just a collection of words stored on file such us wordlist.txt.. so it will try one by one inorder to guess your password.. so if your password is waek enough and some with one of the listed word inside these file.. boom you get hacked!!

## Brute-Force
this is also kinda the some.. but this is more powerfull.. actuly since modern systems implemented rate limit.. attackers faced lots of challange.. so this method is no longer powerfull i guess so.

Imagine if your mobile phone only required 4 digit to log into it??? 

```python
from string import digits
for i in digits:
    for j in digits:
        for k in digits:
            for l in digits:
                print("Cracking...")
                print(i, j, k, l)
                print("Cracked")
```

this python code will break the phone just in 2 second lol

.. what if it is not passcode.. (passcode is only numbers)? what if is is password? since password contain both letters and ascii?

well the some prinpless still apliyes.. but it takes a bit more time than before.. since letters and numbers are too many.
```python
from string import ascii_letters

for i in ascii_letters:
    for j in ascii_letters:
        for k in ascii_letters:
            for l in ascii_letters:
                print(i, j, k, l)
```

again it is the some with digits and punctuation..
```python
from string import ascii_letters, digits, punctuation

for i in ascii_letters + digits + punctuation:
    for j in ascii_letters + digits + punctuation:
        for k in ascii_letters + digits + punctuation:
            for l in ascii_letters + digits + punctuation:
                print(i, j, k, l)
```

there is too many ways that can be used to protect like 2fa, mfa, otp(sim swapping will break this I guess so) and many more