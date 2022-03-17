---
title: ตั้งค่า Regulatory Configuration Service (RCS)
description: หัวข้อนี้อธิบายวิธีการตั้งค่า Regulatory Configuration Service (RCS)
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 33aab6f0a482ce3d90a7e9828015a8e7bebb7827
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371837"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>ตั้งค่า Regulatory Configuration Service (RCS)

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการตั้งค่า Regulatory Configuration Service (RCS)

## <a name="turn-on-globalization-features"></a>เปิดคุณลักษณะมาตรฐานโลก

1. ลงชื่อเข้าใช้บัญชี RCS ของคุณ
2. เลือกไทล์ **การจัดการคุณลักษณะ**
3. ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้เลือก **คุณลักษณะแบบโลกาภิวัฒน์** ในรายการ แล้วเลือก **เปิดใช้งานเดี๋ยวนี้**

ไทล์สำหรับพื้นที่ทำงาน **คุณลักษณะมาตรฐานโลก** ควรปรากฏบนแดชบอร์ด RCS หลัก

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>ตั้งค่าพารามิเตอร์สำหรับการรวม RCS กับการออกใบแจ้งหนี้อิเล็กทรอนิกส์

1. ในพื้นที่ทำงาน **คุณลักษณะมาตรฐานโลก** ในส่วน **การตั้งค่าที่เกี่ยวข้อง** ให้เลือก **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**
2. บนแท็บ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์** ในฟิลด์ **URI ปลายทางของบริการ** ให้ป้อนปลายทางของบริการที่เหมาะสมสำหรับภูมิศาสตร์ Microsoft Azure ของคุณ ดังแสดงในตารางต่อไปนี้

    | ภูมิศาสตร์ของ Datacenter Azure | URI ปลายทางของบริการ |
    |----------------------------|----------------------|
    | สหรัฐอเมริกา              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | ยุโรป                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | สหราชอาณาจักร             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | เอเชีย                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | ญี่ปุ่น                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. ตรวจสอบว่ามีการตั้งค่าฟิลด์ **รหัสแอปพลิเคชัน** เป็น **0cdb527f-a8d1-4bf8-9436-b352c68682b2** ค่านี้เป็นค่าคงที่ ตรวจสอบให้แน่ใจว่ามีเพียงรหัสเฉพาะสากล (GUID) เท่านั้นที่ป้อน ค่านี้ไม่รวมสัญลักษณ์อื่นใด เช่น ช่องว่าง เครื่องหมายจุลภาค เครื่องหมายจุด หรือเครื่องหมายอัญประกาศ
