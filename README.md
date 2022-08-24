# solutions-html-editors

Reusable HTML Editors for Labelbox

This respository has one folder for each custom HTML editor for Labelbox.  

### Editor List
#### eRetailer Shopping Cart Comparison

This HTML editor allows a labeler to easiy compare two shopping cart listings side by side to determine if they pertain to the same product in their product catalog.  The side by side comparison makes the structure of two listings identical, eliminating any labeler bias in judgement that may confuse when two listings are for the same product.  

Configured by providing a JSON payload that dynamically generates the listing. 

#### Design Considerations: 
  
  - Designed to work within the core Labelbox editor capabilities, no app hosting required
  - HTML Template does not require dev of a custom editor
  - No external libraries or vulerabilities required
  - Easy to concatenate creating one HTML file per data row during pre-processing
  - Supports dynamic number of carousel images or listing detail: JSON drives dynamic HTML content
  - Responsive design allows flexible screen sizing to lay inside Labelbox Editor
  - Can be secured if necessary by whitelisting the stable IP for your workforce team

 
#### How to create a datarow for html editor and upload to Labelbox
  1. Edit the listings variable on line 39 with two listings 
  2. Go to Labelbox Catalog and create a new dataset via the UI
  3. Click "Choose files to upload" and upload the .html file 
  4. In Annotate, click "+ new project" and for "Type of data to be labeled" select "Text"
  5. In the project, click "Queue data for labeling" and select the datarow(s) and then "Send data row" as a batch to project

 
#### Testing Locally on a Mac
  1. Download single html file to your machine
  2. Open Terminal. 
  3. Navigate to folder with HTML file
  4. Start a web server at command line with 'python -m http.server'
  5. Open browser to localhost:8000 
  
### More Editors to come!
