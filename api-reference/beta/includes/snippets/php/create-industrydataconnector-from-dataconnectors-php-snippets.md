---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\IndustryData\AzureDataLakeConnector;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AzureDataLakeConnector();
$requestBody->setOdataType('#microsoft.graph.industryData.azureDataLakeConnector');
$requestBody->setDisplayName('CSV connector');
$additionalData = [
	'sourceSystem@odata.bind' => 'https://graph.microsoft.com/beta/external/industryData/sourceSystems(\'aa050107-5784-4a8e-1876-08daddab21bc\')',
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->external()->industryData()->dataConnectors()->post($requestBody)->wait();

```