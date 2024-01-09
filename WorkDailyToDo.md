# Do to list and other useful info

Links for Markdown documentation:
- https://www.markdownguide.org/basic-syntax/
- https://www.markdownguide.org/extended-syntax/



## ⛴️ FGW 2.0

#### 05.01
*Notes:*

69785002 - FGW1 reservation with pet
70030822 - FGW2 with everything


#### 08.01
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

### 09.01
- [ ] FGW2-8 Add Trailers to FGW response
- [ ] FGW2-8 Refactor carDeck.toVehicle
- [ ] FGW2-8 Finish with the endpoint test content

Questions:  
- [ ] Do we need "CODE" in FGW or use straight SW OperatorCode

<br/>

### 10.01
- [ ] FGW2-8 Handle case where booking is not found
- [ ] FGW2-8 Add BookResponseLinks to FGW response


<br/>


household - should look active, look primary address
- also mobile number from there too
- mobile number with international code

Pet classification added under SW addons