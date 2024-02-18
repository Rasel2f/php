# শুরুর পদক্ষেপ

## PHP ইনস্টলেশন

আপনি যদি HTML, CSS এবং JavaScript শিখে **PHP** শিখতে এসে থাকেন প্রথমত আপনাকে একটা বিষয় বুঝতে হবে। **PHP** একটি সার্ভার-সাইড ল্যাংগুয়েজ। যার অর্থ আপনি **PHP** কোড লিখে তার আউটপুট সচরাচর HTML, JavaScript এর মত ব্রাউজারে দেখতে পাবেন না। এজন্য আপনাকে এক্সট্রা কিছু পদক্ষেপ নিতে হবে। যার মধ্যে প্রথম হল, –(সার্ভার-সাইড ল্যাংগুয়েজ রান করার জন্য) – একটি সার্ভার সেটআপ করা। পরবর্তীতে এটা নিয়েই কথা হবে।

সকল অপারেটিং সিস্টেমেই **PHP** ব‍্যবহার করার সুযোগ আছে। অপারেটিং সিস্টেমভেদে ব্যবহার পদ্ধতিতে যেমন ভিন্নতা রয়েছে, তেমনি রয়েছে সিস্টেম স্পেসিফিক বিভিন্ন প‍্যাকেজ এবং টুল।

Mac ইউজারদের জন‍্য **PHP** আগে থেকেই ইনস্টল থাকে। সেক্ষেত্রে _Apache configuration file_ **httpd.conf** এর কিছু লাইন আনকমেন্ট করলেই **PHP** কোড লিখে তা এক্সেস করা যাবে। ফাইলটি `/private/etc/apache2/httpd.conf` সাধারণত এই পাথেই পাওয়া যাবে — (যদি পরিবর্তন না করা হয়)। এই ফাইলের নিন্মের লাইন দুটির সামনে থেকে `# (hash sign)` সরিয়ে দিলে আনকমেন্ট হবে। অতঃপর আপনি `php –v` দিয়ে চেক করতে পারেন PHP কাজ করছে কিনা।

```apache
# LoadModule php5_module libexec/httpd/libphp5.so
# AddModule mod_php5.c
```

আরও, সহজ পন্থায় নিচের প্যাকেজগুলো থেকে যেকোন একটা দিয়েও ইনস্টল করতে পারেন। আরো প্যাকেজ অপশন দেখার জন্য বা ইনস্টলেশন গাইড জানার জন্য গুগল করুন।

