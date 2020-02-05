Instaurant - Final Project of CSE438

Team Member: 
Chengyue Gong, chengyueg@wustl.edu
Junji Heng, heng.junji@wustl.edu
Pengqiu Meng, mengp@wustl.edu
Tiancheng He, tiancheng712@gmail.com
Zifan Wan, zifan.w@wustl.edu


Installation guide 
1. The Pod files are not included in the folder due to the large size of them. It is necessary to "cd" into the project folder and run "pod install".
2. The app is developed on Xcode 10.1 so that there might be some conflicts with Xcode 9.4. Please compile and run on Xcode 10.1.
3. Since this app needs to run on an iPhone and the Firebase is involved, there might be tricky to have it run on your own iPhone.

For your convenience, we leave an unsigned version for you to test. The Bundle ID provided has not been registered so that you can sign by selecting your own team. And this bundle ID has already been registered on the Firebase.

If you encounter any problems when running our app, please do not hesitate to email us. We can help you by, for example, setting the new bundle ID on the firebase and sending you a new GoogleService-Info.plist so that you can access our database.
4. To test our app, you have to find a real restaurant which could be found in Yelp. Other kinds of business other than restaurants work as well, like Washington University Campus Store. It might be easier for you to look for nearby businesses in Yelp app at first to ensure your target business exists in Yelp. You can use any photo you like to test (it should be 2D).

Guidance for Instaurant
AR Camera
(1) Scan: the app will scan the storefront with the camera, and try to match it with the restaurants in our database.
(2) Match: if we have that restaurant in our database, the app will pop up some label with the restaurant's info and you can get more info after clicking on the 'Detail' button.
(3) See details: in detail, you can see info from Yelp.

Add a Restaurant
(1) Add: if we don't have that restaurant, you can create a new one in our database. Just click the '+' button. Since we don't have much in our database, in most cases you need to create one on your own.
(2) The procedure is simple. Fill in the form and click on 'Submit' button:
You need to provide all the following information to be able to submit a new restaurant.
	* name, location, yelp business: you have to provide information about the name and the location of the restaurant to choose a yelp business from possible restaurants. If there is no yelp restaurant for your input, we can't create one for now.
	* photo and its physical size: Then you need to upload a photo of its storefront and the physical width of the photo for later matching. The physical width is the real size of the width of your photo. The unit is meter.
(3) Scan again: now you can scan again in the AR camera

Add to Favorites
In the detail page, you can add/remove the restaurant to/from your favorite list by clicking on the "follow" button on the top right corner. Then you can see the detail of your favorite restaurant by click on the row in the Favorites view.


Development Detail
1. Our database is in Firebase. In fact we use three libraries to fulfill our needs to store and query, including Firestore for restaurants information, Cloud Storage for photos and GeoFirestore for queries based on latitude and longitude. 
All our requests are asynchronous. In addition, to increase the downloading speed of the size of photos, we also minimalize each phto to less than 1MB.

2. Almost all the features listed in our project proposal are implemented. However, some are dismissed with careful consideration.
There are some differences between the appearences of our real app and the wireframe. For example, the reviews are not included in our app since we think it is not appropriate to use the Yelp reviews in our own app. If the users want to see the reviews, the "Read more on Yelp" button is available and after clicking on it the app will be directed to a Yelp webpage. 


Enjoy yourself!
