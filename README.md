# AJAXPhotoGallery

* When a user clicks on any one of the photo links, 
the corresponding photo shall show up. 
But behind the scene, there are two possibilities: 

	* (1) the photo (image) is available but hidden. 
In this case, the click simply makes the photo visible, 
and at the same time you check the readiness of the two photos 
before and after the photo link being clicked on. 
If they are ready to show (loaded), do nothing more; 
if they are not ready/loaded, asynchronously request the photos from the server 
and load into the browser (integrated into the page). 

	* (2) The photo being clicked on is not available. 
In this case, get it from the server through a synchronous request, 
and display it, and then do the same as above for preparing the 2 
neighboring photos (i.e., check their availabilities and 
asynchronously request them from server if unavailable).