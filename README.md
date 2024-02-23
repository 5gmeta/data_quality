# Data Quality

This module needs to be deployed inside a pipeline in the MEC platform.
This modules reads cits/cam data from each dataflow and assigns to each dataflow publishing a quality value from 1 to 7.    
This value is set in the "quality" property in the dataflowdb.    
A quality of 0 means that the dataflow has not published enough messages to be evalued.

## Example execution

```
docker run -e AMQP_ADDRESS=<ip>:><port> -e AMQP_USERNAME=<username> -e AMQP_PASSWORD=<password> -e AMQP_TOPIC=cits-large \
-e DB_ADDRESS=<5gmeta-cloud-db-ip>:<port> -e DB_USERNAME=<db-username> -e DB_PASSWORD=<db-password> -it --rm 5gmeta/data-quality
```

## Authors

* Federico Princiotto ([federico.princiotto@linksfoundation.com](mailto:federico.princiotto@linksfoundation.com))
* Francesco Aglieco ([francesco.aglieco@linksfoundation.com](mailto:francesco.aglieco@linksfoundation.com))

## License

Copyright : Copyright 2022 LINKS

License : EUPL 1.2 ([https://eupl.eu/1.2/en/](https://eupl.eu/1.2/en/))

The European Union Public Licence (EUPL) is a copyleft free/open source software license created on the initiative of and approved by the European Commission in 23 official languages of the European Union.

Licensed under the EUPL License, Version 1.2 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at [https://eupl.eu/1.2/en/](https://eupl.eu/1.2/en/)

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.