# Updating the description of a trigger in {{ serverless-containers-name }}

{% list tabs %}

- Management console

   1. In the [management console]({{ link-console-main }}), select the folder containing your trigger.
   1. Open **{{ serverless-containers-name }}**.
   1. On the left-hand panel, select ![image](../../_assets/functions/triggers.svg) **Triggers**.
   1. Select the trigger whose description you want to update.
   1. In the upper-right corner of the page, click **Edit**.
   1. Edit the description and click **Save**.

- CLI

   {% include [cli-install](../../_includes/cli-install.md) %}

   {% include [default-catalogue](../../_includes/default-catalogue.md) %}

   {% include [trigger-list-note](../../_includes/serverless-containers/trigger-list-note.md) %}

   To update the trigger description, run this command:

   ```
   yc serverless trigger update <trigger_name> --description "<trigger_description>"
   ```

   Result:

   ```
   id: a1sfe084v4**********
   folder_id: b1g88tflru**********
   created_at: "2022-12-04T08:45:31.131391Z"
   name: my-trigger
   description: My trigger for mail.
   rule:
     mail:
       email: a1s8h8avgl**********-cho1****@serverless.yandexcloud.net
       invoke_container:
         container_id: bba5jb38o8**********
         service_account_id: aje03adgd2**********
         retry_settings:
           retry_attempts: "1"
           interval: 10s
   status: ACTIVE
   ```

- API

   To update a trigger description, use the [update](../triggers/api-ref/Trigger/update.md) REST API method for the [Trigger](../triggers/api-ref/Trigger/index.md) resource or the [TriggerService/Update](../triggers/api-ref/grpc/trigger_service.md#Update) gRPC API call.

{% endlist %}
