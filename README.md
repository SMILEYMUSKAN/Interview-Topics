# Interview-Topics

1. Debounce Concept
2. CORS(cross origin request) Error 

## Debounce Concept
Debouncing is a programming practice used to ensure that time-consuming tasks do not fire so often, that it stalls the performance of the web page. In other words, it limits the rate at which a function gets invoked.

Debouncing in JavaScript is a practice used to improve browser performance. There might be some functionality in a web page that requires time-consuming computations. If such a method is invoked frequently, it might greatly affect the performance of the browser, as JavaScript is a single-threaded language. 

### Here is a simple implementation of debouncing:-
```ts
 useEffect(() => {
    setLoading(true);
    const clearTimeOutId = setTimeout(() => {
      getData();
     }, 500)
    
    // ComponentWillUnMount Function
   return () => clearInterval(clearTimeOutId)
  }, [searchText])

```
### Reference Link
https://github.com/SMILEYMUSKAN/nextjs-fullstack-app/blob/main/ui/components/SearchBar.tsx

## CORS(cross origin request) Error 
Handling CORS Errors in React
This error occurs when the server doesn't include an Access-Control-Allow-Origin header in its response, which tells the browser which origins are allowed to access the server's resources. To fix this error, you need to enable CORS on your backend server.

### Note:- 
- We can't resolve **CORS** Error in plain react application, resolving **cors** is backend issue and backend developers had to handle it.

- **CORS** Error always occured in client side rendering, in server side rendering **cors** issue does'nt occurs.

### Reference Link
https://blog.logrocket.com/using-cors-next-js-handle-cross-origin-requests
