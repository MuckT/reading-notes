# class-13 reading notes

## [Quizlet Terms TODO](https://quizlet.com/)

### [THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS](http://diveinto.html5doctor.com/storage.html)

### Before Local Storage

* Cookies predate Local Storage; however, they have downsides:

  * Cookies are included with every HTTP request

  * Cookies are limited to about 4 KB of data

* Precursors to Local Storage - Most of these solutions were either specific to a single browser, or required third party plugins.

  * Microsoft userData

    * Limited to 64KB by default, with a max size of 640KB for trusted domains

  * “Flash cookies”

    * 100 KB of data per domain

    * Prompts the user for each order of magnitude increase in data storage (1 Mb, 10 Mb, ...)

  * Google Gears

    * An API to an embedded SQL database based on SQLite

## Local Storage Details

* Has 5MB of Storage space on the devices hard drive

* A way for web pages to store named key/value pairs locally

* Calling `localStorage.setItem("key", data)` with a named key that already exists will silently overwrite the previous value.

* Calling `localStorage.getItem("key")` with a non-existent key will return `null` rather than throw an exception.

* Calling `localStorage.removeItem("key")` with a non-existent key will do nothing.

* Calling `localStorage.length` will return the number of keys in the localStorage for that origin domain.

* Calling `localStorage.clear()` will clear the localStorage for that origin domain.

* `“QUOTA_EXCEEDED_ERR”` is the exception thrown if the 5MB storage limit is exceeded.

* Data is stored as strings. Will likely need to be coerced it yourself when you retrieve it.

  ```JavaScript
  // Sample localStorage usage
  const data = {
    name: "Sample Data",
    data: {
      array1: [1, 2, 3,],
      object1: {
        name: "Nested Deep",
        nested: [1, 2, 3]
      }
    }
  }
  localStorage.setItem("data", JSON.stringify(data));
  let retrievedData = JSON.parse(localStorage.getItem("data"));
  console.log(retrievedData)
  ```
  
### Alternatives to local Storage - Likely used to store more than 5MB

* [PouchDB](https://pouchdb.com/)

* [JsStore](https://jsstore.net/)

* [IndexDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API)

* [Local Forage](https://localforage.github.io/localForage/)

* [IDB-Keyval](https://www.npmjs.com/package/idb-keyval)
