- React Authentication Crash Course With Firebase And Routing -2020-10
https://www.youtube.com/watch?v=PKwu15ldZ7k&t=156s&ab_channel=WebDevSimplified


React + Context + BootStrap + Firebase


## Firebase Auth API
```
  useEffect(() => {
    const unsubscribe = auth.onAuthStateChanged(user => {
      setCurrentUser(user)
      setLoading(false)
    })

    return unsubscribe
  }, [])
```