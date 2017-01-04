# ##################################################
# Repository:    MicroStrategy
# Sub Folder:    central_headers
#
# Description:   This sub folder contains 
#                
#                
#
# Modifications:
# Date         Modified By          Description
# ----------   ------------------   -------------------------
#
# ##################################################


# ##################################################
# Folder structure
# ##################################################
  - central_headers
    - header_template.html
      -- this file is a template for use in an HTML Container in a MSTR Document

# ##################################################
# HOW TO
# ##################################################
  1. Create MSTR Document to serve as the header (note the size!)
  2. Create MSTR Document (VI would work too)
  3. Add an HTML Container the same size as your document from step 1
  4. Paste the header_template.html contents into the HTML Container and update the URL appropriately
  5. Run the document and confirm everything loaded up OK

# ##################################################
# Version
# ##################################################
Currently written for MSTR v10.2

# ##################################################
# Reference
# ##################################################

https://lw.microstrategy.com/msdz/MSDL/940/docs/mergedProjects/websdk/topics/bestpract/BP_Define_page_layout.htm