Generics: Reusable এবং Strictly Typed কোড
Generics আমাদের এমন function বা component তৈরি করতে সাহায্য করে, যেগুলো বিভিন্ন ধরনের data-এর সাথে কাজ করতে পারে, কিন্তু তারপরও type safety ঠিক থাকে।এর ফলে একই logic বারবার লিখতে হয় না এবং কোড আরও clean ও reusable হয়।

function getValue<T>(value: T): T {
  return value;
}

console.log(getValue("Hello"));
console.log(getValue(100));

এখানে T একটি placeholder type,TypeScript নিজেই বুঝে নেয় কোন data কোন type-এর।