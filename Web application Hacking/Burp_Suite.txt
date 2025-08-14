# Burp Suite Notes

## Proxy
The **Burp Proxy** is the most renowned aspect of Burp Suite.  
It enables interception and modification of requests and responses while interacting with web applications.

---

## [Repeater](https://tryhackme.com/room/burpsuiterepeater)
Another well-known feature. Repeater allows for capturing, modifying, and resending the same request multiple times.  
This functionality is particularly useful when:
- Crafting payloads through trial and error (e.g., SQL Injection)
- Testing the functionality of an endpoint for vulnerabilities

---

## [Intruder](https://tryhackme.com/room/burpsuiteintruder)
Despite rate limitations in Burp Suite Community, Intruder allows for spraying endpoints with requests.  
Common uses:
- Brute-force attacks
- Fuzzing endpoints

---

## [Decoder](https://tryhackme.com/room/burpsuiteom)
Offers a valuable service for data transformation. It can:
- Decode captured information
- Encode payloads before sending them to the target  
While other tools can do this, having Decoder integrated in Burp Suite is highly efficient.

---

## [Comparer](https://tryhackme.com/room/burpsuiteom)
Enables the comparison of two pieces of data at either the word or byte level.  
The ability to send large data segments directly to a comparison tool with a single keyboard shortcut significantly speeds up the process.

---

## [Sequencer](https://tryhackme.com/room/burpsuiteom)
Typically used to assess the randomness of tokens, such as:
- Session cookie values
- Randomly generated data  
If the randomness algorithm is weak, it may expose critical vulnerabilities.
