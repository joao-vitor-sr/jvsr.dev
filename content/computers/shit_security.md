+++
title = "Your security is a shit"
date = 2023-04-01
+++

Password generators, 2FA...

## Introduction
Hello, are you a beginner in programming, or already work with tech?
do you use the same password for everything? do you save the password in a text
file on your google drive? do you download cheats for your games? Do you
receive the authentication code by SMS?

Well, today, we will see why you're doing EVERYTHING wrong. This post describes
general security.

No matter what, you NEVER will be 100% secure

## Basics

One thing that everyone mistakes are the famous recommendations to use strong
and different passwords for every single website. Remember, strong passwords
mean using the maximum number of possible characters, including upper case
letters, lower case letters, symbols, and numbers, with a minimum of 12 chars.
The target is to fill in the password field until the maximum of the website.
Websites that only allow ridiculous sizes, such as 8 or 12. Those websites were
built by idiots and beginners that know *nothing* about security

It's easy to break a password, it's not inconvenient, and the usual thing that
many say is, that no one knows you, why someone would try to break my passwords?

Everyone indeed thinks that no one knows you. Since you're meaningless, no one
follows you on social media, and no one will try to break your accounts.
Hundreds of websites have their security broken. In January 2022, an intern
account on Twitter exposed a massive list of emails and phone numbers. Do you
have an account on Twitter now your email it's on the database of people that
try to break accounts.

And that is not everything, there's this website called "Have I been Pwned",
that documents an accident like this the Twitter, and only on their database,
there're more than 600 websites whose security was broken, and more than 11 a
billion accounts were broken. Yes, your email and possibly the hash of your
passwords, are already naked, and at this moment robots are trying to access
one of your accounts

## How passwords are stored

Passwords *shouldn't* be stored directly on a database, in any kind of
system/website, before being stored a hash function should be applied

### What's a hash function

In simple terms, a hash function is a function, that transforms any string in a
string with a specific length, a little more formally:

```
A hash function is any function that can be used to map data of arbitrary size
to fixed-size values
```

Through time many implementations were applied such as

1. [ md5 ](https://en.wikipedia.org/wiki/MD5)
2. [ sha-256 ](https://en.wikipedia.org/wiki/SHA-2)
3. [ GOST ](https://en.wikipedia.org/wiki/GOST_(hash_function))

And much more, but there's a problem, those functions were not built for a
password, where security is essential, those functions were made to be executed
in a fast manner. But on security especially on passwords we don't need to
execute fast, we need a hash function that's slow to execute to difficult the
life of a hacker.

So on passwords "normal hash functions", are not applied, on those scenarios,
the recommendation is to use a [Password
Hashing](https://www.okta.com/blog/2019/03/what-are-salted-passwords-and-password-hashing/)
the hashes of this type are not built to be executed in a fast manner, a small
list is:

1. [bcrypt](https://en.wikipedia.org/wiki/Bcrypt)
2. [PBKDF2](https://en.wikipedia.org/wiki/PBKDF2)
3. [argon 2](https://en.wikipedia.org/wiki/Argon2)

Normal hashes function such as md5, or sha-256 are useful to rapidly apply the
hash on a PDF or to compare a downloaded file with the version that's on the
server.

When a hacker tries to break a password, the application used must generate
many passwords and apply those functions on a hash function to compare with the
database leaked, with a fast hash function, this process becomes fast but with
password hashes, the process slows down.

### Salt

Salt is a random number concatenated with the password (before the hash), the
reason is to not have equal hashes even when the password is equal, think, of a
hacker discovering the password of the following hash

```
2+xom2k
```
(this is not a valid hash, it's just an example), automatically he gets access
to the accounts of everyone that has the same password, but with a salt (a
random number), even if the passwords are equal, the hash will not be. The salt
is stored in a column on the database

### Hackers are not dumb

Remember hackers (mostly), are not dumb, so they know that a well-built
website/system will use bcrypt, and they also know that it's slow to generate a
hash of bcrypt, so instead, they prefer to collaborate to generate pre-computed
tables, it starts getting a *big* dictionary in English and generates the
password hash of those words, and store them in a database, following many
combinations with numbers made to get the final result (with the salt), and
much more.

On the deep web, there are those tables, they're called rainbow tables, it's
faster to compare passwords on a database, instead of generating a bunch of
hashes, especially on modern hardware. Those tables are extremely useful for
people that use weak passwords since those types of passwords are more common
on rainbow tables.

## Passwords generators/managers

This is the reason that password managers are extremely, it's not only to store
the passwords, but also to generate extremely long passwords (such as with 100
chars), there are many on the market today, such as

[lastpass](https://www.lastpass.com/), [ bitwarden ](https://bitwarden.com/),
[ KeePassXC ](https://keepassxc.org/), the implementation doesn't matter so
much, it's safer than storing the passwords on a dropbox file or remembering,
yes you shouldn't remember the password, if you can remember probably the
password
already is on a rainbow table.

### the master password

There's a small problem with password managers, they need a master password,
this password is essential to open the password database and only this one
*cannot* be completely random, since you need to remember, so at the minimum
don't use a password but a [ passphrase
](https://www.okta.com/identity-101/password-vs-passphrase/).

Passphrases are phrases, and they're longer than passwords it's safer than
passwords (that you can remember), and remember don't use common phrases, and
associated with you, but instead random ones, as an example.

```
Myfavoritefoodispizza!
```

or

```
MyFavouritetripwastoJapan!
```

etc.

## 2FA

Now one of the most important topics is two-factor authentication.

There're three ways to prove that you're actually who you say you're (in this
case, prove that you're the user on the website/system).

1. Something you know (passwords)
2. Something that you're (biometrics...)
3. Something that you have

2fa is responsible to add a new layer of security to the program, not only
requiring the password, but also some other authentication using something that
you're or something that you have, the most common implementation is the [ TOTP
](https://en.wikipedia.org/wiki/Time-based_one-time_password). It means a
discardable password, that you enter on the website with a timer, it's that
code that your phone generates, and you enter on the application to
authenticate. A good implementation is the [ authy ](https://authy.com/) the
program, and I don't recommend google authenticator, for a simple reason, it's
(until the time of the writing), to recover the codes on another device, so if
you lose your phone probably you will not be able to log in, on most
applications.

Another recommendation is to not use SMS, you can lose your phone or a thief can
get it, even if the burglar doesn't know the password, he still has access to
your SIM card and other limitation is that it's not possible to receive SMS
without a signal, how you will receive a signal without it?

## Encrypt your drivers (on laptops)

This is of extreme importance if you use a laptop, it's essential to encrypt
your drivers, there's an implementation for each platform, search the
recommendation of your platform on google or your favorite search engine. For
some reason, many don't think about this, but the password of your account on
your system is useless since it's possible to use the driver as an external
driver, and in this case, the password is not required. So the recommendation
is to encrypt the drivers, so when you be stolen, or lost your laptop, you know
that at least, the data is safe.

Macs are even easier, you can activate the target disk mode and the mac
becomes a giant pen drive, if you didn't know try to reboot and keep
pressing the _t_ key before the boot.

### The proper way to trash a drive

This is not essential, but it costs nothing to do when you trash a drive
specially HD, you have to destroy the disks before, even with a broken HD,
still is possible to recover the data, so the recommendation is to make a hole
in the disks.

