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
    - deploy
      - db_script
        -- contains the database create table statements required for the metadata base
      - env
        -- contains the env file to be stored in C:\env on the server running System Manager
      - package
        -- contains all project packages for the MSTR Deployments project
        -- these need to be manually deployed to get the project up and running
