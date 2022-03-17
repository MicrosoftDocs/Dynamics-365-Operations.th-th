---
title: ไม่สามารถเข้าถึงบริการภาษี
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาความล้มเหลวในการเข้าถึงบริการคํานวณภาษี
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 48a75cd0c1d91c3b3d9c3fb2e6cab93a76756532
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388572"
---
# <a name="failed-to-access-tax-service"></a>ไม่สามารถเข้าถึงบริการภาษี

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

หัวข้อนี้อธิบายวิธีการแก้ไขข้อผิดพลาด "ไม่สามารถเข้าถึงบริการภาษี" ของบริการคํานวณภาษี

## <a name="symptoms"></a>อาการ

ใน Microsoft Dynamics 365 Finance ให้คุณไปที่ **ภาษี** \> **การตั้งค่า** \> **การตั้งค่าคอนฟิกภาษี** \> **พารมิเตอร์บริการภาษี** บนแท็บ **ทั่วไป** คุณสามารถเปิดใช้งานตัวเลือก **เปิดใช้งานการคํานวณภาษี** จากนั้นให้ลองเลือกค่าในฟิลด์ **ชื่อการตั้งค่าคุณลักษณะ** จะเกิดข้อผิดพลาดขึ้น ข้อความแสดงข้อผิดพลาดระบุว่า "ไม่สามารถเข้าถึงบริการภาษี"

## <a name="cause"></a>สาเหตุ

ข้อผิดพลาดนี้เกิดขึ้นเนื่องจาก Finance ไม่สามารถเข้าถึงบริการคํานวณภาษี

## <a name="resolution"></a>การแก้ปัญหา 

1. ลงชื่อเข้าใช้ Microsoft Dynamics Lifecycle Services (LCS)
2. บนหน้า **สภาพแวดล้อม** บนแท็บ **Add-in ของสภาพแวดล้อม** ค้นหารายการ **การคํานวณภาษี** และตรวจทานสถานะของรายการนั้น สถานะควรเป็น **กำลังติดตั้ง** หรือ **ติดตั้งแล้ว** ถ้าไม่ได้ติดตั้ง Add-in ของบริการคํานวณภาษี คุณจะได้รับข้อผิดพลาด

## <a name="mitigation"></a>การลดความเสี่ยง

1. ใน LCS บนหน้า **Finance** ในส่วน **การรวม Power Platform** เลือก **ติดตั้ง Add-in ใหม่**
2. เลื่อนไปที่ด้านล่างของหน้า และเลือก Add-in **การคํานวณภาษี** ที่จะติดตั้ง
3. กลับไปที่สภาพแวดล้อม Finance ของคุณ และลองเข้าถึงบริการคํานวณภาษี

> [!NOTE]
> ก่อนที่คุณจะติดตั้งบริการคํานวณภาษี ให้ทบทวน [ข้อกำหนดเบื้องต้นของบริการคํานวณภาษี](global-get-started-with-tax-calculation-service.md#prerequisites)
> 
> ถ้าคุณไม่สามารถติดตั้ง Add-in เนื่องจากส่วน **การรวม Power Platform** ไม่พร้อมใช้งาน โปรดดู [ภาพรวมของ Add-in](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) หากคุณยังพบข้อผิดพลาดหลังจากที่ติดตั้ง Add-in โปรดติดต่อผู้ดูแลระบบของคุณ
