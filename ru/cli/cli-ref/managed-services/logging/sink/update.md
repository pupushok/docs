---
editable: false
sourcePath: en/_cli-ref/cli-ref/managed-services/logging/sink/update.md
---

# yc logging sink update

Update log sink

#### Command Usage

Syntax: 

`yc logging sink update <SINK-NAME>|<SINK-ID> [Flags...] [Global Flags...]`

#### Flags

| Flag | Description |
|----|----|
|`--id`|<b>`string`</b><br/>Sink id.|
|`--name`|<b>`string`</b><br/>Sink name.|
|`--new-name`|<b>`string`</b><br/>New sink name.|
|`--description`|<b>`string`</b><br/>New sink description.|
|`--labels`|<b>`key=value[,key=value...]`</b><br/>List of label KEY=VALUE pairs to replace existing labels.|
|`--service-account-id`|<b>`string`</b><br/>New service account ID|
|`--s3`|<b>`PROPERTY=VALUE[,PROPERTY=VALUE...]`</b><br/>New storage sink parameters<br/><br/>Possible property names:<br/><ul> <li><code>bucket</code>:     Specifies storage bucket</li> <li><code>prefix</code>:     Specifies prefix for storage objects</li> </ul>|
|`--yds`|<b>`PROPERTY=VALUE[,PROPERTY=VALUE...]`</b><br/>New yds sink parameters<br/><br/>Possible property names:<br/><ul> <li><code>stream-name</code>:     Specifies stream name</li> </ul>|
|`--async`|Display information about the operation in progress, without waiting for the operation to complete.|

#### Global Flags

| Flag | Description |
|----|----|
|`--profile`|<b>`string`</b><br/>Set the custom configuration file.|
|`--debug`|Debug logging.|
|`--debug-grpc`|Debug gRPC logging. Very verbose, used for debugging connection problems.|
|`--no-user-output`|Disable printing user intended output to stderr.|
|`--retry`|<b>`int`</b><br/>Enable gRPC retries. By default, retries are enabled with maximum 5 attempts.<br/>Pass 0 to disable retries. Pass any negative value for infinite retries.<br/>Even infinite retries are capped with 2 minutes timeout.|
|`--cloud-id`|<b>`string`</b><br/>Set the ID of the cloud to use.|
|`--folder-id`|<b>`string`</b><br/>Set the ID of the folder to use.|
|`--folder-name`|<b>`string`</b><br/>Set the name of the folder to use (will be resolved to id).|
|`--endpoint`|<b>`string`</b><br/>Set the Cloud API endpoint (host:port).|
|`--token`|<b>`string`</b><br/>Set the OAuth token to use.|
|`--impersonate-service-account-id`|<b>`string`</b><br/>Set the ID of the service account to impersonate.|
|`--format`|<b>`string`</b><br/>Set the output format: text (default), yaml, json, json-rest.|
|`-h`,`--help`|Display help for the command.|