4. ในฟิลด์ **รหัสสภาพแวดล้อม LCS** ให้ป้อนรหัสของสภาพแวดล้อม Microsoft Dynamics Lifecycle Services (LCS) ของคุณ ค่านี้เป็นการอ้างอิงถึงสภาพแวดล้อม Finance หรือ Supply Chain Management ที่คุณจะใช้กับบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์ เมื่อต้องการขอรับรหัสของคุณ ให้ลงชื่อเข้าใช้ [LCS](https://lcs.dynamics.com/) เปิดโครงการของคุณ จากนั้นบนแท็บ **จัดการสภาพแวดล้อม** ในส่วน **รายละเอียดสภาพแวดล้อม** ให้ค้นหาในฟิลด์ **รหัสสภาพแวดล้อม**

    > [!IMPORTANT]
    > ถ้า Add-in ของการออกใบแจ้งหนี้อิเล็กทรอนิกส์ได้รับการติดตั้งในสภาพแวดล้อม Finance หรือ Supply Chain Management หลายสภาพแวดล้อมใน LCS ให้ใช้รหัสสภาพแวดล้อมของสภาพแวดล้อมที่ติดตั้งล่าสุดเสมอ ถ้าคุณตัดสินใจที่จะติดตั้ง Add-in ในสภาพแวดล้อมใหม่หลังจากที่คุณตั้งค่าและทำงานกับฟังก์ชันการออกใบแจ้งหนี้อิเล็กทรอนิกส์ ให้อัปเดตฟิลด์ **รหัสสภาพแวดล้อม LCS** ใน RCS เป็นค่าล่าสุด

5. เลือก **ตกลง** และจากนั้นปิดหน้า

## <a name="configuration-providers"></a>ตัวให้บริการการตั้งค่าคอนฟิก

คุณสามารถใช้ตัวให้บริการการตั้งค่าคอนฟิกเพื่อแยกความแตกต่างระหว่างเจ้าของการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ที่ใช้ในกระบวนการออกใบแจ้งหนี้อิเล็กทรอนิกส์และเจ้าของคุณลักษณะมาตรฐานโลก สำหรับคุณลักษณะมาตรฐานโลกทั้งหมดที่ได้รับจาก Microsoft และเผยแพร่ในที่เก็บส่วนกลาง ตัวให้บริการการตั้งค่าคอนฟิกจะได้รับการตั้งค่าเป็น **Microsoft** (`http://microsoft.com`)

คุณสามารถปรับเฉพาะการตั้งค่าคอนฟิก ER และคุณลักษณะมาตรฐานโลกที่เป็นของตัวให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่เท่านั้น คุณสามารถใช้การตั้งค่าคอนฟิกและคุณลักษณะต่างๆ เหล่านี้เป็นเทมเพลตเพื่อสร้างการตั้งค่าคอนฟิกและคุณลักษณะที่เป็นของตัวให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่เพื่อให้คุณสามารถปรับได้

อันดับแรก ให้สร้างตัวให้บริการการตั้งค่าคอนฟิก แล้วตั้งค่าหนึ่งในตัวให้บริการการตั้งค่าคอนฟิกเป็นใช้งานอยู่ คุณไม่สามารถตั้งค่าตัวให้บริการการตั้งค่าคอนฟิกของ **Microsoft** เป็นใช้งานอยู่

### <a name="create-a-configuration-provider"></a>สร้างตัวให้บริการการตั้งค่าคอนฟิก

1. ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **ตัวให้บริการการตั้งค่าคอนฟิก**
2. เลือก **ใหม่**
3. ในฟิลด์ **ชื่อ** ป้อนชื่อเฉพาะสำหรับตัวให้บริการการตั้งค่าคอนฟิก
4. ในฟิลด์ **ที่อยู่อินเทอร์เน็ต** ให้ป้อน URL เฉพาะของตัวให้บริการการตั้งค่าคอนฟิก
5. เลือก **ตกลง** และจากนั้นปิดหน้า

### <a name="select-a-configuration-provider-as-active"></a>เลือกตัวให้บริการการตั้งค่าคอนฟิกเป็นใช้งานอยู่

1. ในรายการตัวให้บริการการตั้งค่าคอนฟิก ให้เลือกตัวให้บริการการตั้งค่าคอนฟิกที่คุณต้องการตั้งค่าเป็นใช้งานอยู่
2. เลือก **กำหนดเป็นใช้งานอยู่**

## <a name="import-er-configurations-from-the-global-repository"></a>นำเข้าการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลาง

1. ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **ตัวให้บริการการตั้งค่าคอนฟิก**
2. ในรายการตัวให้บริการการตั้งค่าคอนฟิก เลือก **Microsoft** แล้วจากนั้น เลือก **ที่เก็บ**
3. เลือก **ส่วนกลาง** จากนั้นบานหน้าต่างการดำเนินการ ให้เลือก **เปิด**
4. นําเข้าโมเดล ER ต่อไปนี้:

    - **แบบจำลองบริบทใบแจ้งหนี้ของลูกค้า**
    - **แบบจำลองใบแจ้งหนี้**
    - **เอกสารทางการเงิน** (เช่น สถานการณ์ของบราซิล หากจำเป็น)
    - **แบบจำลองข้อความตอบสนอง**

5. ถ้า **การแมปแบบจำลองใบแจ้งหนี้** ไม่ถูกนําเข้าโดยอัตโนมัติ ให้นําเข้า
6. ปิดหน้า
