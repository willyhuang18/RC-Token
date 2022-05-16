# RC-Token
This application is Non-real Token, this is generate for people is interesting on knowing more about the web token. Not for commercial. The code might not be perfect.

## Technologies Used

* [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
* [ReactJS](https://reactjs.org/)
* [Ubuntu](https://ubuntu.com/)
* [DFX](https://smartcontracts.org/docs/current/developer-docs/quickstart/hello10mins)
* [Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
* [Node.js](https://nodejs.org/en/)
* [Motoko](https://smartcontracts.org/docs/current/developer-docs/build/languages/motoko/)


## Getting Started
- Make sure you had the dfx installed on the computer, and also the ubuntu version of VS code is avaliable. Here is the tutorial for [Window](https://docs.google.com/document/d/e/2PACX-1vTNicu-xuf4EiLAehHIqgfpjAnPjzqMGT-xpZVvYaAWNyvzYK_Ceve_me4PVRIxpzH7ea5PAX9NxGwY/pub) and [Mac](https://docs.google.com/document/d/e/2PACX-1vTSgoWcVvuMW4Aa78MyqeK0_ZRl_MaV7rS-tdhya3jlPbSSbxczQFCohrGf87T4F7tJKXwTjT2z_QSq/pub) Credit to Dr.Angela Yu from Udemy
- To Install and Run the Project

1. start local dfx

```
dfx start --clean
```
2. Run Npm install

```
npm install
```

3. Run NPM server

```
npm start
```

4. Deploy canisters

```
dfx deploy 
```

5. Head to localhost

http://localhost:8080/

## User Stories

As a user, I want to be able to getting the Token from the web

As a user, I want to be able to transfer the token.

As a user, I want to be able to Check the balance.

# Check your Balance

1. Find out your principal id:

```
dfx identity get-principal
```

2. Save it somewhere.

e.g. My principal id is: trt5l-f3h3n-z6ouo-at4z7-akjoe-3tfha-zjljz-4woeh-e5i7m-jzf3j-fqe


3. Format and store it in a command line variable:
```
OWNER_PUBLIC_KEY="principal \"$( \dfx identity get-principal )\""
```

4. Check that step 3 worked by printing it out:
```
echo $OWNER_PUBLIC_KEY
```

5. Check the owner's balance:
```
dfx canister call token balanceOf "( $OWNER_PUBLIC_KEY )"
```

# Charge the Canister


1. Check canister ID:
```
dfx canister id token
```

2. Save canister ID into a command line variable:
```
CANISTER_PUBLIC_KEY="principal \"$( \dfx canister id token )\""
```

3. Check canister ID has been successfully saved:
```
echo $CANISTER_PUBLIC_KEY
```

4. Transfer half a billion tokens to the canister Principal ID:
```
dfx canister call token transfer "($CANISTER_PUBLIC_KEY, 500_000_000)"
```

## Design Layout
![image](https://user-images.githubusercontent.com/87446864/168391903-3c965bbb-bcb4-435c-b9e0-a4d6a01051d6.png)


## Authors

* **Panta Huang** 
- [Github](https://github.com/willyhuang18)
- [LinkedIn](https://www.linkedin.com/feed/)

- Credit to Dr.Angela Yu from Udemy


## License

This project is licensed under the MIT License 
