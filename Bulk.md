# GAM Bulk

#### Determining How Many GAM Commands Run In Parallel
>Windows DOS Shell:

      set GAM_THREADS=10

>Windows PowerShell:

      $env:GAM_THREADS=10

>Linux / OSX:

      export GAM_THREADS=10

#### Format

    gam csv <csv-filename> gam <regular command>

    gam batch <batch-filename>

#### Pipe Command

    gam print users query "orgUnitPath='/<OrganizationalUnit>'" | gam csv - gam update user ~primaryEmail imap off
