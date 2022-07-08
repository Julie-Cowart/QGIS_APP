# qgis_salt_app_041021

## Install directions
1. Clone repo
1. `cd qgis_salt_app_041021`
1. `python3 -m venv venv`
1. `source venv/bin/activate`
1. setup db
    1. install postgres and postgis extension
    1. get datafiles from Pinki Mondal or Julie Cowart
    1. install into db with 
    `raster2pgsql -I -C -M -t 50x50 "Kent_2013.tif" -F | psql -d postgres -U postgres -h localhost` and repeat with Kent_2017.tif (this is slow)
1. run server with `python manage.py runserver`
