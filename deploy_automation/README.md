# ##################################################
# Repository:    MicroStrategy
# Sub Folder:    deploy_automation
#
# Description:   This sub folder contains various components of the deployment automation scripts
#                This includes database scripts for table creation, inserts, updates, etc.
#                as well as MicroStrategy files such as .scp (Command Manager), .mmp (Object Manager), & .smw (System Manager)
#
# Modifications:
# Date         Modified By          Description
# ----------   ------------------   -------------------------
#
# ##################################################


# ##################################################
# Folder structure
# ##################################################
  - deploy_automation
    - deployment
        -- this folder contains the folder structure to use on the server this is deployed to
        -- All files within this folder are required.
      - package
        -- all .mmp (Object Manager) packages will be stored / archived here
      - log
        -- contains a log for each deployment
      - undo
        -- each .mmp file will have an undo .mmp file stored here for rollback purposes
      - template
        -- houses script templates used by the System Manager .smw file
      - temp
        -- temporary file staging directory (for cleanliness)
    - setup
      - db_script
        -- contains the database create table statements required for the metadata base
      - env
        -- contains the env file to be stored in C:\env on the server running System Manager
      - package
        -- contains all project packages for the MSTR Deployments project
        -- these need to be manually deployed to get the project up and running

# ##################################################
# Installation / Set Up
# ##################################################
  The initial setup steps (1-3) are just installing MicroStrategy and getting the project source setup
  1. Install MicroStrategy System Manager & Command Manager & Desktop Developer on the WINDOWS machine
  2. Create a LDAP or Windows AD user in MicroStrategy (so no password required)
  3. Create the project source with the proper parameters and authentication method
  ----------
  The next steps are specific to the deployment automation
  4. Create folder C:\env and copy \setup\env\mstrenv.scp to there (on Windows Utility Server)
    i.  be sure to update the values in mstrenv.scp based on your environment and requirements
    ii. if already using this file from another process, merge appropriately
  5. Copy deployment folder to desired location on Windows Server
  6. Execute db_script on the database to create the tables
  7. Deploy the .mmp packages from ..\setup\package and update the db connection
  8. Test everything out

