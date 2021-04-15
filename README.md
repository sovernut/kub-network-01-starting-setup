
# kub-network-01-starting-setup
**Note**
* Pods internal communication
  * use [localhost](https://github.com/sovernut/kub-network-01-starting-setup/commit/d7f2c7af451f995df70166b0042af39882e876b4) to communicate in Pods
* Between Pods communication examples..
	* use `ClusterIP` in service and use its address (in environment variable) ([commit](https://github.com/sovernut/kub-network-01-starting-setup/commit/a842de65c8a53f094746b003c87b9a79c76d82aa))
	* use {SERVICE_NAME}_SERVICE_HOST Environment variable ([commit](https://github.com/sovernut/kub-network-01-starting-setup/commit/e9072deb9fbc04fce1995bf0a47700695c74b299))
	* use CoreDNS feature by "{SERVICE_NAME}.{NAME_SPACE} ([commit](https://github.com/sovernut/kub-network-01-starting-setup/commit/06eae5e207be80bc02ef9791f28c4e715fe7a763))
* adding FrontEnd
	* when calling tasks-api set url to `/api/tasks` because we will using reverse proxy ([commit](https://github.com/sovernut/kub-network-01-starting-setup/commit/39095483fee2c24522999612ef8ed71e4e3fdc71#diff-4e185b456927ee5c9781afdfbd5054b8cfb34c5b099a169c2bab8c822931625c))
	* set config reverse proxy to auto-generated domain name with port define in service ([commit](https://github.com/sovernut/kub-network-01-starting-setup/commit/39095483fee2c24522999612ef8ed71e4e3fdc71#diff-5d44530dae9808283dd9c2bcdfe420fbcfc1155265e3dad7bc6e4993fb466143))
