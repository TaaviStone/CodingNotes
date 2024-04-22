## FGW SCHEMA VALIDATION ERRORS

1. Field "CODE" is missing
2. If passenger references wrong (too much or wrong REF)

</br>

## FGW OWN EXCEPTIONS
 
- If field "Time" is missing
   - ```<Message Code="321" Description="Required field missing. Custom description: OnBoardMealService Time is required." Severity="Recoverable"/>```

- If field "FacilityCode" is missing
    - ```<Message Code="321" Description="Required field missing. Custom description: OnBoardMealService FacilityCode is required." Severity="Recoverable"/>```

- If no matcing dining is found from availableDinings
    - ```<Message Code="14" Description="No suitable services found. Custom description: No matcing OnBoardMealService is found." Severity="Recoverable"/>```

</br>

## SW EXCEPTIONS MAPPING

- getAvailableDinings gives no dinings - do not know exact error message❓
    - ```<Message Code="14" Description="No suitable services found. Custom description: no available OnBoardMealService is found." Severity="Recoverable"/>```

- *Facility MYSTAR BUFsFET is not found on the Ship MYSTARs* 
    - ```<Message Code="320" Description="Invalid value. Custom description: FacilityCode X is invalid." Severity="Fatal"/>```

- *Sitting information is not found for Starting Time 11:00:00 of
Dining Facility MYSTAR BUFFET*
    - ```<Message Code="14" Description="No suitable services found. Custom description: Sitting information is not found for Starting Time X of FacilityCode X." Severity="Recoverable"/>```