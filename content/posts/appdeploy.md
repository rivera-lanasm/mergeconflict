---
title: "Hugo Blurb: Deploy App on AWS Amplify on Route53 Verified Domain"
date: 2022-12-18T18:15:51-05:00
draft: false
---

### Deploy App on AWS Amplify
[Hugo Docs](https://gohugo.io/hosting-and-deployment/hosting-on-aws-amplify/)
 
Specifying Hugo version Amplify uses upon deployment
- When setting up my site on local, I was using the latest Hugo release (which snap gave me by default: **v.0.108**
- According to this blog [post](https://seanrmurphy.medium.com/deploying-and-managing-a-modern-hugo-site-on-aws-amplify-f771f6440b43), Amplify provides Hugo version 0.75.1 by default. The theme I am using, however, has min. requirement of **0.77**
- Specifying the version of Hugo AWS Amplify should use in the build script is simple, outlined in this [post](https://michaux.co/posts/specifying-hugo-version-on-aws-amplify/)

