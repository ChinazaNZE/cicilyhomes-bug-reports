# Bug Report: CSP & Console Errors

**Date:** 4th November 2026  
**Reporter:** Chukwuemeka Nze (Frontend Engineer)  
**Platform:** https://cicilyhomes.com  
**Severity:** Low – Medium  
**Status:** Open  

## 1. Summary
Two console errors were detected on the live website using Chrome DevTools.

## 2. Errors Found

### Error 1: Content Security Policy (CSP) Violation
- **Blocked Resource:** `https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js.map`
- **Reason:** Violates CSP directive `connect-src 'self'`

### Error 2: Uncaught Promise Error
- **Message:** A listener indicated an asynchronous response by returning true, but the message channel closed before a response was received

## 3. Evidence

![CSP and Console Errors](../assets/screenshots/csp-console-error.png)

## 4. Impact
- Low impact on normal users
- Creates unnecessary console noise
- Source map is blocked (affects debugging)

## 5. Recommended Actions
- **Frontend:** Investigate Swiper source map request and the uncaught promise error
- **Backend:** Confirm whether a Content-Security-Policy header is being set from the server (Hostinger)

## 6. Status Checklist
- [ ] Frontend investigation completed
- [ ] Backend CSP confirmation
- [ ] Fix applied
- [ ] Verified on live site
