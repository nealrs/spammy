# spammy

I write 3-4 email newsletters every week, so deliverability is super important to me. To that end, I need to make sure my subject lines don't set off any ISP / spam filter alarms.  

Pass spammy a string and it'll tell you if it contains any words or phrases commonly associated with email spam. If it returns false, you're good. If it returns true, revise your copy.

I pulled the triggers from this HubSpot blog post: http://blog.hubspot.com/blog/tabid/6307/bid/30684/The-Ultimate-List-of-Email-SPAM-Trigger-Words.aspx

**Usage**

```js
spammy("Hey, do you want to buy a luxury car $$$?"); // true
spammy("Great apartments - no fees"); // true
spammy("Check it out bruh"); // true because of 'check'
spammy("Can you take a look at this?"); // false
spammy("Win a million dollars"); // true
spammy("I love you"); // false
```

**Issues**

spammy isn't perfect. Words like 'check', 'now', 'only', etc _will_ trigger some false positives, even though they are quite common and may be appropriate for your campaign. But I think it's better to be conservative. Perhaps later on I'll revise this to highlight or return the specific spammy text.

**Contribution**

If you can think of any additional trigger phrases, please submit a PR. I'm sure these things evolve over time. Spammy is open sourced under the MIT licensed.
