# Cloudable
High Performance Swift Models with Core Data and CloudKit synchronization

The Lessons of CloudCore:

- Operations are old school.  Who's managing all the threads?!
- implementation details are spread across code and Core Data model documents, tricky not to miss a detail!
- lots of type-blind API surfaces, leading to runtime errors

Based on the experiences of CloudCore, the goal of Cloudable is a re-imagination of Swift model structures, implemented via Swift Concurrency, Core Data, and CloudKit.

Cloudable is actually a set of modules:

Cloudable - handles synchronizing data between Core Data and CloudKit.  Works offline.  Works across Private, Shared, and Public databases.
Sharable - add support for sharing records or zones
Maskable - defines local-only and/or remote-only fields
Cacheable - handles background uploads and downloads of CKAssets, separate from CKRecord sync operations
Publicable - simple toggle to mirror a private CKRecord in the public database
