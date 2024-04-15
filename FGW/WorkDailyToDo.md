# Do to list and other useful info

Links for Markdown documentation:
- https://www.markdownguide.org/basic-syntax/
- https://www.markdownguide.org/extended-syntax/



## ⛴️ FGW 2.0

### 🗓️ 05.01
*Notes:*

69785002 - FGW1 reservation with pet
70030822 - FGW2 with everything


### 🗓️ 08.01
Questions:
- [x] Pet category missing from FGW1 RecallBooking response (only added to costDetails PET ON BOARD)
- [x] Pet ID and vehicle ID come our own FGW generated?
- [x] FGW2-8 How should we find contact person
- [x] FGW2-8 Make sure that we need to take first city or return null from clientFragment
- [x] FGW2-8 Vehicle code vs operatorCode: *Lead vehicle code as assigned by Ferrygateway association. One of Code or OperatorCode must be supplied, if both are supplied the OperatorCode will be used.*

From Ekaterina
- [x] Request with multiple vehicles (trailers)

Tasks:
- [x] FGW2-8 Add Lead vehicle to FGW response



<br/>

### 🗓️ 09.01
- [x] FGW2-8 Refactor carDeck.toVehicle

<br/>

### 🗓️ 11.01
- [x] FGW2-8 Finish up with Contact details

### 🗓️ 12.01
- [x] FGW2-8 Start adding Jacoco Unit tests


### 🗓️ 17.01
- [x] FGW2-8 Continue with unit tests
- [x] FGW2-8 Merge Svetlana branch with mine

### 🗓️ 18.01
- [x] FGW2-8 Continue with unit tests


### 🗓️ 22.01
- [x] FGW2-8 Look into Igor code review changes
- [x] FGW2-8 Map out exactly what has been implemented

</br>

### 🗓️ 23.01
- [ ] FGW2-8 Add unit tests for test coverage
- [x] Split task into multiple subtasks:
    - Add error handling to RecallBooking
        - Connected to the Messages to the RecallBooking response
    - Add ContactDetails to the RecallBooking response
    - Add Passengers to the RecallBooking response
    - Add Vehicles to the RecallBooking response
    - Implement FerryComponents fully in the the RecallBooking response
    - Add Context to the RecallBooking response
    - Add Pets to the RecallBooking response
    - Add TPE to the RecallBooking response
    Will we implement QrCode 
    - Add QrCode to the RecallBooking response

### 🗓️ 25.01
- [x] FGW2-7 Fix where Client object is taken - should be from contacts
- [x] Get full unit test coverage
- [x] Remove false .ignoringFields from RecallWebBookingTest
- [x] Add Endpoint test

### 🗓️ 26.01
- [x] Code review with Igor
- [x] FGW2-39 Implement missing fields for contact person

### 🗓️ 29.01
- [x] FGW2-39 Refactor unit test and TestDataDSL
- [x] FGW2-39 Fix Tests

### 🗓️ 30.01
- [x] FGW2-40 Questions about Vehicles
- [x] FGW2-39 Test if all fields are correct
- [x] FGW2-39 Test ISO mapping
- [x] FGW2-39 TypeKey to enum

### 🗓️ 31.01
- [x] FGW2-40 Add enum class for length and height to vehicle code and operatorCode
- [x] FGW2-40 Add vehicleCodes logic to response 
- [x] FGW2-40 Increase carDeck test coverage
- [x] FGW2-39 Fix ClientFragmentExtTests
- [x] FGW2-39 Fix RecallWebBookTests

### 🗓️ 01.02
- [x] FGW2-8 Implement enpoint test for RecallBooking

### 🗓️ 02.02
- [x] FGW2-38 Add test for invalid referenceId and bookingNotFound
- [x] FGW2-40 Add ID to vehicles and add valid logic

### 🗓️ 08.02
- [x] FGW2-42 Increacse CreateBookInputService coverage
- [x] FGW2-42 Increacse and refactor PassengerBookTypeExt coverage
- [x] FGW2-42 Add test for BookRequestExt??? - *needs to be deleted, not used*
- [x] FGW2-42 Add test for ReturnedRequestTypeExt - *needs to be deleted, not used*
- [x] FGW2-42 Increase SailingBookRequestTypeExt coverage

