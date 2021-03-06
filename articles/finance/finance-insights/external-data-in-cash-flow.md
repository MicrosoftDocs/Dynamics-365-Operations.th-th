---
title: ใช้ข้อมูลภายนอกในการคาดการณ์กระแสเงินสด (ตัวอย่าง)
description: หัวข้อนี้จะอธิบายขั้นตอนการตั้งค่าที่คุณต้องดำเนินการให้เสร็จสมบูรณ์เพื่อให้สามารถป้อนหรือนำเข้าข้อมูลภายนอกเข้าในการคาดการณ์กระแสเงินสดได้
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ae0eba6d397725cf425d9781a597d904e1958d44
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009404"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>ใช้ข้อมูลภายนอกในการคาดการณ์กระแสเงินสด (ตัวอย่าง)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

คุณสามารถป้อนหรือนำเข้าข้อมูลภายนอกเข้าในการคาดการณ์กระแสเงินสดได้ หัวข้อนี้จะอธิบายขั้นตอนการตั้งค่าที่เกี่ยวข้องกับการใช้ข้อมูลภายนอกโดยเฉพาะและเปิดใช้งานข้อมูลภายนอกที่จะรวมไว้ในการคาดการณ์กระแสเงินสด

## <a name="external-data-setup"></a>การตั้งค่าข้อมูลจากภายนอก

ใช้แท็บ **แหล่งที่มาภายนอก** ในหน้า **การตั้งค่าการคาดการณ์กระแสเงินสด** (**การจัดการเงินสดและธนาคาร \> การคาดการณ์กระแสเงินสด**) เพื่อป้อนการตั้งค่าที่สนับสนุนการใช้ข้อมูลภายนอกในการคาดการณ์กระแสเงินสด

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่า ให้ดูที่ [การคาดการณ์กระแสเงินสด](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting)

เมื่อต้องการป้อนข้อมูลภายนอกสำหรับการคาดการณ์กระแสเงินสด คุณสามารถใช้ประสบการณ์เปิดใน Excel สำหรับการป้อนและการปรับเปลี่ยนข้อมูลภายนอก เลือกปุ่ม **ข้อมูลภายนอก** แล้วเลือก **เพิ่มข้อมูลภายนอก** หรือ **แก้ไขข้อมูลภายนอกที่มีอยู่** เมื่อ Microsoft Excel เปิดไฟล์แล้ว คุณสามารถป้อนข้อมูลในฟิลด์ต่อไปนี้:

- **รหัสรายการ**
- **คำอธิบาย** (ไม่จำเป็น)
- **ชื่อแหล่งที่มาภายนอก** – เลือกค่าใดค่าหนึ่งในรายการที่คุณได้กำหนดไว้เมื่อคุณตั้งค่าข้อมูลเชิงลึกทางการเงิน
- **นิติบุคคล**
- **วัน เดือน**
- **จำนวนเงินในสกุลเงินของธุรกรรม**
- **รหัสสกุลเงิน**
- **มิติเริ่มต้น** (ไม่จำเป็น)
- **หมายเลขเอกสาร** (ไม่จำเป็น)
- **หมายเลขบัญชี** (ไม่จำเป็น)
- **ชื่อบัญชี** (ไม่จำเป็น)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>การนำเข้าข้อมูลภายนอกโดยใช้กรอบงานการจัดการข้อมูล

คุณสามารถนำเข้าข้อมูลภายนอกสำหรับการคาดการณ์กระแสเงินสดโดยใช้พื้นที่ทำงาน **การจัดการข้อมูล** และเอนทิตีที่มีการตั้งชื่อ **การคาดการณ์กระแสเงินสดสำหรับการคาดการณ์กระแสเงินสด**

นอกจากนี้ ถ้าคุณต้องการย้ายข้อมูลการตั้งค่าจากสภาพแวดล้อมหนึ่งไปยังอีกพื้นที่หนึ่ง เอนทิตีที่พร้อมใช้งานสำหรับตารางการตั้งค่าที่จำเป็นต้องใช้:

- การตั้งค่าแหล่งที่มาภายนอกของการคาดการณ์กระแสเงินสด
- การตั้งค่านิติบุคคลที่เป็นแหล่งที่มาภายนอกของการคาดการณ์กระแสเงินสด

#### <a name="privacy-notice"></a>ประกาศความเป็นส่วนตัว
การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการ (SLA) สำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด
