## Configuring Web3 + React-Native

1. yarn add react-native-crypto react-native-randombytes node-libs-browser base-64 web3
2. yarn add -D rn-nodeify@latest
3. ./node_modules/.bin/rn-nodeify --hack --install
4. Copy metro.config.js from this repository
5. Copy shim.js from this repository
6. Add import ./shim.js to index.js first line
7. cd ios/ && pod install && cd ..
8. iOS: Remove GCDAsyncSockcdet.m from references TcpSockets and react-native-udp in Pods => Build Phases => Compile Sources
9. Add script to package.json: "postinstall": "./node_modules/.bin/rn-nodeify --install 'crypto,buffer,react-native-randombytes,vm,stream,http,https,os,url,net,fs' --hack"
