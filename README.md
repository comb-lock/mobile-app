# Comb Lock Mobile App

[中文版](/README-CN.md)

This is an implementation of a basic mobile app in accordance with the [Core Specification](https://github.com/comb-lock/Core/blob/master/README.md#client-rules) of the Comb Lock project, which can be compiled and used on Android and iOS in recent years.

You can [download](download.url) the Android app to experience it.

[a few images, across the row]

## App Features

From the originator of this project, the official minimalist version, just good.

- No background residue or wakeup call
- even NOT need internet access
- Each action is fully prompted and responded to with results
- Forced high strength root password
- Minimal, very easy for you to modify to your liking

## Frequent Q&A

Q: How do I recover data if I forgot the root password?

> A: Unfortunately, all clients are encrypted in the same way as [Core](https://github.com/comb-lock/Core/blob/master/README-CN.md), securely and transparently, with no way to retrieve the password. If you can't remember the root password, then the encrypted document will remain a secret forever.

Q: Is the encryption secure, and is there any chance of it being broken?

> A: As above, the project is encrypted and decrypted by taking the `MD5` hash of the strong `root password` to a unique `32-bit key`, and then encrypting and decrypting the `entire document` by the `AES-256 CBC` algorithm.
> 
> Theoretically, the package was secure enough for quite some time. Where it could go wrong is in being socially engineered for using the same password that has been compromised.
>
> So, make sure the root password is strong enough and stored only in a secure place (maybe only in your head, haha).

Q: Are encrypted documents also universal and can I decrypt them manually?

> A: Yes, you can back up the encrypted document to multiple places to ensure it stays around longer. As long as the root password is secure, then it is absolutely safe.
> 
> The project was designed with all kinds of extremes in mind, so Comb Lock is more like a specification than a few products. The encrypted documentation is common to all clients, and you can still refer to [Core](https://github.com/comb-lock/Core/blob/master/README-CN.md) to do everything manually.

Q: I think the app is too rudimentary and I'd like to add some new features!

> A: Welcome! The point of open source is to inspire more wonderful creations. All repositories in this project are under Apache-2.0 License, which you are free to modify.
>
> But please note that the Comb Lock project itself exists to provide as much security as possible at the tool level, and if your work fails to adhere to the [Core Specification](https://github.com/comb-lock/Core/blob/master/README.md#client-rules), please prominently prompt the user (e.g., at least three seconds to force reading) to prevent the associated risks from arising.
>
> The author is not responsible for any consequences that may arise as a result, so please be careful.