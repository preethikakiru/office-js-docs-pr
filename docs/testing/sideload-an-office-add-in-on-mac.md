---
title: Sideload Office Add-ins on Mac for testing
description: Test your Office Add-in on Mac by sideloading.
ms.date: 07/07/2022
ms.localizationpriority: medium
---

# Sideload Office Add-ins on Mac for testing

To see how your add-in will run on Office on Mac, you can sideload your add-in's manifest. This action won't enable you to set breakpoints and debug your add-in's code while it's running, but you can see how it behaves and verify that the UI is usable and rendering appropriately.

> [!NOTE]
> To sideload an Outlook add-in, see [Sideload Outlook add-ins for testing](../outlook/sideload-outlook-add-ins-for-testing.md).

## Prerequisites for Office on Mac

- A Mac running OS X v10.10 "Yosemite" or later with [Office on Mac](https://products.office.com/buy/compare-microsoft-office-products?tab=omac) installed.

- Word on Mac version 15.18 (160109).

- Excel on Mac version 15.19 (160206).

- PowerPoint on Mac version 15.24 (160614).

- The manifest .xml file for the add-in you want to test.

## Sideload an add-in in Office on Mac

1. Use **Finder** to sideload the manifest file. Open **Finder** and then enter Command+Shift+G to open the **Go to folder** dialog.

1. Enter one of the following filepaths, based on the application you want to use for sideloading. If the `wef` folder doesn't exist on your computer, create it.

    - For Word:  `/Users/<username>/Library/Containers/com.microsoft.Word/Data/Documents/wef`
    - For Excel:  `/Users/<username>/Library/Containers/com.microsoft.Excel/Data/Documents/wef`
    - For PowerPoint: `/Users/<username>/Library/Containers/com.microsoft.Powerpoint/Data/Documents/wef`

        > [!NOTE]
        > The remaining steps describe how to sideload a Word add-in.

1. Copy your add-in's manifest file to this `wef` folder.

    ![Wef folder in Office on Mac.](../images/all-my-files.png)

1. Open Word, and then open a document. Restart Word if it's already running.

1. In Word, choose **Insert** > **Add-ins** > **My Add-ins** (drop-down menu), and then choose your add-in.

    ![My Add-ins in Office on Mac.](../images/my-add-ins-wikipedia.png)

    > [!IMPORTANT]
    > Sideloaded add-ins will not show up in the My Add-ins dialog box. They are only visible within the drop-down menu (small down-arrow to the right of My Add-ins on the **Insert** tab). Sideloaded add-ins are listed under the **Developer Add-ins** heading in this menu.

1. Verify that your add-in is displayed in Word.

    ![Office Add-in displayed in Office on Mac.](../images/lorem-ipsum-wikipedia.png)

## Remove a sideloaded add-in

You can remove a previously sideloaded add-in by clearing the Office cache on your computer. Details on how to clear the cache for each platform and application can be found in the article [Clear the Office cache](clear-cache.md).

## See also

- [Sideload Office Add-ins on iPad for testing](sideload-an-office-add-in-on-ipad.md)
- [Debug Office Add-ins on a Mac](debug-office-add-ins-on-ipad-and-mac.md)
- [Sideload Outlook add-ins for testing](../outlook/sideload-outlook-add-ins-for-testing.md)
