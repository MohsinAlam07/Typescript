any ব্যবহার করলে TypeScript নিশ্চিতভাবে type checking করতে পারে না। অথচ TypeScript-এর মূল উদ্দেশ্যই হলো type safety নিশ্চিত করা। any ব্যবহার করলে TypeScript সেই ভ্যারিয়েবলের জন্য type checking প্রায় বন্ধ করে দেয়। এর ফলে runtime bug হওয়ার সম্ভাবনা বেড়ে যায়। এছাড়া IDE ভালোভাবে auto-suggestion দিতে পারে না এবং code refactoring করার সময়ও ঝুঁকি তৈরি হয়।1এ কারণেই any কে বলা হয় Type Safety Hole.


unknown বেশি নিরাপদ কারণ এটি আমাদেরকে সাবধানে কোড লিখতে বাধ্য করে।বাস্তব জীবনে আমরা অনেক সময় এমন ডাটা পাই যার টাইপ আগে থেকে নিশ্চিত থাকে না , যেমন API response, user input বা বাইরের কোনো JSON data। এই ধরনের ডাটাকে সরাসরি ব্যবহার করলে runtime error হওয়ার ঝুঁকি থাকে।এখানেই unknown গুরুত্বপূর্ণ।


let age: unknown = 20;

if (typeof age === "number") {
  console.log(age + 5);
}

এখানে আগে check করা হচ্ছে age আসলেই number কিনা।তারপরই calculation করা হচ্ছে।এটাই unknown এর সবচেয়ে বড় সুবিধা