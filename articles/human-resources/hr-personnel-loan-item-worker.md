---
title: สินค้าที่ให้กู้ยืมแก่ผู้ปฏิบัติงาน
description: 'ขั้นตอนนี้แสดงวิธีการยืมสินค้ากับผู้ปฏิบัติงาน และบันทึกการส่งสินค้าคืนของผู้ปฏิบัติงาน '
author: twheeloc
ms.date: 11/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonLoan, HcmPersonLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6e0833eed3a423938ecc76957d18cccad2ca9b0
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686980"
---
# <a name="loan-item-to-a-worker"></a>สินค้าที่ให้กู้ยืมแก่ผู้ปฏิบัติงาน


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



ขั้นตอนนี้แสดงวิธีการยืมสินค้ากับผู้ปฏิบัติงาน และบันทึกการส่งคืนสินค้าของสินค้าที่ถูกยืม ผู้ปฏิบัติงานยังสามารถขอยืมสินค้าผ่านทางหน้า **ระบบบริการตนเองของพนักงาน**  บริษัทข้อมูลสาธิต **USMF** ถูกนำมาใช้ในการสร้างกระบวนงานนี้


## <a name="loan-an-item-to-a-worker"></a>ให้ผู้ปฏิบัติงานกู้ยืมสินค้า

1. ไปที่ **ฝ่ายทรัพยากรบุคคล \> ผู้ปฏิบัติงาน \> ให้กู้ยืมสินค้า \> อุปกรณ์ที่ให้ยืม**
2. เลือก **ใหม่**
3. ในฟิลด์ **บุคคล** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
4. ในฟิลด์ **สินค้าที่ให้กู้ยืม** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
5. ในฟิลด์ **แผนการส่งคืน** ให้ป้อนวันที่ที่พนักงานต้องส่งคืนสินค้าที่ให้กู้ยืม
6. เลือก **บันทึก**
7. ปิดหน้า

## <a name="return-a-loan-item"></a>ส่งคืนสินค้าที่ให้กู้ยืม

1. ไปที่ **ฝ่ายทรัพยากรบุคคล \> ผู้ปฏิบัติงาน \> ให้กู้ยืมสินค้า \> อุปกรณ์ที่ให้ยืม**
2. เลือก **แก้ไข**
3. ในฟิลด์ **การส่งคืนจริง** ให้ป้อนวันที่และเวลา

[!INCLUDE[footer-include](../includes/footer-banner.md)]
