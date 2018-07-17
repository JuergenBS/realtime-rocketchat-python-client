# Realtime Rocketchat Python Client (originally Unha2)

This is a work-in-progress library to interact with Rocket.Chat using
websockets (the "realtime API") in an asynchronous way.

It has been developed by @mathieui a year ago. Since that time [aiohttp](https://github.com/aio-libs/aiohttp) 
had some breaking change, which have been solved in this version. Furthermore some enhancements on missing functions have been made.
Feel free to contribute to this library!

## Getting started

You can clone the lib using:
```
git clone git@github.com:djuelg/realtime-rocketchat-python-client.git
```

Afterwards you have to install it, using the installer:
```
python3 setup.py install
```

Now head over to the `examples/` folder and have a look at the example code.
You can run the interactive shell example using:
```
python3 prompt.py --server open.rocket.chat --username username --password your-super-secret-password
```

## Documentation

### Classes in client.py

The most important funcionality is stored in `client.py` as shown below. The other files are rather small and you can take a look at them for yourself.

* ClientData → Data used to connect to a server
* ClientAPI → Contains all the API methods
* Client → Creates a websocket and a connection to the server
* EventClient → Handling incoming events of type *added, changed, updated, removed, failed*
* OverrideClient → This is a basic implementation of a client. You can take a look how it is used in the [prompt example](/examples/prompt.py)

For further documentation take a look at the [docs folder](/docs).

## Thanks

I want to thank @mathieui for developing the basic structure of this library!

Many things were found out from reading the source of *purple-rocketchat*, so
@mathieui want to thank its author for taking the time to write the plugin.