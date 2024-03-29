---
sidebar_position: 2
---

# Create a Type

A Type is used to describe the data model for a SKU. Konfig uses Types to generate forms for an LOM to make live updates. Types also help developers validate data that is returned from [Konfig's CDN](/reference/cdn).

:::danger Before you dive into creating your first type!
**Configuring a Type should come after you have decided what the data model for
your SKUs should be.** It is up to your client's code to properly handle the data
model described in a Type. It is imperative that you think about what
:::

In this tutorial we will re-create a simple transaction product type.

### 1. Navigate to the Type Tab

Click on the **Type** tab in the top-left corner.

![Type Tab](/img/type-tab.png)

### 2. Create & Name your Type

Click on the **Create Type** button.

![Create Type Button](/img/create-type-button.png)

Provide a name and description for your type and click **Save**.

![Name your Type](/img/name-your-type.png)

### 3. Add [Fields](/reference/field/what-is-a-field)

Once you click **Save** you will be redirected to a page to create your type. Click the **Add Field** button.

![Add Field Button](/img/add-field-button.png)

Click **Text**.

![Add Text Field](/img/add-text-field.png)

Fill out your name and check **This field is the title of this Type** and any
relevant field-level validations. In this case we want the **SKU Name** to be
required and unique amongst all SKUs of the type. When a field is marked as the
**title** of a [Type](/reference/type), Konfig will use the value of the field to identify SKUs
of this Type in the dashboard.

![Add Text Field Button](/img/add-text-field-button.png)

Congrats you have created your first Field! Now add a Field for the price of our product. Click **Add Field** again but this time select **Number**.

![Add Number Field](/img/add-number-field.png)

Fill out a name and check the **Required** box to make sure that our field is never empty. We also want to specify a minimum value of `0` because we never want our product to be offered at a negative price. Once you are done, click **Add**.

![Add Number Field Button](/img/add-number-field-button.png)

Now our transaction product has the fields **SKU Name** and **Price**. Lets now setup [Content](/reference/content/what-is-content) for our game so we can create a [Content Field](/reference/field/types/content)
