# tdjr-range-utils

Implementation of basic numeric Range functionality

## Range and Bounds
A _Range_ consists of numeric values bounded by two limiting values referred to as _Bounds_.  
The two _Bounds_ are generally referred to the _Lower Bound_ and the _Upper Bound_.  

_Ranges are cmmonly used to define a valid range of values against which other values can be validated based on whether they fall within the range_  

### Bounds Inclusion/Exclusion
A Bound's value can be participate in the Range in two ways:  
  *Inclusionary* - in this case the Bound's value is included within the range  
  *Exclusionary* - in this case the Bound's value sets the Limit to the range but is not included  
   
  #### examples
      Assume a _Range_ with a _Lower Bound_ of 5 and an _Upper Bound_ of 10, often expressed [5..10] or [5:10]  
        
          If the Lower Bound is *Exclusionary* and the Upper Bound is *Inclusionary*  
              then any number greater than 5 AND less than or equal to 10 is within the Range  
                
          If the Lower Bound is *Inclusionary* and the Upper Bound is *Exclusionary*  
              then any number equal to or greater than 5 AND less than 10 is within the Range  
                
          If the Lower Bound is *Exclusionary* and the Upper Bound is *Exclusionary* 
              then any number greater than 5 AND less than 10 is within the Range  
                
          If the Lower Bound is *Inclusionary* and the Upper Bound is *Inclusionary*  
              then any number equal to or greater than 5 AND equal to or less than 10 is within the Range  
   
 ## To use:  
  Require/Import range-helper  
      `const rangeHelper = require('<relativePath'/range-helper)`   
  Use a range-helper function to create a range  
      `const rangeFrom6To100 = createRangeHelper(6, true, 100, false)`  
  Check if your value is within the range  
      `const myValue = 100`   
      `const isInRange = rangeFrom6To100.isInRange(myValue)`  
      
