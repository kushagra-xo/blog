+++
title = 'Virtual Private Networks (VPNs)'
date = 2023-11-14T17:12:44+05:30
draft = true
+++

![](https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/78f991b5-80ee-4932-bdca-5f9d824f6cb9/d2uifj1-13e353f1-14b5-476b-893f-739ddd7edde2.jpg/v1/fill/w_1280,h_800,q_75,strp/time_tunnel_by_hbkerr_d2uifj1-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9ODAwIiwicGF0aCI6IlwvZlwvNzhmOTkxYjUtODBlZS00OTMyLWJkY2EtNWY5ZDgyNGY2Y2I5XC9kMnVpZmoxLTEzZTM1M2YxLTE0YjUtNDc2Yi04OTNmLTczOWRkZDdlZGRlMi5qcGciLCJ3aWR0aCI6Ijw9MTI4MCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.o-fAMegBewJwxX43xq1eTLwpzDxiF5P6pFLXkFe9mTY)

## What is a VPN?

VPN stands for Virtual Private Network.

> A virtual private network (VPN) is a mechanism for creating a secure
> connection between a computing device and a computer network, or
> between two networks, using an insecure communication medium such as the
> public Internet
> -- <cite>[Wikipedia][1]</cite>

They provide with the ability to ***connect to remote computers, securely***

> Security and privacy are two distinct concepts.
> <cite> Read more here: [PrivacyGuides][2]</cite>

But why do you care? By connecting to remote computers, you could
***mask and tunnel*** all of your traffic through it. That is how
VPNs are usually used in a personal setting.

What do i mean by mask and tunnel?

- Mask
  - The source of all of your traffic now seems to be the VPN server. It's no longer you connecting to the destination, it's the server.
- Tunnel
  - A secure tunnel is established between you and the VPN server, via encryption, such that the ISP  or anyone else trying to snoop in cannot know what you're trying to do over the Internet.

[1]: https://en.wikipedia.org/wiki/Virtual_private_network
[2]: https://www.privacyguides.org/en/basics/common-threats/#security-and-privacy
