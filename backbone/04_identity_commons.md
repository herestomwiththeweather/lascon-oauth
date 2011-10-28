!SLIDE
# Dwolla OAuth API

!SLIDE bullets
# Dwolla API
* [Get a Token](https://www.dwolla.com/developers/authentication)
* [Use a Token](https://www.dwolla.com/developers/endpoints/accountapi/send)

!SLIDE center
![Dwolla](oauth-dwolla.png)

!SLIDE commandline incremental
# Make a payment #

    $ export DWOLLA_OAUTH2_TOKEN=abcdefghijklmnopqrstuvwxyz
    $ export DWOLLA_PIN=1234
    $ irb
    $> load "dwolla_pay.rb"
    $> r = Dwolla.new.send('herestomwiththeweather@gmail.com',1)
    $> txn_id = JSON.parse(r.body)['SendResult']


