1.

a.getElementById() দিয়ে আমরা সহজেই আইডিকে কল করতে পারি, আর আইডিটা সব সময় ইউনিক হবে। একই আইডি একাধিক বার থাকতে পারবে না।

b. getElementsByClassName() দিয়ে আমরা ক্লাস নেমকে কল করি, আর একই ক্লাস নেম একাধিক বার থাকতে পারে। কিন্তু আমাদের যে ক্লাস নেমটা দরকার সেটাও ব্যবহার করতে পারি [] এই ফাঁকা array এর ভিতর আমাদের যে ক্লাস নেমটা দরকার সেটার index নাম্বার দিয়ে। আর যদি আমরা index নাম্বার কল না করি তাহলে প্রথম ক্লাস নেমটাই কাজ করবে।

c.querySelector() এর ব্যবহার করে আমরা id, className, tagName সবই কল করতে পারবো। সেক্ষেত্রে আমরা id, className, tagName কল করার জন্য querySelector(#id), querySelector(.className), querySelector(h1) এই ভাবে কল করতে হবে। এটা প্রথম ম্যাচিং element কেই ধরে, আর এটা অনেক বেশি ফ্লেক্সিবল।

d.querySelectorAll() দিয়ে আমরা সব ম্যাচিং ক্লাসকেই পাবো

2. DOM এ নতুন element তৈরি করে insert করা খুব সহজ

এটা সাধারণত ৩টা ধাপে করা হয় যথাঃ

1. createElement()

2. a. innerText b. classList c. classList

3. setAttribute

3. কোনো element এ event ঘটলে, সেই event ভিতরের element থেকে বাইরে parent element পর্যন্ত উঠে যায়।

সহজ কথায়ঃevent টা child থেকে parent হয়ে উপরের দিকে উঠতে থাকে।

এটাই হলো Event Bubbling।

৪. Event Delegation হলো এমন একটি টেকনিক যেখানে আমরা প্রতিটি child element-এ আলাদা করে event না দিয়ে, তাদের common parent element-এ একটাই event listener বসাই — আর Event Bubbling ব্যবহার করে child কে handle করি। মানে Event Delegation Parent দিয়ে child handle করে

5. preventDefault() কোনো element-এর default browser behavior বন্ধ করে দেয়।

stopPropagation() Event যেন parent এ bubble না হয় — সেটা বন্ধ করে।