-   [Home Brew](https://brew.sh/)


-   [Herd](https://herd.laravel.com/)


যদি লিনাক্স ইউজার হোন তাহলে আমার পরামর্শ হচ্ছে আপনি কোন প্রকার প‍্যাকেজ ব‍্যবহার না করে সরাসরি টারমিনাল দিয়ে সেটাপ দিন। এ জন‍্য নিচের কমান্ড ২টি ব্যবহার করুন। বিস্তারিত জানতে গুগল করুন।

```bash
sudo  apt-get update &&  sudo  apt-get upgrade

sudo apt-get  install php
```

Windows ইউজারদের জন‍্য **PHP** সেটাপ করাটা কিছুটা ট্রিকি টাস্ক। কারণ এক্ষেত্রে Mac এর মত যেমনি _Pre-installed_ **PHP** পাওয়া যায় না, তেমনি কমান্ড লাইন ব্যবহার করেও ইনস্টল করার সুযোগ নাই। তবে সহজ দুটি অপশন আছে। এক. ম্যানুয়ালি সেটআপ করা। যেটা ফলো করা কঠিন হলেও আপনার জন্য রেকমেন্ডেড। এক্ষেত্রে মূল কাজটি হল আপনার মেশিনে **_PHP Environment Variable_** সেট করা। কেন এবং কিভাবে জানতে এই [ডক ফাইলটির](https://docs.google.com/document/d/1eLROwtv_BHfqPpa_lMPod__pWLTkin3446SKQl7taM4/edit?usp=sharing) সাহায্য নিন। আপনি গুগল বা ইউটিউবেও গাইডলাইন পেয়ে যাবেন।

২য় উপায় হল, **_PHP Installer Tools_** এর সাহায্য নেয়া। সেজন্য অনেক ধরণের টুল এভেলেবল আছে। নিচে জনপ্রিয় কিছু টুলের তালিকা দেয়া হল।

-   [Laragon](https://laragon.org/index.html)


-   [Wampserver](https://www.wampserver.com/en/)


-   [XAMPP Server](https://www.apachefriends.org/download.html)


-   [WSL](https://learn.microsoft.com/en-us/windows/wsl/install)


এখানে খেয়াল রাখবেন, ম্যানুয়ালি **PHP** ইনস্টল করলে আপনি আলাদা কিছু সুবিধা পাবেন, যা এই টুলগুলোর ক্ষেত্রে সুলভ নয়। এ বিষয়ে আরো বিস্তারিত জানতে **PHP’র** [**Official Manual**](https://www.php.net/manual/en/install.php) এর সাহায্য নিন।

## PHP ইনস্টলেশনের পরবর্তী পদক্ষেপসমূহ

**PHP** ইনস্টল করা হলে আপনাকে _Terminal'র_ ব‍্যবহার শেখা উচিত। প্রতিটি অপারেটিং সিস্টেমের সাথে _Terminal_ ইন্টিগ্রেটেড বা যুক্ত করা থাকে। সংক্ষেপে _Terminal_ হল আপনার কম্পিউটারের একটি টেক্সট-বেইজড ইন্টারফেস। যা দিয়ে বিভিন্ন ধরণের অপারেশন যেমন: কমান্ড টাইপ করে ফাইল ম্যানিপুলেশন, প্রোগ্রাম এক্সিকিউশন, ডকুমেন্টস ওপেন করাসহ আরো অনেক কিছু করতে পারবেন। বেসিক্যালি এমন অনেক কাজ যা আপনি কিবোর্ড-মাউস চেপে করে থাকেন তা কিছু নির্দিষ্ট কমান্ডের সাহায্যেই করতে পারবেন।

যারা এডভান্সলি _Terminal_ ব্যবহার করেন তারা এই কমান্ডগুলো জানেন, যারা একদমই নতুন তাদের এগুলো শেখা উচিত। নিচে সচরাচর ব‍্যবহৃত কিছু কমান্ড দেওয়া হল:

ফোল্ডার তৈরি করা

```bash
mkdir foldername
```

তৈরি করা ফোল্ডারে প্রবেশ করা

```bash
cd foldername
```

ফোল্ডারের ভিতরে কি কি আছে তা চেক করা

```bash
ls
```
```bash
ls  -la
```

ফোল্ডার থেকে বাহির হওয়া

```bash
cd  ..
```

মনে রাখবেন উপরের কমান্ডগুলো _Linux_ বেইজড _Git Bash’র_। কিছু কিছু কমান্ড Mac বা Windows’র সাথে মিলে যেতে পারে। তবে প্রত্যেকটা অপারেটিং সিস্টেমের আলাদা আলাদা কমান্ড লাইন আছে। যেহেতু ডে-টু-ডে লাইফে এমন কমান্ডগুলোর ব্যবহার আপনার দরকার হবে, তাই এই কমান্ডগুলো সকল ডেভলপারের শেখা উচিত।

### কোন কমান্ড লাইন শিখবেন?

সিস্টেম স্পেসিফিক কমান্ড লাইন অনেক ক্ষেত্রেই দরকার পড়ে। তাই সেগুলো শেখা যেতে পারে। তবে আপনার এমন কমান্ড লাইন শেখা উচিত যেটা আসলে কোন সিস্টেমের মধ্যে সীমাবদ্ধ থাকে না। ফলে Mac, Windows বা Linux; সিস্টেম যাইহোক আপনি নির্দ্বিধায় যেকোন জায়গায় সেটা ব্যবহার করতে পারেন। এমন মাল্টি-সিস্টেম-সাপোর্টেড একটি টুলের নাম [**Git Bash**](https://git-scm.com/downloads)। এছাড়াও আরো অনেক টুল আছে। সব বিষয়ে বিস্তারিত জানতে, Git Bash’র আরো কমান্ড পেতে [ডকুমেন্টেশন ম্যানুয়াল](https://git-scm.com/docs) পড়ুন বা গুগল করুন।

এছাড়াও আপনি Mac ইউজার হলে ডিফল্ট যে Terminal আছে সেটা ব‍্যবহার করতে পারেন অথবা [iterm2](https://iterm2.com/), [warp](https://www.warp.dev/) ব‍্যবহার করতে পারেন।

Windows’র জন‍্য [Windows Terminal](https://apps.microsoft.com/detail/windows-terminal/9N0DX20HK701?hl=en-us&gl=BD) এবং Linux’র জন‍্য ডিফল্ট যে Terminal আছে তাই যথেষ্ট। চাইলে আপনার পছন্দ অনুযায়ী বিকল্প কিছুও ব্যবহার করতে পারেন।