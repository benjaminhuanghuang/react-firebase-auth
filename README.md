- React Authentication Crash Course With Firebase And Routing -2020-10
https://www.youtube.com/watch?v=PKwu15ldZ7k&t=156s&ab_channel=WebDevSimplified


React + Context + BootStrap + Firebase


## Firebase Auth API
listener for login and logout

```
  useEffect(() => {
    const unsubscribe = auth.onAuthStateChanged(user => {
      setCurrentUser(user)
      setLoading(false)
    })

    return unsubscribe
  }, [])
```

Uer name / password login
```
   return auth.signInWithEmailAndPassword(email, password)
```


Google login
```
  auth.signInWithPopup(provider)
      .then((user) => {
        setCurrentUser(user);
        history.push("/");
      })
      .catch((error) => {
        alert(error.message);
      });
```

Logout
```
  auth.signOut()
```


Reset password
```
  auth.sendPasswordResetEmail(email)
```

Update
```
   currentUser.updateEmail(email)
   currentUser.updatePassword(password)
```
