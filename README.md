# Firebase Snapshot Existence Check Error

This repository demonstrates a common error when working with Firebase document snapshots: attempting to access properties before verifying the document's existence using `snapshot.exists`.  This can lead to unexpected runtime errors. The `bug.js` file shows the problematic code, while `bugSolution.js` provides the corrected implementation.

**Problem:** The asynchronous nature of Firebase operations often leads developers to access snapshot data prematurely.  If the document doesn't exist, accessing its properties will throw an error.

**Solution:** Always check `snapshot.exists` before accessing any properties of the document snapshot. This ensures that your code handles cases where the document might not be found gracefully.

This example uses JavaScript, but the principle applies to other Firebase SDKs.