### 🗓️ 09.02
- [x] FGW2-42 Increase ContactDetailsTypeExt coverage -> kahtlane
- [x] FGW2-42 Increase IdentityCategoryTypeExt coverage


### 🗓️ 13.02
- [x] FGW2-45 Create successful reservation with CAR inside SW
- [x] FGW2-45 Write out logic flow of adding a car and what are restrictions of FGW and of SW


### 🗓️ 14.02
- [x] FGW2-45 Add basic vehicle logic
- [x] FGW2-45 Add SailLeg logic

### 🗓️ 15.02
- [x] FGW2-45 Increase test coverage to green
- [x] FGW2-45 Add tests for VehicleTypeExt 
- [x] FGW2-45 Add tests for CarDeckExt 
- [x] FGW2-45 Add tests for CreateBookInputService


### 🗓️ 16.02
- [x] FGW2-45 Look if triple can be made to model
- [x] FGW2-45 Validate with team vehicle passenger logic

### 🗓️ 19.02
- [x] FGW2-45 Add passenger to the vehicle
- [x] FGW2-45 Roundtrip logic for vehicles
- [x] FGW2-45 Add AllVehicles to SailingsBookResponseType
- [x] FGW2-45 Add VehicleRefs to SailingsBookResponseType

### 20.02
- [x] FGW2-45 Error "vehicle refs should be defined when isAllVehicles is false"
- [x] FGW2-45 Validation for VehicleRef to match with VehicleType.id
- [x] FGW2-45 Add message if code is defined - unnsuported, use operatorCode

RECallbooking car id mapping

### 21.02
- [x] FGW2-45 What happens when heigth is 1
- [x] FGW2-45 Why height and length are by default null
- [x] FGW2-45 Increase test coverage to have mid-commit
- [x] FGW2-45 Extra validation if no operatorcode, height and length are given
- [x] FGW2-45 Add operatorCode to model from common
- [x] FGW2-45 When outward has vehicle and return has allVehicles false, will then just vehicle not be added?
- [x] FGW2-45 Add IsVehicleAvailable to SailingsBookResponseType
- [x] FGW2-45 Create mapping of heigth and length to operatorCode


### 22.02
- [x] FGW2-45 Validation when code is wrong and operatorCode missing
- [x] FGW2-45 Look into what happens when Vehicles or Vehicle is null - why not saying exactly what is missing

### 27.02
- [x] FGW2-45 BookInputService increase test coverage to remove @Generated annotation

### 29.02
- [x] Ask what tasks are not done in list?

### 07.03
- [x] FGW-667 Find where the difference comes in with correct sail



### Overall Questions

### UNDONE:
- [ ] FGW2-42 Update the endpoint test content
- [ ] FGW2-42 Increase Common test coverage (when Vehicle logic is finalized)
- [ ] FGW2-42 Increase ClientFragmentExtTest coverage

<br/>


#### Big questions about FGW2-8

**Business**  

*vehicles* 
- [x] Do we need "CODE" in FGW or use straight SW OperatorCode
- [x] Vehicles Trailers

Pet classification added under SW addons

**Technical**

[ ] - How should error handling look like?


<br/>

**Missing**
- Error handling for no reservation
- Error handling for some other reservation (GraphQl) issues
- Comments under https://jira.fleet.zone/projects/FGW2/issues/FGW2-8?filter=myopenissues
- BookResponseLinks missing 
- Some fields in vehicles (Question about FGW code), hire car, BikeOnBack, RoofLoad, Make, Model, FuelType, width
- Missing trailer from response (how should be used?)


### Different reservations for testing

#### SW DEV 270
- 70306901 (with one car)
- 70306902 (car withoud licencePlate)

#### Unknown
- 70030822 - Pets
- 70306648 - has vehicles Lead and Trailer 
- 498 - Client with full address fields
- 70306731 - some Svetlanas
- 70359795
- 70306844
- 70306701 - in FGW1

error 200 vs 400