A software platform that lets you create self-contained versions of your applications that can be deployed quickly, and consistently.

- Lightweight - Alpine environments can save literal gigabytes of space in image size as the operating system is stripped down to what it needs (eg: no need for a gui for your headless server application)
- Portable - can be used across vm's, if you're able to get a docker container up and running on your machine it will more than likely work across all machines
- Fast - spins up in seconds

One way to think about docker and cloud infrastructures is to think about pre-fabricated houses. Houses can be pretty incredibly complicated things to build, first you have to find a plot of land, you have to make sure that the utility companies in your area will be able to service your house, then you have to lay down a foundation on which to build the house on top of. After laying down the foundation, you'll have to build the house itself and it goes on and on...

This situation is exacerbated when you think about the need to house entire villages. For every family you have to build another house. This is kind of analogous to what companies in the early cloud days were forced to do. For every application, they had to stand up another physical server, and install an operating system.

Why not make the apps all live together on the same server? Here, you run into the issue of shared resources. Someone's hogging all the power sockets in the common area, stealing the food in the fridge, and taking showers for way too long. (hogging the cpu and ram, connecting to the network sockets that you need access to) Not only does this situation make for unhappy families, but it's very insecure as well.

What if multiple families could inhabit the same building (multiple apps and os's on the same server) without having to share the same resources (bathrooms, kitchens)? 

Enter virtualization. Through software such as vmware it was made possible to dedicate and isolate compute resources to virtual instances of individually compartmentalized OS's running within a single server (ie: ram, network ports, cpu). eg: a 64 core 512GB ram ubuntu server running 16 instances of CentOS/Ubuntu with 16 cores with 32GB ram each. I would like virtualization to splitting the building into separate apartments with individual 

Perfect! Let's keep this analogy going... 

A bare apartment isn't really a suitable place to live, there's no bed, there's no couch etc... You'll have to still go shopping at Ikea and furnish your apartment, ie: you still have to pull down your code, set your environmental variables, install Node, install your dependencies etc. 

If virtualization is like being able to have individual apartments within the same building. Docker is like having a blueprint for a furnished apartment that you can 3d print on demand. With docker, you make an image based off of a fully operational version of your application. With that image, you can ensure that if it works in one OS environment, you can with relatively high confidence know that it works across all environments.