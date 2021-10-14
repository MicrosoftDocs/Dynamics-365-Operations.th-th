---
title: ขยายเอนทิตี้ข้อมูลปริมาณสินค้าคงคลังคงเหลือ
description: หัวข้อนี้มีตัวอย่างที่แสดงวิธีการเพิ่มฟิลด์แบบขยายลงในมุมมอง INVENTORSITEONHANDENTITY และ INVENTWAREHOUSEONHANDENTITY เพื่อให้สามารถทำงานกับเอนทิตี้ข้อมูลปริมาณสินค้าคงคลังคงเหลือที่สามารถทำงานร่วมกับส่วนขยายได้
author: yufeihuang
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8161d951c3296b63476c4e7b527efca163a4f4b3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577707"
---
# <a name="extend-inventory-on-hand-data-entities"></a>ขยายเอนทิตี้ข้อมูลปริมาณสินค้าคงคลังคงเหลือ

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management มีคุณลักษณะ [ความสามารถในการเพิ่มฟังก์ชัน](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) ซึ่งช่วยให้คุณสามารถ [เพิ่มฟิลด์ลงในตารางผ่านส่วนขยาย](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md) หัวข้อนี้มีตัวอย่างที่แสดงวิธีการเพิ่มฟิลด์แบบขยายลงในมุมมอง `INVENTORSITEONHANDENTITY` และ `INVENTWAREHOUSEONHANDENTITY` เพื่อให้สามารถทำงานกับเอนทิตี้ข้อมูลปริมาณสินค้าคงคลังคงเหลือที่สามารถทำงานร่วมกับส่วนขยายได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเอนทิตี้ข้อมูล โปรดดูที่ [ภาพรวมของการจัดการข้อมูล](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)

> [!NOTE]
> ต่อไปนี้เป็นรายการเอนทิตี้ข้อมูลของปริมาณสินค้าคงคลังคงเหลือบางรายการ:
>
> - ปริมาณคงคลังคงเหลือของสินค้าคงคลังโดยเรียงตามไซต์
> - ปริมาณคงคลังคงเหลือของสินค้าคงคลังโดยเรียงตามไซต์ V2
> - สินค้าคงคลังคงเหลือตามคลังสินค้า
> - ปริมาณสินค้าคงคลังคงเหลือโดยเรียงตามคลังสินค้า v2

หลังจากที่คุณเพิ่มฟิลด์ลงในตารางที่ใช้โดยมุมมอง `inventSiteOnHandView` แล้ว คุณต้องซิงค์กลไกจัดการเพื่อให้มีการรับรู้ส่วนขยายอย่างถูกต้อง

1. ขยายมุมมอง `InventSiteOnHandView` โดยการเพิ่มฟิลด์ส่วนขยาย
1. ขยายมุมมอง `InventSiteOnHandAggregatedView` ด้วยฟิลด์ส่วนขยาย
1. ขยายคลาส `InventSiteOnHandAggregatedViewBuilder` viewBuilder โดยการปรับเปลี่ยนเมธอด `getExtensionFields()` ด้วยวิธีนี้ คุณแม็ปฟิลด์มุมมองเก่ากับฟิลด์มุมมองใหม่เมื่อเรียกใช้การซิงโครไนส์ viewBuilder ได้

ตัวอย่างเช่น คุณได้เพิ่มฟิลด์สี่ฟิลด์ต่อไปนี้ลงในตาราง `InventTable` ผ่านส่วนขยาย:

- ฟิลด์ที่กำหนดเอง 1
- ฟิลด์ที่กำหนดเอง 2
- ฟิลด์ที่กำหนดเอง 3
- ฟิลด์ที่กำหนดเอง 4

ในกรณีนี้ คุณต้องแก้ไขเมธอด `getExtensionFields()` ในลักษณะต่อไปนี้

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

หลังจากที่คุณทำตามขั้นตอนต่อไปนี้แล้ว คุณสามารถขยายปริมาณสินค้าคงคลังคงเหลือโดยเรียงตามไซต์และปริมาณสินค้าคงคลังคงเหลือโดยใช้เอนทิตี้ข้อมูลคลังสินค้าโดยการเพิ่มฟิลด์ใหม่ ด้วยวิธีนี้ คุณต้องตรวจสอบให้แน่ใจว่ามีการรับรู้และรวมฟิลด์แบบขยายในระหว่างการย้ายข้อมูลที่ใช้เอนทิตี้ข้อมูลเหล่านั้น


[!INCLUDE[footer-include](../../includes/footer-banner.md)]