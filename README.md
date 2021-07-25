# nssm Services Install

##Top Ref ::

1.(nssm 2.24-101-g897c7ad)  and copy either the 32-bit or 64-bit executable to any folder on your computer.
```
    nssm install
```
2. add EX. see below

    Path: 
    > C:\Users\Administrator\AppData\Roaming\npm\node-red.cmd
    Startup Dir: 
    > C:\Users\Administrator\.node-red\
    Arguments: 
    > --settings "C:\Users\Administrator\.node-red\settings.js"
    Name: 
    > node-red

3. Win + R RUN type 
```
    services.msc 
```
On the Details tab, give the service a name and set it's startup type to >>Automatic (Delayed Start)<<
you now have a Node-RED service - under service manager, click the 
>>Start Service<< 
button to start your Node-RED service.+

4. For Edit >>nssm edit node-red

    Output :: 
    > C:\Users\Administrator\Documents\node-red
    Error :: 
    > C:\Users\Administrator\Documents\node-red

If you navigate to the I/O tab you will see options for stdin, stdout and stderror streams. These are used mainly on *NIX based systems, but node.js provides some implementation of them and so does nssm. 
If you provide a path to a .txt file like shown above (although I forgot to add the extension), save and restart your Node-RED service, 
the files will be created and any console output from Node-RED will be redirected to the file specified, e.g.:

Ref.
http://richardn.ca/2017/06/12/installing-node-red-as-a-windows-service/
