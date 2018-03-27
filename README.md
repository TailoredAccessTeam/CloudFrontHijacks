When a CloudFront customer uses the service, but later removes it from their account, it leaves a CNAME record in their Domain. An attacker can go ahead and register that CloudFront CNAME and obtain the necessary access to "hijack" the domain involved and serve content under that domain.

This repository is released to the public. As of 27 March 2018, I found that a large number of the domains had been "reserved" and no longer hijackable. This indicates that an entity had performed similar enumeration and identified this list and took action to weaponise and attack all of these domains, but had not released any public information. The instances had not been activated yet at this point in time but whoever has took control over all of these CNAMEs could "flip the switch" and serve malicious content at any time of their choosing.

I am releasing this list so that the public can check whether they are likely to be suspectible. If not, you should still check that there are no dangling CNAME records pointed to abandoned CloudFront instances. If you are on this list, you should remove your CNAME record immediately if you do not have control over the corresponding CloudFront instance with the matching CNAME.