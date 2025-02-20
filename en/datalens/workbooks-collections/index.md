# Workbooks and collections {{ datalens-short-name }}


Workbooks and collections are a new way to store objects in {{ datalens-short-name }}, which is alternative to the old navigation across folders. This new approach allows you to place {{ datalens-short-name }} objects in special containers:

* A **workbook** stores [connections](../concepts/connection.md), [datasets](../concepts/dataset/index.md), [charts](../concepts/chart/index.md), and [dashboards](../concepts/dashboard.md).

   {% cut "Workbook" %}

   ![image](../../_assets/datalens/workbook.png =800x450)

   {% endcut %}

* A **collection** is a container used for grouping workbooks and other collections.

## Features of the new approach {#features}

Workbooks make it much easier to work with objects:

* They allow you to consistently [set up permissions](./security.md) to linked objects: connections, datasets, charts, and dashboards.
* With them, you can set up permissions for [user groups](../../iam/operations/groups/create.md).
* You can copy workbooks maintaining the integrity of internal links and making their copies independent of the original.
* You can group workbooks into collections.

## How to enable workbooks and collections {#enable-workbooks}

To get started with workbooks:

1. Go to the [service settings]({{ link-datalens-settings }}).
1. Under **Workbooks**, click **Enable workbooks**.

   {% note info %}

   To enable workbooks, a user must have the `{{ roles-datalens-admin }}` role. They can do this only if a {{ datalens-short-name }} instance is deployed at the [organization](../concepts/organizations.md) level.

   {% endnote %}

To transfer any object from a folder to a workbook, perform [migration](./migrations.md).



