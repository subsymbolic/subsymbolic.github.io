---
layout: post
title: "The future of online card payments"
date: 2015-02-14
categories: 
  - "tech"
tags: 
  - 3dsecure
  - payments
---

If you shop online you will invariably have seen 3-D Secure, a service used to protect online card payments, embedded in your payment screen under one of its guises. Perhaps as Verified by Visa or MasterCard SecureCode. <!--more-->

![3-D Secure popup](/assets/future-of-online-payments-3-d-secure-popup.gif)

While some consumers may feel that this service keeps them safe when shopping online, in reality, it suffers from major security and usability issues and Visa and Mastercard have announced that they are pulling the plug.[^1] 

## What's wrong are the problems with 3-D Secure?


### It teaches people bad habits

Websites use SSL encryption to keep private data safe during communication. Users should check that they are on the website they expect, that the URL starts with https to indicate SSL encryption and that the identity of the website is trusted. Most web browsers visually indicate a securely encrypted connection.

<img src="/assets/future-of-online-payments-browser-https.png" alt="Web browser https indicator" width="440"/>

One problem with 3-D Secure is that the service is hosted by third-party providers. This means that the user is *not* communicating with the site they are currently on. To hide this confusing fact, the 3-D Secure form often appears in a popup window or iframe (a website embedded within the merchant's website) and does not display a URL bar. This limits a user's ability to easily verify the site's identity and encourages them to just "trust" the popup or iframe.

### It is vulnerable to phishing

Another problem with presenting payment authentication in iframes or popups is that they can be indistinguishable from iframes or popups from malicious websites. For example, if a user is shopping and browsing over numerous tabs, a malicious website could open a new window that looks like the 3-D Secure service, to fool them into entering their details.

On the flip side, savvy users who meticulously check their traffic may see their browser communicate with an unknown third party and assume that a legitimate 3-D Secure screen is a phishing attack.

### User experience is poor

I could write pages about how poor the user experience is. Everything from the overall dated look and feel, the jarring integration with merchant websites, to pages not rendering correctly or at all.

The mobile experience is worse again with the site bordering on unusable on many mobile browsers. As there is no mobile application solution, developers have been forced to embed completely alien-looking web views in their apps to render the 3-D Secure service. Users may be thrust from a slick application to a payment page designed for a desktop - one that on mobile requires lots of whitespace scrolling and tiny forms with tiny text fields.

But I will stop my usability rant there. It is the customer reaction to the service that speaks loudest. A significant number of customers abandon their shopping carts at the 3-D Secure phase and this equates to revenue loss. In one example, North Side Media reported around a 60% reduction in client sales during a 3-D Secure trial.[^2]

### It is designed to protect the merchant, not the customer

Few consumers realise that 3-D Secure is designed to protect the merchant not them. Generally, when a customer calls their bank about a fraudulent card transaction, their bank will pull the funds from the merchant and refund them. A merchant using 3-D Secure is however protected from this potential loss of revenue.

It almost seems reasonable. The merchant has done everything they can to protect their customer by using a secure service. If there's fraud, it's not their fault. It must have come from somewhere else. Perhaps the customer shared their password with someone. Or maybe they have malware on their computer.

So who pays? The burden returns to the bank. Some banks have wording deeming the customer responsible for all 3-D Secure transactions, even in cases where fraud has occurred and there is no evidence to suggest negligence on their part.[^3]


## The future

We have little information about what financial institutions have in store for us next. Ideally, the next card protection service will be secure, seamless and user-friendly. It should minimise fraud by taking advantage of new technologies and should incorporate a risk-based authentication model, requesting greater customer verification for riskier transactions.

### Determining risk

Transactions could be given a risk score that takes into consideration details such as:

- **where is the customer?** Are they at home, at work or on the other side of the world?
- **what device are they on?** Are they on their laptop, mobile phone or an unknown computer?
- **who is the merchant?** Are they generally trusted? Has this customer used the merchant before?
- **how large is the transaction?** Is it a trivial or larger amount? 
- **is this type of transaction risky?** Gambling credits may be more fraud-prone than linen purchases.
- **is it a typical transaction?** Is this kind of purchase characteristic of the customer's usual spending habits?

### Authentication

Once a risk level is calculated this could be used to determine the requisite authentication. The following examples outline some authentication scenarios.

<table>
  <tbody>
    <tr>
      <td><strong>Almost risk-free</strong></td>
      <td>Customer is on their mobile at home and buys a small item from a regular merchant</td>
      <td>No authentication required. Customer simply enters payment details</td>
    </tr>
    <tr>
      <td><strong>Low-risk</strong></td>
      <td>Customer is on their pc at home and buys an item from a new merchant</td>
      <td>Customer is asked a verification question</td></tr>
    <tr>
      <td><strong>Medium risk</strong></td>
      <td>Customer is on their laptop 30km from home and is purchasing an item from a new merchant and for a non-trivial amount</td><td>Customer is sent an SMS authorisation to enter to complete the transaction</td>
    </tr>
    <tr>
      <td><strong>High-risk</strong></td>
      <td>Customer is on an unrecognised computer on the other side of the world, buying expensive goods from a high-risk merchant</td>
      <td>Customer provides a fingerprint or iris scan</td>
    </tr>
  </tbody>
</table>

## Conclusion

3-D Secure is a poor service which exposes customers to serious security issues while simultaneously pushing the burden of fraudulent activity onto them. This is unfair. Additionally, usability is problematic. While 3-D Secure may protect merchants from fraud, it also costs them a significant amount of lost revenue. All things considered, the move away from 3-D Secure is a good one.

Looking forward, any new system should be easy to use and should legitimately protect consumers. Fraud signifies that current systems or processes have been breached -- the burden of fraud must lie with the financial institutions that have the power to fix these.

Done right, a new easy and secure system will promote stress-free customer spending online.

## References

[^1]: S. Curtis, "Mastercard and Visa to kill off password authentication," _The Telegraph,_ Nov 13, 2014. \[Online\]. Available: [http://www.telegraph.co.uk/technology/news/11228300/Mastercard-and-Visa-to-kill-off-password-authentication.html](http://www.telegraph.co.uk/technology/news/11228300/Mastercard-and-Visa-to-kill-off-password-authentication.html). Accessed Nov. 13, 2014.

[^2]: A. Bouch, "3-D Secure: A critical review of 3-D Secure and its effectiveness in preventing card not present fraud," MSc thesis, University of London. 2011. Available: [http://www.58bits.com/thesis/3-D\_Secure.pdf](http://www.58bits.com/thesis/3-D_Secure.pdf).

[^3]: S. J. Murdoch & R. Anderson, "Verified by Visa and MasterCard SecureCode: or, How Not to Design Authentication", _Financial Cryptography and Data Security_, vol. 10, pp. 25-28, Jan. 2010.