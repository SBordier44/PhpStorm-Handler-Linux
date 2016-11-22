# Linux Tools And Tips

## PhpStorm Handler for Ubuntu/Debian users

    sudo cp phpstorm-url-handler /usr/bin/phpstorm-url-handler
    sudo desktop-file-install phpstorm-url-handler.desktop
    sudo desktop-update-database
    
#### Usage

It can be used to open files at the specified line from within the browser by 
placing a link of the following kind in the markup:
    
    <?php
    $file = "/path/to/filename.php";
    $line = 35;
    print "<a href="phpstorm://open?file=$file&line=$line">Open with PhpStorm</a>";
    ?>
    
#### Commandline usage

    FILE="/path/to/filename.php"
    LINE=35
    /usr/bin/env phpstorm-url-handler "phpstorm://open?file=${FILE}&line=${LINE}"
    
#### XDebug

    xdebug.file_link_format="phpstorm://open?file=%f&line=%l"
