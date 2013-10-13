SSL Mirrors
===========

Some forms of idleness require preparation.

```
vagrant up
vagrant ssh mirror-a
/vagrant/launch-particle
```

What?
-----

Let us pretend that each of the four Vagrant boxes is a perfect mirror, arranged
in a rectangle such that they will reflect a perfectly elastic particle between
them forever.

```
/-----\
|     |
|     |
|     |
|     |
\\-----/
```

Let us also pretend that the bash script launch-particle generates a perfectly
elastic particle and throws it at the first mirror.

If a particle bounces off the server you happen to be logged into at the time,
then you will hear it. Or at least you can pretend to hear it when it wall emits
to all users.

How Do I Stop This Thing?
-------------------------

Remove a mirror, obviously. Otherwise, good luck and perfect timing.

    vagrant halt mirror-b

Should I Set This Up On A Bunch of Machines at Work?
----------------------------------------------------

No, absolutely not.
