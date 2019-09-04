Secret Contact Sharing
======================

Ideas about sharing *secret identities* in *encrypted* and *obfuscated* form
over  channels where *identity* has *already been established*

Definitions
-----------

For the sake of keeping track of what's going on, I am following these
definitions as best I can while writing this document.

  1. **Identity** A characteristic or group of long-term characteristics which
  can be correlated to the activities of an individual or group
  2. **Secret Identity:** A means of address, such as a name, IP address, or
  hash which is intentionally de-coupled from other identities.
  3. **Encrypted:** When a message is encrypted, it is unreadable except to a
  recipient who has a private key.
  4. **Obfuscated:** When a message is obfuscated, it is impossible to determine
  from the characteristics of the message who the message was communicated to
  or from.

Problem
-------

A user wants to share a peer-to-peer ID with another user of that software whom
the user already knows on a centralized, non-E2E-encrypted, identity-laden
popular platform such as Twitter or Facebook. Lacking other means, the users
must share this secret information using the means at their disposal. Here we
attempt to devise a procedure which is able to de-couple the 'Secret Identity'
which the users wish to share privately from the 'Identity' which is already
established from their association via a publicly derivable social graph.

Initial Thoughts
----------------

I don't think I can possibly prevent a network-level attacker from observing
direct P2P connections as they exist today. It is safest when used with
applications that already feature anonymity, such as I2P, Freenet, and Tor Onion
Services.

This procedure will probably have subtle implications, which is unfortunate. It
is tempting to say that it may only be used on Peer-to-Peer networks that bring
their own anonymity to the table, such as Freenet, I2P, and Tor Onion Services
for example. However, I believe there are other use cases, after all, few people
have the same ISP and primary social network, so association of a secret
identity with a user account by a network level attacker capable of targeting
P2P connection data takes the extra steps of asking a social network for
records, acquiring those records, and analyzing them to correlate activity with
the first occurrence of a peer-to-peer connection. Given that most people aren't
engaging in criminal activity on these networks, it is unlikely that these
non-trivial steps will be taken for much of our target audience, say for
instance casual Tox messenger users. In fact, if a Tox user is facing a network
level attacker who is issuing subpeoneas, nothing has changed for that person
except that Facebook doesn't know something the attacker can already figure out
on their own. Therefore, *even in the case of non-anonymous peer-to-peer ID's,*
*this procedure, properly implemented, should help protect your information*
*from a Facebook-level attacker.* Moreover, in the absence of such a protocol,
it is sometimes possible on some P2P networks for Facebook to observe DHT
acivity by running it's own client. In that case, a user gains something by not
giving Facebook the information necessary to target them with such an attack.

Generified de-coupling procedure
--------------------------------

