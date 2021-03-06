---
title: "Track your site with Google Tag manager and Google Analytics"
description: "How to track your site with Google Tag manager and Google Analytics 4 Tags"
slug: "google-analytics-4"
createdAt: "2021-02-01"
tags: ["google-tag-manager", "google-analytics", "how-to"]
---

## Problem

Last week I was trying to set up Google Analytics for my project and I knew that Google Tag manager might also be worth trying as it centralizes and bootstraps all your tags so that you can not only use Goolge Analytics but also other tools from Google on your site.

However, such a common and supposedly easy task took me a while to figure out what the most up to date solution is as Google keeps updating their products and result of a simple search on the internet could be overwhelming for some people. Here's the solution I am using and I think is up to date.

## End Result

Go to website you are tracking and you should see statistics in your google analytics (so that you can see at least there is one visitor, yourself)

![ga result](https://blog0post0images.blob.core.windows.net/google-analytics-4/ga-result.png)

In your Google Tag Manager, you should see a tag of type "Google Analytics: GA4 Configuration"

![gtag result](https://blog0post0images.blob.core.windows.net/google-analytics-4/gtag-result.png)

## Steps

### 1. Google Analytics: Create a new property

- 1.1 Click Admin

![step1-admin](https://blog0post0images.blob.core.windows.net/google-analytics-4/step1-admin.png)

- 1.2 Create new property

![step1-new-property](https://blog0post0images.blob.core.windows.net/google-analytics-4/step1-new-property.png)

- 1.3 Make sure this is disabled

![step1-no-universal](https://blog0post0images.blob.core.windows.net/google-analytics-4/step1-no-universal.png)

### 2. Google Analytics: Create a data stream for the property

- 2.1 Go to Data Streams and add a data stream (mine is for web)

![step2-add-data-stream](https://blog0post0images.blob.core.windows.net/google-analytics-4/step2-add-data-stream.png)

- 2.2 Here's an example. Measurement Id will be used later in Google Tag Manager.

![step2-data-stream-example](https://blog0post0images.blob.core.windows.net/google-analytics-4/step2-data-stream-example.png)

### 3. Google Tag Manager: Create new account and container

Not much going on here, just select the platform you want to target when creating
![step3-new-container](https://blog0post0images.blob.core.windows.net/google-analytics-4/step3-new-container.png)

### 4. Google Tag Manager: Create a new tag

- 4.1 Add a new tag

![step4-new-tag](https://blog0post0images.blob.core.windows.net/google-analytics-4/step4-new-tag.png)

- 4.2 Paste the id here from step 2.2

![step4-new-tag](https://blog0post0images.blob.core.windows.net/google-analytics-4/step4-new-tag-id.png)

### 5. Google Tag Manager: Publish changes

![step5-publish](https://blog0post0images.blob.core.windows.net/google-analytics-4/step5-publish.png)

## Read more

[Google Analytics 4 Tags](https://support.google.com/tagmanager/answer/9442095?hl=en)
