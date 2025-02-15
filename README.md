# Caching Issue with next/server MetadataRoute in Next.js 13 middleware

This repository demonstrates a caching issue encountered when using the `next/server` API's `MetadataRoute` in a Next.js 13 middleware function.  The issue involves the middleware failing to respect cache headers set within the `headers` property, leading to inconsistent caching behavior.

## Problem Description
The provided `Metadata.js` file contains a middleware function that attempts to set a `Cache-Control` header. Despite this, the cache control is not respected and unexpected caching behavior is observed. This issue is specific to Next.js 13 and its new `next/server` API.

## Solution
The `MetadataSolution.js` file demonstrates a potential solution by using the `next/headers` API which provides more reliable cache control mechanisms within Next.js Middleware.