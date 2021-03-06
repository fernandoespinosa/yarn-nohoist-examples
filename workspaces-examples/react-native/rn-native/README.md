# how to create a native react-native app in yarn workspaces

Goal: Create a react-native app in yarn workspaces using `react-native init` (see react-native [Building Projects with Native Code](https://facebook.github.io/react-native/docs/getting-started.html))

## step-1 setup the workspaces config
Follow the configuration setup for [react-native workspaces](../README.md#common-configuration). 

## step-2 create react-native package
go to the "packages" directory, follow the react-native getting started guide **"Building Projects with Native Code"** to create a react-native app:
```
$pwd
.../workspaces-examples/react-native/rn-native
$ cd packages
$ react-native init MyApp
```
the installation will run for a while, once it is done it will prompt you to go into the MyApp directory and run `react-native run-ios` or `react-native run-android`. If you encountered any issue when starting the app, try to reset node_modules then run yarn install again:
```
$ cd MyApp
$ rm -rf node_modules/ package-lock.json 
$ yarn install
```
now you should be able to start the app:
```
$ react-native run-ios
```
If you see the app started in the simulator, congratulations, you have just installed the react-native in yarn workspaces, hopefully much easier than before.  



