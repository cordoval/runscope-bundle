##CordovalRunscopeBundle

Require it with composer:

```cli
composer require cordoval/runscope-bundle dev-master
```

Add to your kernel:

```php
new Cordoval\RunscopeBundle\CordovalRunscopeBundle(),
```

Add to your config:

```yml
cordoval_runscope:
    bucket_key: secretKeyHere
    auth_token: secretTokenHere
    gateway_host: ~ # runscope.net
    target_api: https://api.github.com
```

Now you can use the guzzle client as follows:

```php
$client = $this->get('cordoval_runscope.guzzle.client');
$response = $client->get('/')->send();
echo $response->getBody();
```

##Acknowledgements

I thank the Lord Jesus Christ for motivating this wretched man.