# utl-querying-github-repositories-and-working-around-github-limits
Querying github and working around github limits 
    %let pgm=utl-querying-github-repositories-and-working-around-github-limits;

    github
    https://tinyurl.com/3wxf8seh
    https://github.com/rogerjdeangelis/utl-querying-github-repositories-and-working-around-github-limits

    Querying github and working around github limits

    Create a listing of 1,974 repository names

    QUERY EXAMPLES

    I was not able to split the github api commands

    REPO NAMES THAT CONTAIN the string MAPPING

      gh api search/repositories --method=GET -F q="mapping" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h

    ALL 2023 Repository Names in file d:\txt\repos1.txt

      gh api search/repositories --method=GET -F q="rogerjdeangelis/utl created:2023-01-01..2023-12-31" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h | Tee-Object -FilePath "d:\txt\repos1.txt";

    REOSITORY NAMES with string rogerjdeangelis but NOT utl

     gh api search/repositories --method=GET -F q="rogerjdeangelis/ NOT utl" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h | Tee-Object -FilePath "d:\txt\30.txt"


    https://tinyurl.com/369caxcw
    https://docs.github.com/en/search-github/getting-started-with-searching-on-github/understanding-the-search-syntax#query-for-values-between-a-range


    AGENDA

          1. Install SCOOP command processor
          2. install github api
          3.list all my repos (over the 1.000 limit - limits 100 per page and 10 pages for 1000 search results

    /*           _               _
      ___  _   _| |_ _ __  _   _| |_
     / _ \| | | | __| `_ \| | | | __|
    | (_) | |_| | |_| |_) | |_| | |_
     \___/ \__,_|\__| .__/ \__,_|\__|
                    |_|
    */

    /*********************************************************************************************************************************/
    /*                                                                                                                               */
    /* GIT.GIT_010_REPOS total obs=1,974 22JUN2023:11:30:10                                                                          */
    /*                                                                                                                               */
    /*  REPO                                                                                                                         */
    /*                                                                                                                               */
    /*  https://github.com/rogerjdeangelis/-let-pgm-utl-create-sas-v5-transport-files-with-long-variable-names-in-the-label-field-   */
    /*  https://github.com/rogerjdeangelis/-utl-is-the-file-a-sas-v5-transport-or-a-cport-file-or-is-the-transport-file-corrupted    */
    /*  https://github.com/rogerjdeangelis/Calculate-more-accurate-standard-deviation-as-quarters-are-added                          */
    /*  https://github.com/rogerjdeangelis/Common-Format-and-MIME-Type-for-Comma-Separated-Values-CSV-Files                          */
    /*  https://github.com/rogerjdeangelis/CostReports                                                                               */
    /*  https://github.com/rogerjdeangelis/Create-a-single-sequence-of-negative-then-positive-numbers-centered-around-zero           */
    /*  https://github.com/rogerjdeangelis/Creating-command-macros-for-the_1980s-DMS-Classic-Editor                                  */
    /*  https://github.com/rogerjdeangelis/Dynamic_variable_in_a_DOSUBL_execute_macro_in_SAS                                         */
    /*  https://github.com/rogerjdeangelis/Elegant-simple-array-input-from-a-flatfile-by-Novinosrin                                  */
    /*  https://github.com/rogerjdeangelis/Export-exel-sheet-names-to-sas-dataset                                                    */
    /*  https://github.com/rogerjdeangelis/Fastest-method-to-determine-if-a-column-contains-any-duplicates                           */
    /*  https://github.com/rogerjdeangelis/How-to-create-a-table-to-hold-the-missing-value-count-for-multiple-columns                */
    /*  https://github.com/rogerjdeangelis/Median-of-all--maximum-payments-over-all-my-clients                                       */
    /*  https://github.com/rogerjdeangelis/SASweave                                                                                  */
    /*  https://github.com/rogerjdeangelis/SPDE-for-complex-indexing-and-table-scans-on-power-workstation                            */
    /*  https://github.com/rogerjdeangelis/SQL-change-character-date-to-formatted-numeric-date-without-a-rename-statement            */
    /*  https://github.com/rogerjdeangelis/Sorting-columns-of-a-table-in-place-in-a-SAS-dataset                                      */
    /*  https://github.com/rogerjdeangelis/Synthetic-CMS-Minimum-Data-Set-MDS-dataset-with-all-codes-and-decodes                     */
    /*  https://github.com/rogerjdeangelis/Utl-is-ds2-significantly-slower-that-pure-datastep-programming                            */
    /*  https://github.com/rogerjdeangelis/dedup-a-sorted-macro-list                                                                 */
    /*  https://github.com/rogerjdeangelis/distinct-counts-for_3200-variables-and_660-thousand-records-using-HASH-SQL-and-proc-freq  */
    /*  https://github.com/rogerjdeangelis/excel-how-do-I-remove-troublesome-characters-before-importing                             */
    /*  https://github.com/rogerjdeangelis/generate_50_million_alphanumeric_unique_keys                                              */
    /*  https://github.com/rogerjdeangelis/given_a_history_dataset_append_dates_from_daily_dataset_after_max_date_in_history         */
    /*  https://github.com/rogerjdeangelis/mySQL-uml-modeling-to-create-entity-diagrams-for-sas-datasets                             */
    /*  https://github.com/rogerjdeangelis/ods_excel_does_not_always_honor_start_at--bug                                             */
    /*  https://github.com/rogerjdeangelis/ods_rtf_mutiple_justifications_within_one_compute_block                                   */
    /*  https://github.com/rogerjdeangelis/python_importing_sas_dataset_with_505_columns_and_100_thousand_rows                       */
    /*  https://github.com/rogerjdeangelis/sasbcat                                                                                   */
    /*  https://github.com/rogerjdeangelis/ut_average_minimum_differences_for_all_pairs_of_variables_by_row                          */
    /*  https://github.com/rogerjdeangelis/utl-AI-compute-the-distance-between-objects-in-an-image-python                            */
    /*  https://github.com/rogerjdeangelis/utl-AI-first-name-and-birth-date-range-to-gender                                          */
    /*  https://github.com/rogerjdeangelis/utl-AI-geometry-is-the-figure-a-right-triangle-                                           */
    /*  https://github.com/rogerjdeangelis/utl-AI-internal-angles-of-polygon-from-vertex-coordinates-in-r                            */
    /*  https://github.com/rogerjdeangelis/utl-AI-labeling-centroids-inside-and-within-a-boundary-polygon                            */
    /*  https://github.com/rogerjdeangelis/utl-AI-remove-noise-from-an-image-python-opencv                                           */
    /*  https://github.com/rogerjdeangelis/utl-AI-spelling-corrector-when-word-is-close-to-the-correct-word                          */
    /*  https://github.com/rogerjdeangelis/utl-Bland-Altman-statistics_95-percent-limit-of-agreement                                 */
    /*                                                                                                                               */
    /*********************************************************************************************************************************/

    /*     _           _        _ _
    / |   (_)_ __  ___| |_ __ _| | |  ___  ___ ___   ___  _ __
    | |   | | `_ \/ __| __/ _` | | | / __|/ __/ _ \ / _ \| `_ \
    | |_  | | | | \__ \ || (_| | | | \__ \ (_| (_) | (_) | |_) |
    |_(_) |_|_| |_|___/\__\__,_|_|_| |___/\___\___/ \___/| .__/
                                                         |_|
    */

    Create restore point (just in case)

    INSTALL INSTRUCTIONS FOR SCOOP


    https://tinyurl.com/wv395drw
    https://computingforgeeks.com/install-applications-from-command-line-windows/

    start powershell from command line

    Set-ExecutionPolicy RemoteSigned -scope CurrentUser
    iex (new-object net.webclient).downloadstring('https://get.scoop.sh')

    Scoop was installed successfully!

    >scoop help

    S C:\Windows\system32> Set-ExecutionPolicy RemoteSigned -scope CurrentUser
    PS C:\Windows\system32> iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
    Initializing...
    Downloading ...
    Creating shim...
    Adding ~\scoop\shims to your path.
    Scoop was installed successfully!
    Type 'scoop help' for instructions.
    PS C:\Windows\system32> scoop help
    Usage: scoop <command> [<args>]

    Available commands are listed below.

    Type 'scoop help <command>' to get more help for a specific command.

    Command    Summary
    -------    -------
    alias      Manage scoop aliases
    bucket     Manage Scoop buckets
    cache      Show or clear the download cache
    cat        Show content of specified manifest.
    checkup    Check for potential problems
    cleanup    Cleanup apps by removing old versions
    config     Get or set configuration values
    create     Create a custom app manifest
    depends    List dependencies for an app, in the order they'll be installed
    download   Download apps in the cache folder and verify hashes
    export     Exports installed apps, buckets (and optionally configs) in JSON format
    help       Show help for a command
    hold       Hold an app to disable updates
    home       Opens the app homepage
    import     Imports apps, buckets and configs from a Scoopfile in JSON format
    info       Display information about an app
    install    Install apps
    list       List installed apps
    prefix     Returns the path to the specified app
    reset      Reset an app to resolve conflicts
    search     Search available apps
    shim       Manipulate Scoop shims
    status     Show status and check for new app versions
    unhold     Unhold an app to enable updates
    uninstall  Uninstall an app
    update     Update apps, or Scoop itself
    virustotal Look for app's hash or url on virustotal.com
    which      Locate a shim/executable (similar to 'which' on Linux)

    /*___      _           _        _ _         _                   _
    |___ \    (_)_ __  ___| |_ __ _| | |   __ _| |__     __ _ _ __ (_)
      __) |   | | `_ \/ __| __/ _` | | |  / _` | `_ \   / _` | `_ \| |
     / __/ _  | | | | \__ \ || (_| | | | | (_| | | | | | (_| | |_) | |
    |_____(_) |_|_| |_|___/\__\__,_|_|_|  \__, |_| |_|  \__,_| .__/|_|
                                          |___/              |_|
    */
    https://computingforgeeks.com/how-to-install-github-cli-on-linux-and-windows/


    scoop bucket add github-gh https://github.com/cli/scoop-gh.git
    scoop install gh

    PS C:\Windows\system32> scoop bucket add github-gh https://github.com/cli/scoop-gh.git
    >> scoop install gh
    Checking repo... OK
    The github-gh bucket was added successfully.
    Installing 'gh' (2.31.0) [64bit] from main bucket
    gh_2.31.0_windows_amd64.zip (9.7 MB) [========================================================================] 100%
    Checking hash of gh_2.31.0_windows_amd64.zip ... ok.
    Extracting gh_2.31.0_windows_amd64.zip ... done.
    Linking ~\scoop\apps\gh\current => ~\scoop\apps\gh\2.31.0
    Creating shim for 'gh'.

    'gh' (2.31.0) was installed successfully!

    PS C:\Windows\system32>

    /*____    _ _     _           _ _
    |___ /   | (_)___| |_    __ _| | |  _ __ ___  _   _   _ __ ___ _ __   ___  ___
      |_ \   | | / __| __|  / _` | | | | `_ ` _ \| | | | | `__/ _ \ `_ \ / _ \/ __|
     ___) |  | | \__ \ |_  | (_| | | | | | | | | | |_| | | | |  __/ |_) | (_) \__ \
    |____(_) |_|_|___/\__|  \__,_|_|_| |_| |_| |_|\__, | |_|  \___| .__/ \___/|___/
                                                  |___/           |_|
    */

    gh auth login

    ? What account do you want to log into?  [Use arrows to move, type to filter]
    ? Do you want to re-authenticate? (y/N) Y
    ? What is your preferred protocol for Git operations?  [Use arrows to move, type to filter]
    > HTTPS
      SSH
    HIT ENTER
    ? How would you like to authenticate GitHub CLI?
    HIT ENTER
    ! First copy your one-time code: 1234-5675
    Press Enter to open github.com in your browser...
    HIT ENTER
    WEB PAGE OPENS UP TO TYPE IN CODE
    HIT AUTORIZE
    ENTER PASSWORD
    CONGRATULATIONS

    GO BACK TO POWERSHELL

    PS $o=gh api search/repositories --method=GET -F q="utl-mapping" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h

    THESE ARE MY REPOS THAT CONTAIN "mappi"

    >> $o
    https://github.com/rogerjdeangelis/utl-reduce-your-sdtm-and-adam-mapping-effort-using-a-common-meta-data-model
    https://github.com/rogerjdeangelis/utl-cdisc-check-adam-table-mappings
    https://github.com/rogerjdeangelis/utl_binning_36_character_and_numeric_variables_with_separate_mappings
    https://github.com/rogerjdeangelis/utl-given-latitude-and-longitude-determine-the-us-state-mapping
    https://github.com/rogerjdeangelis/utl-enhanced-common-meta-data-model-to-reduce-CDSIC-mapping-efforts
    https://github.com/rogerjdeangelis/utl-mapping-clinical-terms-to-descriptions-for-a-large-number-of-vocabularies
    https://github.com/rogerjdeangelis/utl-using-binary-mappings-and-normailztion-to-simplify-an-N-percent-crosstab
    https://github.com/rogerjdeangelis/utl_define_a_mapping_to_verify_a_numeric_and_return_the_number_of_digits_in_a_string

    I HAD TO ENTER THE COMMAND BELOW ON ONE LINE

    CREATE A LISTING BY YEAR OF ALL PUBLIC REPOSITORES

    gh api search/repositories --method=GET -F q="rogerjdeangelis/utl created:2023-01-01..2023-12-31" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h | Tee-Object -FilePath "d:\txt\repos21.txt";
    gh api search/repositories --method=GET -F q="rogerjdeangelis/utl created:2022-01-01..2022-12-31" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h | Tee-Object -FilePath "d:\txt\repos22.txt";
    gh api search/repositories --method=GET -F q="rogerjdeangelis/utl created:2021-01-01..2021-12-31" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h | Tee-Object -FilePath "d:\txt\repos23.txt";
    gh api search/repositories --method=GET -F q="rogerjdeangelis/utl created:2020-01-01..2020-12-31" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h | Tee-Object -FilePath "d:\txt\repos24.txt";
    gh api search/repositories --method=GET -F q="rogerjdeangelis/utl created:2019-01-01..2019-12-31" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h | Tee-Object -FilePath "d:\txt\repos25.txt";
    gh api search/repositories --method=GET -F q="rogerjdeangelis/utl created:2018-01-01..2018-12-31" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h | Tee-Object -FilePath "d:\txt\repos26.txt";
    gh api search/repositories --method=GET -F q="rogerjdeangelis/utl created:2017-01-01..2017-12-31" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h | Tee-Object -FilePath "d:\txt\repos27.txt";
    gh api search/repositories --method=GET -F q="rogerjdeangelis/utl created:2016-01-01..2016-12-31" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h | Tee-Object -FilePath "d:\txt\repos28.txt";
    gh api search/repositories --method=GET -F q="rogerjdeangelis/utl created:2015-01-01..2015-12-31" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h | Tee-Object -FilePath "d:\txt\repos29.txt";

    gh api search/repositories --method=GET -F q="rogerjdeangelis/ NOT utl" --jq ".items[].html_url" -F per_page=100 --paginate --cache 1h | Tee-Object -FilePath "d:\txt\30.txt"


    filename txt (
    "d:/txt/repos21.txt"
    "d:/txt/repos22.txt"
    "d:/txt/repos23.txt"
    "d:/txt/repos24.txt"
    "d:/txt/repos25.txt"
    "d:/txt/repos26.txt"
    "d:/txt/repos27.txt"
    "d:/txt/repos28.txt"
    "d:/txt/repos29.txt"
     );

    libname git "d:/git";

    data git.git_010_repos(label="List of all Roger DeAngelis Repositories");
      length repo $384;
      infile txt;
      input;
      repo=_infile_;

    run;quit;

    proc sort data=git.git_010_repos (label="List of all Roger DeAngelis Repositories") nodupkey;
    by repo;
    run;quit;

    NOTE: The data set GIT.GIT_010_REPOS has 1974 observations and 1 variables.

    /*              _
      ___ _ __   __| |
     / _ \ `_ \ / _` |
    |  __/ | | | (_| |
     \___|_| |_|\__,_|

    */

    data _null_;
    file "d:/git/git_010repos.txt";
    set git.git_010_repos;
    put repo;
    run;quit;
