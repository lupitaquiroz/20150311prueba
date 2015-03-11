// require codebird
require_once('/path/to/codebird_php_v2.4.1/codebird.php');
 
\Codebird\Codebird::setConsumerKey("your_ConsumerKey", "your_ConsumerSecret");
$cb = \Codebird\Codebird::getInstance();
$cb->setToken("your_AccessToken", "your_AccessTokenSecret");
 
$params = array(
  'status' => 'Auto Post on Twitter with PHP http://goo.gl/OZHaQD #php #twitter'
);
$reply = $cb->statuses_update($params);




$reply = $cb->statuses_update('status=Whohoo, I just tweeted!');





$reply = $cb->statuses_update('status=' . urlencode('Fish & chips'));
// will result in this:
$reply = $cb->statuses_update('status=Fish+%26+chips');







$params = array(
    'status' => 'Fish & chips'
);
$reply = $cb->statuses_update($params);





$params = array(
    'status' => 'I love London',
    'lat'    => 51.5033,
    'long'   => 0.1197
);
$reply = $cb->statuses_update($params);




$params = array(
    'screen_name' => 'jublonet'
);
$reply = $cb->users_show($params);


