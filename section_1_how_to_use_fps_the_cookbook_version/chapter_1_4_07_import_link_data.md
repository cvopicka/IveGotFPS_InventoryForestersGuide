# Chapter 1.4.07 - Import / Link Data

While there may be several FPS ways to do this process, it is best to stick with the basic methods outlined here as they are based on the MS Access software and will work regardless of security updates.

This process is MS Office version dependent. Please choose your version to continue.

## Importing in MS Office 2000 - 2003

- *File*
  - *Get External Data*
    - *Import*
      - Change *Files of type* at the bottom of the window.
      - Navigate to the file of interest
      - Select the file
      - Click *Import*

## Linking in MS Office 2000 - 2003

- *File*
  - *Get External Data*
    - *Import*
      - Change *Files of type* at the bottom of the window.
      - Navigate to the file of interest
      - Select the file
      - Click *Link*

## Importing MS Office 2007+ (Ribbon)

- *External Data*
  - Select your filetype. Be aware that other file types are listed under the *More* menu item.
    - *Browse* to the file of interest.
      - *Open*
    - Select
      - *Import tables, queries, forms, reports, macros, and modules into the current database.*
      - **Or**
      - *Link to the data source by creating a linked table.*
    - OK

__NOTE__

With the release of MS Access 2016, the user is no longer able to use DBase or DBF files. Access no longer supports this format directly.

A possible method of mitigation at the time of publishing is to use MS Excel. There has been some limited success consuming DBF files with Excel directly then saving into another format such as Excel or text/CSV.
