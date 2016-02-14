# GenieACS Juju Charm

To deploy GenieACS through Juju:

    $ juju deply cs:~zaidka/trusty/genieacs-0

Then deploy the database (MongoDB) and cache (redis) engines and link them:

    $ juju deploy mongodb
    $ juju deploy redis
    $ juju add-relation mongodb genieacs
    $ juju add-relation redis:master genieacs

To expose GenieACS ports:

    $ juju expose genieacs
