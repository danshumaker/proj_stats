# proj_stats
* Author: Dan Shumaker 
* LICENSE: MIT
* Created: 2011

# Description
  Generate File size statistics for a project. It generates SQL code that will have file sizes, lines of code, file name, extension, and file type printed out for each file in the source directory given.

  The SQL code can then be loaded into MySQL (Sequel Pro) for browsing and investigating purposes.  This quickly lets you view the statistics for lines of code in a project.
  By exporting the statistics into a MySQL database it makes it more versitile than an Excel spreadsheet or a text file in my opinion.

# USAGE:
    Example 1. This will run the script, output the SQL commands to the XXMY_PROJ.sql file, then load that file into the my_db database in mysql - this is the one stop shop

    ```
    proj_stats -l XXMY_PROJ.sql ; mysql -uroot -proot my_db < XXMY_PROJ.sql
    ```

# DEFAULTS:

## Command Line Options
    --help            : Print help
    --ignore          : Specify the types of files to ignore. default= NONE
    --directory       : The Directory to analyze. default to current working directory
    --verbose         : print verbose output. default off
    --logfile         : Put the statistics in this logfile
    --table           : Files Sizes Table Name.  default='PROJ_STATS_FILE_SIZES' )
    --query-table     : Twenty largest MYSQL tables table name", default='PROJ_STATS_MYSQL_TABLE_SIZES
    --extension-table : Extension File Table Name.  default=PROJ_STATS_FILE_SIZES_BY_EXTENSION
    --type-table      : Type File Table Name.  default= PROJ_STATS_FILE_SIZES_BY_TYPE
    --quiet           : Do NOT print process output. default off
