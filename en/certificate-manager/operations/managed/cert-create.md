# Adding a Let's Encrypt certificate

You can use a certificate from {{ certificate-manager-name }} in the [specified](../../concepts/services.md) {{ yandex-cloud }} services only.

To add a new Let's Encrypt [certificate](../../concepts/managed-certificate.md):

{% list tabs %}

- Management console

   1. In the [management console]({{ link-console-main }}), select the [folder](../../../resource-manager/concepts/resources-hierarchy.md#folder) to add a certificate to.
   1. In the list of services, select **{{ certificate-manager-name }}**.
   1. Click **Add certificate**.
   1. In the menu that opens, select **Let's Encrypt certificate**.
   1. In the window that opens, enter a name for the certificate in the **Name** field.
   1. (Optional) In the **Description** field, enter a description for the certificate.
   1. In the **Domains** field, list the domains to issue a certificate for.
   1. Select the [type of check for domain rights](../../concepts/challenges.md): `DNS` or `HTTP`.
   1. Click **Create**.

- CLI

   {% include [cli-install](../../../_includes/cli-install.md) %}

   {% include [default-catalogue](../../../_includes/default-catalogue.md) %}

   1. View a description of the command:

      ```bash
      yc certificate-manager certificate request --help
      ```

   1. Run the following command:

      ```bash
      yc certificate-manager certificate request \
        --name mymanagedcert \
        --domains example.com
      ```

      Where:
      * `--name`: Certificate name.
      * `--domains`: Certificate domains.

      Command result:

      ```bash
      id: fpq6gvvm6piuegbb2nol
      folder_id: b1g7gvsi89m34qmcm3ke
      created_at: "2020-09-15T08:49:11.533771Z"
      ...
      - example.com
      status: VALIDATING
      updated_at: "2020-09-15T08:49:11.533771Z"
      ```

- API

   To add a certificate, use the [requestNew](../../api-ref/Certificate/requestNew.md) REST API method for the [Certificate](../../api-ref/Certificate/) resource or the [CertificateService/RequestNew](../../api-ref/grpc/certificate_service.md#RequestNew) gRPC API call.

{% endlist %}

A new certificate appears in the certificate list with the `Validating` status. This status means that a Let's Encrypt certificate was requested and you need to pass the [domain rights check](cert-validate.md) to process it.