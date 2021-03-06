---
title: Categorizing images - Computer Vision
titleSuffix: Azure Cognitive Services
description: Learn concepts related to the image categorization feature of the Computer Vision API.
services: cognitive-services
author: PatrickFarley
manager: nitinme

ms.service: cognitive-services
ms.subservice: computer-vision
ms.topic: conceptual
ms.date: 08/29/2018
ms.author: pafarley
ms.custom: seodec18
---

# Image categorization with Computer Vision

In addition to tagging and descriptions, Computer Vision returns the taxonomy-based categories defined in previous versions. These categories are organized as a taxonomy with parent/child hereditary hierarchies. All categories are in English. They can be used alone or with our new tagging models.

## The 86-category concept

Based on a list of 86 concepts seen in the following diagram, an image can be categorized ranging from broad to specific. For the full taxonomy in text format, see [Category Taxonomy](category-taxonomy.md).

![Grouped lists of all the categories in the category taxonomy](./Images/analyze_categories-v2.png)

## Image categorization examples

The following JSON response illustrates what Computer Vision returns when categorizing the example image based on its visual features.

![A woman on the roof of an apartment building](./Images/woman_roof.png)

```json
{
    "categories": [
        {
            "name": "people_",
            "score": 0.81640625
        }
    ],
    "requestId": "bae7f76a-1cc7-4479-8d29-48a694974705",
    "metadata": {
        "height": 200,
        "width": 300,
        "format": "Jpeg"
    }
}
```

The following table illustrates a typical image set and the category returned by Computer Vision for each image.

| Image | Category |
|-------|----------|
| ![Four people posed together as a family](./Images/family_photo.png) | people_group |
| ![A puppy sitting in a grassy field](./Images/cute_dog.png) | animal_dog |
| ![A person standing on a mountain rock at sunset](./Images/mountain_vista.png) | outdoor_mountain |
| ![A pile of bread roles on a table](./Images/bread.png) | food_bread |

## Next steps

Learn concepts about [tagging images](concept-tagging-images.md) and [describing images](concept-describing-images.md).
