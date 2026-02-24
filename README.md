1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
Ans: getElementById শুধু id দিয়ে একটি নির্দিষ্ট element নেয়, getElementsByClassName একই class-এর সব element নেয় (HTMLCollection আকারে), querySelector CSS selector ব্যবহার করে প্রথম matching element নেয়, আর querySelectorAll CSS selector দিয়ে সব matching element নেয় (NodeList আকারে)।

2. How do you create and insert a new element into the DOM?
Ans: DOM-এ নতুন element তৈরি করতে প্রথমে document.createElement()  দিয়ে element বানাতে হয়, তারপর innerText বা `innerHTML` দিয়ে তার content ঠিক করতে হয়, আর শেষে appendChild() বা insertBefore() দিয়ে যেখানে চাই সেখানে DOM-এ বসাতে হয়।

3. What is Event Bubbling? And how does it work?
Ans: Event Bubbling হলো যখন কোনো element-এ event ঘটে, সেটা প্রথমে নিজে handle হয় এবং তারপর ধীরে ধীরে parent element, body, document এর দিকে উপরে ওঠে। 
উদাহরণস্বরূপ, button click করলে প্রথমে button, তারপর parent div, তারপর body listener trigger হয়।

4. What is Event Delegation in JavaScript? Why is it useful?
Ans: Event Delegation হলো JavaScript-এ parent element-এ একবার event listener বসিয়ে তার child element-এর events handle করা। কারণ এতে কম code লাগে, performance ভালো থাকে, এবং নতুন dynamically add হওয়া element-এও একই listener দিয়ে event handle করা যায়।

5. What is the difference between preventDefault() and stopPropagation() methods?
Ans: preventDefault() browser-এর default কাজ বন্ধ করে, আর stopPropagation() event bubbling বন্ধ করে যাতে event parent বা উপরের element-এ না যায়। 
