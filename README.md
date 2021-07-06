# Oracle APEX Plug-In: Bootstrap Carousel Extension

A carousel/slideshow is used to cycle through elements. A plugin to display images as a responsive slideshow. Special thanks to **Farzad Soltani** for his **bootstrap image carousel plugin**, that will add a bootstrap carousel with three images (static), but this plugin (**Bootstrap Carousel Extension**) will render a bootstrap carousel region based on query output (dynamic) and changing the slides can be controlled via left and right arrow keys.

Demo Application: https://apex.oracle.com/pls/apex/f?p=133110:9999::BRANCH_TO_PAGE_ACCEPT::9999:P9999_APP_PAGE_REDIRECT:8

# Prerequisite:

**DB versions:**	12.1.0.1,12.2.0.1,18.4.0.0,19.0.0.0.0,19.2.0.0.19,21.0.0.0.0,21.1.0.0.0,21.1.0.0.1

**APEX versions**	20.1.0.00.13,20.2.0.00.20,21.1.0

# Installation:

Export plugin file **"region_type_plugin_orclking_bootstrap_carousel_extension.sql"** from source directory and import it into your application.

# Steps to Achieve:

**Step 1:** Export a script **"Script to Populate Sample Data.sql"** from directory and compile it in your schema.

**Step 2:** Create a new blank page.

**Step 3:** Export plugin file **"region_type_plugin_orclking_bootstrap_carousel_extension.sql"** from Source directory and import it into your application.

**Navigation:** Shared Components ==> Plug-ins ==> Import

![image](https://user-images.githubusercontent.com/85283603/121812264-46bf0e00-cc78-11eb-842e-3e1c5671d978.png)

Plugin will be listed under plug-ins bucket after successful installation.

![image](https://user-images.githubusercontent.com/85283603/124363841-e1df4e00-dc4e-11eb-8429-9833897f3479.png)

**Step 4:** Create a region to the page. Change region type to **Bootstrap Carousel Extension [Plug-In]**.

![image](https://user-images.githubusercontent.com/85283603/124364165-b6f5f980-dc50-11eb-8ff3-8780924d27c7.png)

**Step 5:**  Construct Oracle SQL query and copy and paste it in region SQL Query section.

![image](https://user-images.githubusercontent.com/85283603/124364176-cbd28d00-dc50-11eb-97bb-129bbc51456b.png)

**Query Template:**

    SELECT 1 slide_key,
    
           'https://image.com/01' slide_url
              
      FROM dual
              
     WHERE 1 = 1;
        
       
**Sample Query to Render a Report:**

**Note:** Populate sample data by exporting a script **"Script to Populate Sample Data.sql"** from directory and compile it in your schema.

    SELECT document_id slide_key,
                     
           file_url slide_url
    
    FROM fxgn_documents
  
    ORDER BY sequence_no ASC;

**Step 6:** Set region template **"Blank with Attributes"**.

![image](https://user-images.githubusercontent.com/85283603/124364233-2c61ca00-dc51-11eb-8a6e-ff00c0b455b8.png)    
 
 **Step 7:** Fill required attributes
 
![image](https://user-images.githubusercontent.com/85283603/124619944-1ee35480-de8a-11eb-98d8-f4dc007ed2ca.png)
 
 **Output:** Then you output would display like this,
 
 ![image](https://user-images.githubusercontent.com/85283603/124620036-2e629d80-de8a-11eb-9330-23727ed3de1d.png)
 
Note: This pugin will support for **all language applications**. Please give a try.
  
That's it.

Happy APEXing!!!...

# References:

1) https://www.w3schools.com/bootstrap/bootstrap_carousel.asp

2) https://apex.world/ords/f?p=100:710:7163073110843::::P710_PLG_ID:COM.JAFR.BOOTSTRAP.CAROUSEL
