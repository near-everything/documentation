---
sidebar_position: 4
---

# transact

The [transact page](https://playground.everything.dev/transact) on the playground allows you to transact on sample marketplaces.

:::caution

Both an everything account and a NEAR wallet must be connected in order to interact with this feature.

:::

The dashboard is broken down into 4 sections:
  
  1. **personal inventory:** shows a user's owned things. This data is associated with the everything account and supplemented by the NEAR wallet.
  2. **personal market:** a representation of a user's personal market. This market only shows products that the connected user owns and has listed.
  3. **ecosystem market:** a representation of a market within the everything ecosystem. From the drop down, you can select sample marketplaces that represent exclusive marketplaces. These marketplaces feature listed products within the ecosystem that match a specific criteria.
  4. **everything market:** shows the catch-all everything marketplace. This marketplace features all listed items across the entire ecosystem.

If the personal inventory is empty, start by [creating a thing](#creating-a-thing).

## creating a thing

1. Click "create thing" within the personal inventory. This will bring up a modal prompting to provide an image and some attributes.
2. Upload an image (preferrably one that represents a real, tangible asset) and type in some attributes. Then click submit and see the product appear in your personal inventory.

### guided example

1. Save the following image and upload into the photo box:

![NEAR shirt](https://arweave.net/oNGd9-hZCRU8KEtTNQzDPvW8s7jG1foD_c-GaBBo9Do)

2. Then, enter in some attributes:

| Attribute | Value |
| --- | --- |
| Category | Clothing |
| Subcategory | Tops |
| Type | T-Shirt |
| Brand | NEAR Protocol |

3. Click submit to create the shirt and see it appear in your personal inventory.

## minting a thing

Assuming that an unminted thing exists in the personal inventory:

1. Click the image to flip the card and expose the "MINT" button.
2. Click "MINT" and this will redirect to NEAR wallet to approve the transaction.
3. Approve the transaction.

It may take a moment to take effect, but you should see the "MINT" button turn into a "LIST" button, signifying that the thing has been minted.

## listing a thing

:::info

A thing can only be listed by the user that owns it and if it has already been minted.

:::

Listing requires storage.

To deposit storage:

1. Click the "deposit storage" button which will redirect to NEAR wallet.
2. Approve the transaction

Now you have storage available to list your things.

To list:

1. Click the image of a minted thing to flip the card and expose the "LIST" button.
2. Click "LIST" and this will bring up a listing modal where you can enter in a price.
3. Enter in a price or keep it at 0.
4. Click submit. This will redirect to NEAR wallet to approve the listing.
5. Approve the transaction.

It may take a moment to take effect, but you should see the Thing appear in multiple approriate markets, signifying that the thing has been listed.

## delisting a thing

:::info

A thing can only be delisted by the user that owns it and if it has already been listed.

:::

To delist:

1. Click the image of a listed thing in your personal market to flip the card and expose the "DELIST" button.
2. Click "DELIST" and this will redirect to NEAR wallet to approve the delisting.
3. Approve the transaction.

It may take a moment to take effect, but you should see the Thing disappear from the markets, signifying that the thing has been delisted.

## buying a thing

:::info

A thing can only be bought by a user that does not own it and if it has already been listed.

:::

To buy:

1. Click the image of an unowned thing in any of the markets to flip the card and expose the "BUY" button.
2. Click "BUY" and this will redirect to NEAR wallet to approve the buy.
3. Approve the transaction.

It may take a moment to take effect, but you should see the Thing appear in your personal inventory and no longer appear in any of the markets, signifying that the thing has been bought.

:::info

There is a known bug that if the buy transaction fails, then the thing will still appear in the personal inventory and not be removed from any of the markets.
We are working with Mintbase to fix this with their improved callback mechanism coming soon.

:::
