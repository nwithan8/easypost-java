# CHANGELOG


## NEXT RELEASE

* Removes `items` and `containers` which have not been supported for some time
* Corrects references of `contact@easypost.com` to `support@easypost.com`
* Updates the connection timeout to 30 seconds from 20 and the request timeout to 60 from 40


## 4.0.4 2020-10-29

* Actually bump User-Agent (which hadn't been bumped since 4.0.0)


## 4.0.3 2020-10-26

* Change `PUT` requests to be properly-encoded
* Handle null previous_attributes


## 4.0.2 2020-03-30

* Merged pull request #49
* Added EvenTest file
* Fixed test cases on EasyPostTest (testPickup, testShipmentWithPostageLabelWithOptions )
* Fixed intermittent WebHook callback event containing "previous_attributes": null


## 4.0.1 2018-08-28

* Add labelFile for postage_label_inline option


## 4.0.0 2018-03-15

* Added additional fields to Error object used in Address verification
* Added delivery details to Address verification
* Changed message field of ShipmentMessage to support non-string values
* Fixed currency field of Rate to handle null
* Fixed Report params to include start_date and end_date in the top-level JSON, as expected by the reports endpoint


## 3.4.1 2018-03-09

* Added createdAt, updatedAt and fees fields on all top-level objects
* Added batchId to Shipment objects


## 3.4.0 2017-12-07

* Updated version of junit from 4.1.10 to 4.1.12
* Updated version of maven-compiler-plugin from 1.5 to 1.8
* Added tests for new shipment option payment


## 3.3.5 2017-05-23

* Added orderId field to Shipments
* Allow Reports to be retrieved without passing a type


## 3.3.4 2017-03-10

* Updated X-EasyPost-Client-User-Agent to X-Client-User-Agent
* Added additional values to CarrierDetail
* Added statusDetail field to Trackers and TrackingDetails


## 3.3.3 2017-02-14

* Added newRates method to Orders to refresh rates


## 3.3.2 2017-01-24

* Allow Webhook update and index to be called with empty params


## 3.3.1 2017-01-19

* Fixed ScanForm create


## 3.3.0 2017-01-17

* Added basic CRUD methods for Webhooks


## 3.2.1 2017-01-09

* Fixed bug in Maven test dependencies


## 3.2.0 2017-01-04

* Changed Shipment and Order options from being a Map<String, String> to Map<String, Object> to support new non-string options


## 3.1.0 2016-12-14

* Added ability to create, retrieve, and index shipment, tracker and payment_log reports


## 3.0.5 2016-11-21

* Added delete() to Users (for children only)


## 3.0.4 2016-10-12

* Added getbatchId() and other methods to ScanForms


## 3.0.2 2016-08-30

* Added getCreatedAt() and getUpdatedAt() methods for Tracker objects


## 3.0.1 2016-08-19

* Removed some CRUD methods that are not (and never were) valid


## 3.0.0 2016-07-25

* Updated version of GSON from 2.2.4 to 2.7 to allow looser parsing of DateTime formats


## 2.2.7 2016-07-25

* Added standalone insurance objects


## 2.2.6 2016-07-22

* Allow the connection's read timeout to be set with EasyPost.readTimeout


## 2.2.5 2016-07-08

* Allow shipment_id to be null on rates


## 2.2.4 2016-03-09

* Bump version for deployment reasons


## 2.2.3 2016-06-27
* Updated POM.xml to fit Maven better and support the correct plugins
* Removed a flaky text


## 2.2.2 2016-03-09

* Updated PickupRate to properly include the carrier field


## 2.2.1 2016-03-02

* Updated Order Messages to be of the new, more descriptive format


## 2.2.0 2016-02-25

* Added "confirmation" field to ScanForm object, along with appropriate accessor methods
* Update Address verification errors array


## 2.1.9 2016-02-08

* Added ability to create new top-level users without API KEY


## 2.1.8 2016-01-26

* Added a Form attribute - submittedElectronically.


## 2.1.7 2016-01-19

* Fixed some types on the User object so that they match what is returned by the API (Number -> String).
* Added support for the new "verify" and "verify_strict" parameters for Address creation/validation.


## 2.1.6 2015-12-21

* Fixed Shipment Insure method so that it correctly uses http POST.


## 2.1.5 2015-11-19

* Added createList method to Tracker class


## 2.1.4 2015-09-24

* Added CarrierDetail object to tracker model.


## 2.1.3 2015-07-31

* Added Rate.listRate and Rate.listCurrency.


## 2.1.2 2015-07-08

* Added Carrier field to the tracker model.


## 2.1.1 2015-06-19

* Added Form model and Shipment.forms.


## 2.1.0 2015-04-15

* Added User model, and filled out CarrierAccount to be able to interact with
both via the API.


## 2.0.14 2015-04-08

* Updated Tracker model to have weight, signedBy and estDeliveryDate fields


## 2.0.13 2015-04-07

* Fixed Address createAndVerify method
* Added Address verifyWithCarrier and createAndVerifyWithCarrier methods


## 2.0.12 2015-03-03

* Added Pickup classes and pickup create, buy, cancel methods


##= 2.0.11 2015-03-03

* Orders now update themselves after a buy call.


== 2.0.10 2015-01-27

* Added Address.residential attribute, and Batch.buy function


## 2.0.9 2014-12-22

* Added a number of new Rate attributes and Batch.numShipments, Batch.reference, ScanForm.status


## 2.0.8 2014-12-18

* Added ShipmentMessage type for Shipment.messages


## 2.0.7 2014-11-04

* Added Tracker to shipment buy response
* Added Tracking Locations to Tracking Details
* Enhanced Tests


## 2.0.6 2014-07-28

* Added Container, Item, Order resources.
* Added Batch.createScanForm function for generating manifests from a batch.
* Refactored and added a lot of new attributes for objects across the board.


## 2.0.5 2013-12-11

* Bug fix. Made Batch.status public and removed the conflicting getStatus method.


## 2.0.4 2013-10-14

* Added Event resource for webhook digestion.
* Changed Batch.getStatus to Batch.getBatchStatus to avoid collisions with Tracker.getStatus in Event deserialization.


## 2.0.3 2013-08-28

* Bug fix: Fixed handleAPIError to return proper exception message.


## 2.0.2 2013-08-02

* API Addition: Tracker resource added. Trackers can be used to register any tracking code with EasyPost webhooks.
* Attribute Addition: Added new BatchStatus attribute, and additional label format attributes to PostageLabel.


## 2.0.1 2013-07-05

* Added unique carrier/service combination serviceCodes to Rate objects.
* Added function to Address to all creating and verifying at the same time.
* Add label function to Shipment to request specific label file_formats (pdf, epl2, zpl).
* Add insure function to Shipment. Add insurance to any shipment in one call!
