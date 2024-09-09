# Description
Promise JavaScript ka aik feature hai jo asynchronous code ko handle karnay mein madad karta hai. Jab hum koi promise create karte hain, us waqt humein foran uska final result (value ya error) nahi milta, lekin promise humein ye guarantee deta hai ke future mein wo result mil jayega.



### Promises Ke 3 States Hoti Hain:
1. **Pending (Intezaar Karna):** Jab promise banaya jata hai, wo initial state mein hota hai aur abhi kuch result nahi diya.
   
2. **Fulfilled (Kaam Ho Gaya):** Jab asynchronous kaam successfully complete ho jata hai, to promise fulfilled ho jata hai aur humein result deta hai.

3. **Rejected (Kaam Mein Ghalti Hui):** Agar kaam galat hota hai ya error aata hai, to promise reject ho jata hai aur humein error milta hai.

### Promises Ke Saath Handlers:
Promises ke sath hum 2 main handlers use karte hain:
- **`.then()`:** Ye tab call hota hai jab promise fulfill ho jata hai, yani kaam successful hota hai aur result mil jata hai.
- **`.catch()`:** Ye tab call hota hai jab promise reject ho jata hai, yani koi error ya problem aati hai.
### Example:
```javascript
let promise = new Promise((resolve, reject) => {
  // Asynchronous kaam: API se data fetch karna
  setTimeout(() => {
    let success = true; // maan lo data successfully mil gaya
    if (success) {
      resolve("Data mil gaya!"); // Agar success ho, to ye result humein milega
    } else {
      reject("Error aayi!"); // Agar success na ho, to ye error milega
    }
  }, 2000);
});

// Kaise promise ka result handle karte hain
promise
  .then((result) => {
    console.log(result); // "Data mil gaya!" ye tab chalega jab promise fulfill ho
  })
  .catch((error) => {
    console.error(error); // "Error aayi!" ye tab chalega jab promise reject ho
  });
```

 ## Summary:
Promise ek "intezaar ka vaada" hai ke future mein result ya error milega. Jab promise ka kaam complete ho jata hai, wo ya to result dega (then()) ya error (catch()), lekin ye sab kuch asynchronously hota hai, yani kuch time baad, foran nahi.
Promise JavaScript ka aik feature hai jo asynchronous code ko handle karnay mein madad karta hai. Jab hum koi promise create karte hain, us waqt humein foran uska final result (value ya error) nahi milta, lekin promise humein ye guarantee deta hai ke future mein wo result mil jayega.





