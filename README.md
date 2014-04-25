Content Providers Lab 
=====================================

Week 8 lab. This lab deals with ContentProviders, and uses a CursorLoader to access data from the content provider.

It is the same UI as last week, but this week the Place Badges are stored in an SQLite database as the ContentProvider. There are actually two projects in the Skeleton files this week. The `ContentProviderLabContentProvider` is the definition of the ContentProvider for the lab, and needs to be run in the background for the lab to work. The `ContentProviderLabUser` is the application with the Activities that the user interacts with. 

In `PlaceViewAdapter.java` the CursorLoader is defined that handles the places. The methods I added to were
* swapCursor()
* add()
* removeAllViews()

In `PlaceViewActivity.java` the following functions had to be defined because this class implemented the `LoaderCallbacks<Cursor>` interface (making it a CursorLoader). The callback methods defined were:
* onCreateLoader()
* onLoadFinished()
* onLoaderReset()

The other functions in this file dealing with location contained code copied over from the Locations lab.
