# todo

```
$ firebase use yourproject
$ cd functions
$ npm i
```

create /public/firebase.js

```firebase.js
const firebaseConfig = { // replace to your apiKey
    apiKey: "",
    authDomain: "",
    projectId: "",
    storageBucket: "",
    messagingSenderId: "",
    appId: "",
};

firebase.initializeApp(firebaseConfig);
const isEmulating = window.location.hostname === "localhost";
if (isEmulating) {
    //firebase.auth().useEmulator("http://localhost:9099");
    //firebase.storage().useEmulator('localhost', 9199);
    firebase.firestore().useEmulator('localhost', 8080);
    firebase.functions().useEmulator('localhost', 5001);
}
```

