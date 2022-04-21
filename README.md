# Gearing-Calculator
This project is a web based Gearing Calculator that provides a vehicle's engine RPM at a given speed using road speed, tire size, and gear ratios within the drivetrain as inputs. 

The current production version is implemented here: https://toledo-cars.com/gearing-calculator 

The core of this project is a Javascript function defined as GRtoRS(). The GRtoRS() function uses the following variables generated from the user's entered values from the corresponding HTML inputs: 
  1. "FirstR" is the variable used to represent the ratio used by first gear in the vehicle's transmission;
  2. "SecondR" is the variable used to represent the ratio used by second gear in the vehicle's transmission;
  3. "ThirdR" is the variable used to represent the ratio used by third gear in the vehicle's transmission;
  4. "FourthR" is the variable used to represent the ratio used by fourth gear in the vehicle's transmission;
  5. "FifthR" is the variable used to represent the ratio used by fifth gear in the vehicle's transmission;
  6. "SixthR" is the variable used to represent the ratio used by sixth gear in the vehicle's transmission;
  7. "TCR" is the variable used to represent the ratio used by the transfer case in the vehicle;
  8. "FDR" is the variable used to represent the ratio used by the vehicle's axles (often called a final drive ratio). 
  9. "TD" is the variable used to represent the diameter of the vehicle's driven wheels and tire assembly in inches; and 
  10. "RS" is the variable used to represent the road speed used to calculate engine RPMs according to the vehicle's gearing. 

The GRtoRS() function stores the following variables as statically defined mathematical formulas: 
  1. "Circumference" is the variable used to represent the circumference of vehicle's driven wheel and tire assembly in feet by using the TD variable as an input;
  2. "FPM" is the variable used to represent the road speed used for calculation in feet per minute by using the RS variable as an input;  
  3. "TireRPM" is the variable used to represent the RPM of the vehicle's wheel and tire assembly at the road speed used for calculation by using the "FPM" and "Circumference" variables as inputs; 
  4. "FirstRPM" is the variable used to represent the vehicle's engine RPM at the road speed used for calculation assuming the vehicle is in first gear by using the "TireRPM", "FDR", "TCR", and "FirstR" variables as inputs:
  5. "SecondRPM" is the variable used to represent the vehicle's engine RPM at the road speed used for calculation assuming the vehicle is in second gear by using the "TireRPM", "FDR", "TCR", and "SecondR" variables as inputs; 
  6. "ThirdRPM" is the variable used to represent the vehicle's engine RPM at the road speed used for calculation assuming the vehicle is in third gear by using the "TireRPM", "FDR", "TCR", and "ThirdR" variables as inputs;
  7. "FourthRPM" is the variable used to represent the vehicle's engine RPM at the road speed used for calculation assuming the vehicle is in fourth gear by using the "TireRPM", "FDR", "TCR", and "FourthR" variables as inputs;
  8. "FifthRPM" is the variable used to represent the vehicle's engine RPM at the road speed used for calculation assuming the vehicle is in fifth gear by using the "TireRPM", "FDR", "TCR", and "FifthR" variables as inputs; and
  9. "SixthRPM" is the variable used to represent the vehicle's engine RPM at the road speed used for calculation assuming the vehicle is in sixth gear by using the "TireRPM", "FDR", "TCR", and "SixthR" variables as inputs. 

The GRtoRS() function is called by a HTML button following the HTML form allowing for the user to input. When called, the GRtoRS() function uses the variables generated from user inputs to output the following back to HTML for display to the user: 
  1. The "RS" variable with text and an image indicating that it is the vehicle's road speed; 
  2. If the "TCR" variable is less than or eqaul to 1, a text string and image indicating that the vehicle's transfer case is in high range, else a text string and image indicating that the vehicle's transfer case is in low range; 
  3. The "FirstRPM" variable with text and an image indicating the vehicle's engine RPM in that gear;  
  4. The "SecondRPM" variable with text and an image indicating the vehicle's engine RPM in that gear;  
  5. The "ThirdRPM" variable with text and an image indicating the vehicle's engine RPM in that gear;  
  6. The "FourthRPM" variable with text and an image indicating the vehicle's engine RPM in that gear;  
  7. The "FifthRPM" variable with text and an image indicating the vehicle's engine RPM in that gear;  and
  8. The "SixthRPM" variable with text and an image indicating the vehicle's engine RPM in that gear. 

After user feedback and testing, it was discovered that users desired the ability to have the form automatically populate based on known vehicle configurations. Accordingly, additional HTML select inputs were added to allow known values to be automatically populated into the form that calls the GRtoRS() function. This allows ease of use for the user while retaining the ability to customize the inputs as needed. 

After testing in the client's website, it was discovered that the GoDaddy website builder was altering the display of the code in a manner inconsistent with the design. Accordingly, the HTML portion of the code was arranged into a table with a responsive width of 100% in order to correct display issues. 

The project's versions 1 through 4 were used for internal and beta testing. Version 5 was attempted to be implemented for the client, however display issues prevented the desired graphical representation and the client was finally presented with and approved the current version 6.  
