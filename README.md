Steps to reproduce:

1.  Run `./pants compile src/scala/larry/:larry`
2.  Run `./pants compile src/scala/larry/:larry-bin`.  Notice that webpack compiles but scala code is used from cache
3.  Run `./pants compile src/scala/larry/:larry-bin` again.  Everything uses cache
4.  Run `./pants invalidate ::`.  
5.  Run `./pants compile src/scala/larry/:larry`.  Uses cache
6.  Run `./pants compile src/scala/larry/:larry-bin`.  Notice that webpack compiles but scala code is used from cache.  Y THO?

This is a bit of a contrived example but this happens when you switch branches and start from scratch checkout even though
there is a shared cache.
