---
title: ขยายเอนทิตี้ข้อมูลปริมาณสินค้าคงคลังคงเหลือ
description: หัวข้อนี้มีตัวอย่างที่แสดงวิธีการเพิ่มฟิลด์แบบขยายลงในมุมมอง INVENTORSITEONHANDENTITY และ INVENTWAREHOUSEONHANDENTITY เพื่อให้สามารถทำงานกับเอนทิตี้ข้อมูลปริมาณสินค้าคงคลังคงเหลือที่สามารถทำงานร่วมกับส่วนขยายได้
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0f48e424a9ab3349d3c114ecbd01424005b9a9c6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219352"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="d9aae-103">ขยายเอนทิตี้ข้อมูลปริมาณสินค้าคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="d9aae-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9aae-104">Microsoft Dynamics 365 Supply Chain Management มีคุณลักษณะ [ความสามารถในการเพิ่มฟังก์ชัน](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) ซึ่งช่วยให้คุณสามารถ [เพิ่มฟิลด์ลงในตารางผ่านส่วนขยาย](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md)</span><span class="sxs-lookup"><span data-stu-id="d9aae-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span></span> <span data-ttu-id="d9aae-105">หัวข้อนี้มีตัวอย่างที่แสดงวิธีการเพิ่มฟิลด์แบบขยายลงในมุมมอง `INVENTORSITEONHANDENTITY` และ `INVENTWAREHOUSEONHANDENTITY` เพื่อให้สามารถทำงานกับเอนทิตี้ข้อมูลปริมาณสินค้าคงคลังคงเหลือที่สามารถทำงานร่วมกับส่วนขยายได้</span><span class="sxs-lookup"><span data-stu-id="d9aae-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="d9aae-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเอนทิตี้ข้อมูล โปรดดูที่ [ภาพรวมของการจัดการข้อมูล](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)</span><span class="sxs-lookup"><span data-stu-id="d9aae-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d9aae-107">ต่อไปนี้เป็นรายการเอนทิตี้ข้อมูลของปริมาณสินค้าคงคลังคงเหลือบางรายการ:</span><span class="sxs-lookup"><span data-stu-id="d9aae-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="d9aae-108">ปริมาณคงคลังคงเหลือของสินค้าคงคลังโดยเรียงตามไซต์</span><span class="sxs-lookup"><span data-stu-id="d9aae-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="d9aae-109">ปริมาณคงคลังคงเหลือของสินค้าคงคลังโดยเรียงตามไซต์ V2</span><span class="sxs-lookup"><span data-stu-id="d9aae-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="d9aae-110">สินค้าคงคลังคงเหลือตามคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="d9aae-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="d9aae-111">ปริมาณสินค้าคงคลังคงเหลือโดยเรียงตามคลังสินค้า v2</span><span class="sxs-lookup"><span data-stu-id="d9aae-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="d9aae-112">หลังจากที่คุณเพิ่มฟิลด์ลงในตารางที่ใช้โดยมุมมอง `inventSiteOnHandView` แล้ว คุณต้องซิงค์กลไกจัดการเพื่อให้มีการรับรู้ส่วนขยายอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d9aae-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="d9aae-113">ขยายมุมมอง `InventSiteOnHandView` โดยการเพิ่มฟิลด์ส่วนขยาย</span><span class="sxs-lookup"><span data-stu-id="d9aae-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="d9aae-114">ขยายมุมมอง `InventSiteOnHandAggregatedView` ด้วยฟิลด์ส่วนขยาย</span><span class="sxs-lookup"><span data-stu-id="d9aae-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="d9aae-115">ขยายคลาส `InventSiteOnHandAggregatedViewBuilder` viewBuilder โดยการปรับเปลี่ยนเมธอด `getExtensionFields()`</span><span class="sxs-lookup"><span data-stu-id="d9aae-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="d9aae-116">ด้วยวิธีนี้ คุณแม็ปฟิลด์มุมมองเก่ากับฟิลด์มุมมองใหม่เมื่อเรียกใช้การซิงโครไนส์ viewBuilder ได้</span><span class="sxs-lookup"><span data-stu-id="d9aae-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="d9aae-117">ตัวอย่างเช่น คุณได้เพิ่มฟิลด์สี่ฟิลด์ต่อไปนี้ลงในตาราง `InventTable` ผ่านส่วนขยาย:</span><span class="sxs-lookup"><span data-stu-id="d9aae-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="d9aae-118">ฟิลด์ที่กำหนดเอง 1</span><span class="sxs-lookup"><span data-stu-id="d9aae-118">Custom field 1</span></span>
- <span data-ttu-id="d9aae-119">ฟิลด์ที่กำหนดเอง 2</span><span class="sxs-lookup"><span data-stu-id="d9aae-119">Custom field 2</span></span>
- <span data-ttu-id="d9aae-120">ฟิลด์ที่กำหนดเอง 3</span><span class="sxs-lookup"><span data-stu-id="d9aae-120">Custom field 3</span></span>
- <span data-ttu-id="d9aae-121">ฟิลด์ที่กำหนดเอง 4</span><span class="sxs-lookup"><span data-stu-id="d9aae-121">Custom field 4</span></span>

<span data-ttu-id="d9aae-122">ในกรณีนี้ คุณต้องแก้ไขเมธอด `getExtensionFields()` ในลักษณะต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d9aae-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

<span data-ttu-id="d9aae-123">หลังจากที่คุณทำตามขั้นตอนต่อไปนี้แล้ว คุณสามารถขยายปริมาณสินค้าคงคลังคงเหลือโดยเรียงตามไซต์และปริมาณสินค้าคงคลังคงเหลือโดยใช้เอนทิตี้ข้อมูลคลังสินค้าโดยการเพิ่มฟิลด์ใหม่</span><span class="sxs-lookup"><span data-stu-id="d9aae-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="d9aae-124">ด้วยวิธีนี้ คุณต้องตรวจสอบให้แน่ใจว่ามีการรับรู้และรวมฟิลด์แบบขยายในระหว่างการย้ายข้อมูลที่ใช้เอนทิตี้ข้อมูลเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="d9aae-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]