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

### 🗓️ 05.02
- [ ] VehicleRefs
- [ ] FGW2-8 Valid payload, namespace
- [ ] FGW2-40 Increase Common test coverage (when Vehicle logic is finalized)
- [ ] FGW2-39 Increase ClientFragmentExtTest coverage

Questions  
- Do all LeadVehicleType values need to be implemented from schema?
- What will do with the FGW code
- Now will not take phone from household but from mobilephone?

### UNDONE:
- [ ] FGW2-8 Look how current developments work with legacy responses from DB
- [ ] FGW2-8 Look into problems raised by Igor
- [ ] FGW2-8 Add Trailers to FGW response
- [ ] FGW2-8 Add BookResponseLinks to FGW response
- [ ] FGW2-8 Add FGW_PET classification to PET
- [ ] FGW2-8 Finish with the endpoint test content

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

- 70030822 - Pets
- 70306648 - has vehicles Lead and Trailer 
- 498 - Client with full address fields
- 70306731 - some Svetlanas
- 70359795

70306844

- 70306701 - in FGW1

error 200 vs 400