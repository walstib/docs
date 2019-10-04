---
description: >-
  This article describes how to author Azure labs for use on the go deploy Cloud
  Sharing platform.
---

# Authoring

Authoring labs for Microsoft Azure is somewhat different to the conventional Virtual Machine based labs.  Several challenges need to be addressed which have been accommodated in this documentation to ensure a smooth and seamless experience.

### Do I use a Tenant, Subscription or Resource Group deployment? <a id="preparing-an-arm-template-for-deployment-in-cloud-slice"></a>

There are several options when creating Azure labs on the go deploy Cloud Sharing platform.  go deploy can supply everything required or you can BYOS\(s\) \(Bring your own Subscription\(s\)\).  

Most customers do not have 100's of Tenants or Subscriptions available to be able to use for labs.  In these circumstances they tend to use our own subscription pool which has 1000s of Subscriptions available.  However, this comes at a cost.

Here is a break down of the different types of deployment models that go deploy can provide

| Type | Reasons for use |
| :--- | :--- |
| Tenant  | When access is required at the tenant and Azure AD Level \(one per student\) |
| Subscription | When access to the Subscription features is required \(one per student\) |
| Resource Group | When one Subscription can be used for multiple users |

Feel free to reach out to us if you require additional information or wish to discuss these deployment models.

