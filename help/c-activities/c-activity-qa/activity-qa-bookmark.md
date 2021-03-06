---
description: Information to help you use the Target QA bookmarklet to force Target to release you from QA mode.
keywords: qa;preview;bookmarklet;preview links
seo-description: Information to help you use the Target QA bookmarklet to force Target to release you from QA mode.
seo-title: Activity QA bookmarklet
solution: Target
title: Activity QA bookmarklet
topic: Advanced,Standard,Classic
uuid: 2890e215-16c9-4b22-a8eb-732cd6efede3
---

# Activity QA bookmarklet{#activity-qa-bookmarklet}

Information to help you use the Target QA bookmarklet to force Target to release you from QA mode.

Because [QA mode](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) is sticky, after you browse a website in QA mode, your Target session must expire or you need to have Target release you from QA mode before you can view your site like a typical visitor. Use the QA Target bookmarklet to force yourself out of QA mode.

To use the Target QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser's Bookmarks Toolbar:

```javascript
(function%20()%20{var%20parts%20=%20window.location.href.split('at_preview_token',2);%20if%20(parts.length%20>%201)%20{window.location.href%20=%20parts[0].concat('at_preview_token=');}%20})();
```

The bookmarklet should then appear on the toolbar for re-use.

>[!NOTE]
>
>The process to create a bookmarklet varies by browser type and version. Consult your browser's help or search on the Internet for specific directions.

You can also manually force yourself out of QA mode by loading a page on your site with the `at_preview_token` parameter with an empty value (for example, `https://www.mysite.com/?at_preview_token=`). 
