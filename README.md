D287: Java Frameworks

C.  Customize the HTML user interface for your customer’s application. The user interface should include the shop name, the product names, and the names of the parts.
    mainscreen.html:
        Line 13: changed title to "The Straight Arrow"
        Line 15-71: Created CSS Styling for the page
        Line 74-82: Added Navigation Bar to top of page with Store Name and links to Home and About page.
        Line 83-86: Added breaks to increase space between nav bar and heading
        Line 88-89: Changed heading to "The Straight Arrow" and added smaller heading below it describing the store
        Line 90: Break between heading and horizontal rule
        Line 92: Changed heading to "Parts & Accessories"
        Line 124: Changed heading to "Bows
        
D.  Add an “About” page to the application to describe your chosen customer’s company to web viewers and include navigation to and from the “About” page and the main screen.
    Created about.html and added the following:
    Line 6-57: Created CSS Styling
    Line 60-68: Created Navigation Bar with link to Home(mainscreen.html) and an About (about.html) page
    Line 69: Added breaks to increase space between navigation bar and heading 
    Line 70-79: Added headings and paragraphs describing our mission and community involvement

E.  Add a sample inventory appropriate for your chosen store to the application. You should have five parts and five products in your sample inventory and should not overwrite existing data in the database.
    BootStrap.java:
        Line 37-144: Created 5 parts(Riser, Limb, Arrow, Release and Quiver) and set company names, inventory, minimum/maximum inventories, prices, names, and Ids for each
        Line 151-160: Created and saved 5 products including IDs, names, Prices, and inventory for each.
        Line 35: Created if statement that would only provide sample part inventory if the repository is empty
        Line 150: Created an if statement for products that will only provide the sample inventory if the repository is empty

F.  Add a “Buy Now” button to your product list. Your “Buy Now” button.
    mainscreen.html
        Line 156: Added Buy Now Button
    Created BuyProductController.java and added the following:
        Line 1-36: New controller added for Buy Now button on mainscreen.html
    Created confirmFailure.html and added the following:
        Line 5: Title Changed to "Purchase Failed"
        Line 6-56: CSS Styling
        Line 59-67: Navigation Bar added with links to Home and About Pages
        Line 69: Heading added describing that purchase was unsuccessful
    Created confirmSuccess.html and added the following:
        Line 5: title changed to "Purchase Successful"
        Line 6-56: CSS Styling
        Line 59-67: Navigation Bar added with links to Home and About Pages
        Line 69: Heading added describing that purchase was successful
        

G.  Modify the parts to track maximum and minimum inventory by doing the following:
    Part.java:
        Line 19-20: Added annotation for ValidMin and ValidMax
        Line 35-36: Created int values for minInv and maxInv
        Line 58-59: set minInv = 0 and maxInv = 100 in Part constructor
        Line 94-98: Created setters and getters for maxInv and minInv
        Line 121-128: Created validateLimits method
    InhousePart.java:
        Line 18-19: set values for minInv and MaxInv
    OutsourcedPart.java:
        Line 18-19: set values for minInv and MaxInv
    InhousePartForm.html:
        Line 26-30: Added minimum and maximum inventory input fields
    OutsourcedPartForm.html:
        Line 27-31: Added minimum and maximum inventory input fields
    PartServiceImpl.java
        Line 58: Called validateLimits method
    OutsourcedPartServiceImpl.java
        Line 52: Called validateLimits method
    InhousePartServiceImpl.java
        Line 52: Called validateLimits method
    
H.  Add validation for between or at the maximum and minimum fields. The validation must include the following:
    Created ValidMin.java and added:
        Line 1-25: Created a custom error message for when updated part inventory falls below set minimum
    Created MinValidator.java and added:
        Line 1-33: Created custom error message for when updated part inventory falls below set minimum
    Created Validmax.java and added:
        Line 1-36: Created custom error message for when updated part inventory is above set maximum
    Created MaxValidator.java and added:  
        Line 1-30: Created custom error message for when updated part invetory is above set maximum
    Part.java:
        Line 19-20: Added annotation for ValidMin and ValidMax
    Product.java
        Line 21: Added annotation for ValidEnufParts
    InhousePartForm.html:
        Line 32-36: Added list to display error message
    OutSourcedPartForm.html:
        Line 33-37: Added list to display error message
I.  Add at least two unit tests for the maximum and minimum fields to the PartTest class in the test package.
    PartTest.java
    Line 142-176: Two test set up to set/get minimum and maximum inventory values. 

J.  Remove the class files for any unused validators in order to clean your code.
    BootStrapData.Java:
        Line 4: Removed unused import Statement for Part class
        Line 9-12: Removed unused import statements for OutsourcedPartService, OutsourcedPartServiceImpl, ProductService, and ProductServiceImpl classes
        Line 17: Removed unused import statement for Optional
    AddInhousePartController.java: 
        Line 4, 7-8, 17: Removed unused import statements for Part, PartService, PartServiceImpl classed and requestParam annotation
    AddOutsourcedPartController.java:
        Line 3, 8-9,18: Removed unused import statements for InhousePart, PartService, PartServiceImpl classes and requestParam annotation
    AddPartController.java:
        Line 6, 12: Removed unused import statement for bindingResult and PartRepository
    MainScreenController.java:
        Line 5,6: Removed unused import statements for Part/ProductRepositories
    PartRepository.java
        Line 4: Removed unused import statement for Product class
    InhousePartService.java
        Line 4-5: Removed unused import statement for Part and OutsourcedPart
    InhousePartServiceImpl.java
        Line 4, 6: Removed unused import statement for OutsourcedPart and OutsourcedPartRepository
    OutsourcedPartService.java:
        Line 4: Removed unused import statement for part
    PartService.java
        Line 4: Removed unused import statement for product
    ProductService.java
        Line 3: Removed unused import statement for part
    ProductServiceImpl.java:
        Line 3, 5: Removed unused import statement for Part and Part repository
    DeletePartValidator.java
        Line 4: Removed unused import statement for product
    EnufPartsValidator.java:
        Line 9: Removed unused import statement for ValidEnufParts
    PriceProductValidator.java:
        Line 5-7: Removed unused import statements for InhousePartRepository, InhousePartServiceImpl, and ProductRepository
    ValidMax.java:
        Line 3: Removed unused import statement for MaxValidator