---
sidebar_position: 2
---

# create

The [create page](https://playground.everything.dev/create) on the playground allows you to interact with the everything sdk's main methods directly.
These methods can be found in [@everything-sdk-js/sdk](https://github.com/near-everything/everything-sdk-js/tree/main/packages/sdk) package.

## create thing

:::caution

An everything account must be connected in order to interact with this method.

:::

To create a thing, type or create an attribute under "select attributes". A new thing only requires one attribute and it's value to be provided -- this creates a characteristic that defines a thing.
Once an attribute and value has been entered, select the storage (currently only supports "cloud") and click submit.

The method will run and a response will be generated. If successful, then a UUID representing a thingId will be returned.
This thingId will be used for the other methods.

## create media

:::caution

An everything account must be connected in order to interact with this method.

:::

To create media, either select "camera" to take a picture or interact with the input to select or drag and drop your photos.
Then, select the storage. Cloud will save the image to an Amazon S3 bucket while blockchain will save the image to [Arweave](https://www.arweave.org/).
Paste the thingId into the input that you want the provided images to be associated with then click submit.

The method will run and a response will be generated. If successful, then a list of urls representing the image references will be returned.
No further action is necessary, the images have been associated with the thing.

## mint thing

:::caution

A NEAR wallet must be connected in order to interact with this method.

:::

To mint a thing, paste the thingId into the input that you want minted and click submit.

This will redirect you to a page where you must approve the mint.

If successful, then you will be redirected back to the playground.
No further action is necessary, a reference of the thing has been minted on chain.
