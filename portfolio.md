---
layout: portfolio
title: "Portfolio"
permalink: /portfolio/
cwd: portfolio
---
# Projects
Some of my projects can be found on my [GitHub](https://github.com/signaryk) profile.

## Operating Systems
**Plan 9 from Bell Labs / 9front**: After being introduced to the Plan 9 from Bell Labs operating system by Source Hut author
Drew DeVault, I've begun a dive into the [9front](http://9front.org/) operating system, a fork of the original 
(and now abandoned) Plan 9 operating system. I'm particularly intrigued by the distributed desing of the operating
system and the 9P network protocol for mounting distributed file systems.    

**Pinebook Pro**: I did some work bootstrapping [Arch Linux ARM](https://archlinuxarm.org) and 
[Void Linux](https://voidlinux.org) to the [Pinebook Pro](https://www.pine64.org/pinebook-pro/), a previously unsupported
platform for both distributions. At the time, I hosted a private repository to host binary packages of patched mainline Linux 
kernel, u-boot, and other necessary firmware files. I had intended to write a series of shell scripts and Docker
images to automate the process, but official support was announced as I had more time to work on the project.

**Cross-compiling with `distcc`**: To support my efforts in maintaining a platform for Arch Linux ARM, I'm
using the program `distcc` to distribute builds from a slower-compiling ARM-based SBC to a cross-compiler
on an x86-based workstation. This significantly speeds up build times for large packages such as the Linux
kernel.

**WireGuard**: I have been testing the relatively new [WireGuard](https://wireguard.com) 
VPN protocol in order to access my personal
computing resources securely while away from home and secure my Internet traffic on untrusted networks. Since
the protocol has no support for DHCP, IP addresses must be statically assigned. In order to create a
functioning network, I've had to learn a bit about RFC 1918 IPv4 addressing, CIDR, and IPv6 addressing. 

**Void Linux Binary Packages**: I have contributed to updating a few packages for the 
[Void Linux](https://voidlinux.org) distribution.
Most of this work involved updating build templates, testing the resulting package by compiling and installing
a locally-built version of the package based off the template, and following the project's Git workflow for
submitting changes to templates for automatic package building. 

## Programming
**"SignalAnalyzer"**: An Android application which uses the device's built-in radios to scan the surroundings
for WiFi access points and Bluetooth devices. The scan results are presented to the user in a list showing SSID,
BSSID, and RSSI value for WiFi access points, and device name and MAC address for Bluetooth devices. WiFi access
points are plotted on a map based on location data from the WiGLE database. (GitHub link coming soon)

**Academic assignments**: In my academic career I've worked on many programming assignments in C++ designed
to help me explore general programming principles and practices, data structures and algorithms, and 
interacting with the operating system through POSIX APIs in the C and C++ standard libraries. My most ambitious
project has been writing a client process which can concurrently send requests and receive data from a remote 
server via TCP/IP, and safely write the received data to a file even with 15,000 threads working on the same
file.

**Go**: In a self-guided course of study, I am learning the [Go programming language](https://golang.org) 
by implementing some of the topics learned in past computer science courses in Go instead of C++. As an
example, I've written a solution to a version of the classic reader-writer problem in Go, with 200 threads
(known as "goroutines" in Go) concurrently either producing data or consuming that data. This solution has
two implementations, one utilising mutexes and thread locking, and the other using Go's native "channels"
to share data in a thread-safe manner.  

## Web
**Personal website**: Using the [Jekyll](https://github.com/jekyll/jekyll) static website generator, I've 
created this website, which serve as my digital contact card, resume, and portfolio (and eventually blog).
It is currently hosted on GitHub Pages, but will eventually be moved to my own infrastructure.

**Email**: I run my own SMTP server which serves my personal email address for this domain. It runs on a NixOS
VPS so the server is defined using the Nix package manager's declarative configuration system. In order to
ensure emails that originate from silverknoll.net are authentic, I've set up proper SPF, DKIM, and DMARC records
in my domains DNS settings. SPF defines which IP address I've authorised to deliver emails for my domain, DKIM
is a signature attached to every email originating from the mail server to verify the email originated from my
server, and DMARC defines the policy for emails originating from my domain (in this case that emails should 
pass both SPF and DKIM checks).

**NextCloud**: I host an instance of [NextCloud](https://nextcloud.com) on a VPS provider in order to store 
my files remotely and maintain access to them from any of my devices.
