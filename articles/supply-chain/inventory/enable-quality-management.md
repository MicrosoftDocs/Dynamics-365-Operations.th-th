---
title: เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน
description: หัวข้อนี้แสดงภาพรวมของกระบวนการสำหรับการตั้งค่าและการตั้งค่าคอนฟิกคุณลักษณะการจัดการคุณภาพและความไม่สอดคล้องกันใน Microsoft Dynamics 365 Supply Chain Management
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2c8b7e9a1a8d7692e1d2215e38de1b0f4d2d82
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567426"
---
# <a name="enable-quality-and-nonconformance-management"></a>เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน

[!include [banner](../includes/banner.md)]

หัวข้อนี้แสดงภาพรวมของกระบวนการสำหรับการตั้งค่าและการตั้งค่าคอนฟิกคุณลักษณะการจัดการคุณภาพและความไม่สอดคล้องกันใน Microsoft Dynamics 365 Supply Chain Management

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อเปิดใช้งานการจัดการคุณภาพบนระบบของคุณ

1. ไปที่ **การจัดการสินค้าคงคลัง \> การตั้งค่า \> พารามิเตอร์สินค้าคงคลังและการจัดการคลังสินค้า**
1. บนแท็บ **การจัดการคุณภาพ** ให้ตั้งค่าตัวเลือก **ใช้การจัดการคุณภาพ** เป็น *ใช่*
1. ในฟิลด์ **อัตราต่อชั่วโมง** ป้อนอัตราค่าแรงต่อชั่วโมงในสกุลเงินท้องถิ่น อัตราต่อชั่วโมงจะถูกใช้ในการคำนวณต้นทุนสำหรับการดำเนินงานที่เกี่ยวข้องกับความไม่สอดคล้อง อัตราต่อชั่วโมงและต้นทุนที่คำนวณได้ให้การอ้างอิงข้อมูลสำหรับความไม่สอดคล้อง จะไม่สัมพันธ์กับฟังก์ชันอื่น
1. เลือก **การตั้งค่ารายงาน**
1. เพิ่มบรรทัดใหม่ให้กับรายงานชนิดต่างๆ และเลือกชนิดของเอกสารที่จะใช้สำหรับรายงานแต่ละฉบับ
1. ปิดหน้า
1. ปิดหน้า

## <a name="quality-management-configuration-process"></a>กระบวนการตั้งค่าคอนฟิกการจัดการคุณภาพ

ก่อนที่คุณสามารถเริ่มใช้คุณลักษณะการจัดการคุณภาพและสร้างใบสั่งตรวจสอบคุณภาพได้ คุณต้องตั้งค่าคอนฟิกระบบและข้อกำหนดเบื้องต้น ต่อไปนี้เป็นรายการขั้นตอนที่ต้องใช้ในการตั้งค่าคอนฟิกการจัดการคุณภาพ

1. [เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน](#enable-qm)
1. ไม่ระบุ: [ตั้งค่าคอนฟิกเครื่องมือทดสอบ](quality-test-instruments.md)
1. [ตั้งค่าคอนฟิกการทดสอบ](quality-tests.md)
1. [ตั้งค่าคอนฟิกตัวแปรทดสอบและผลที่ได้](quality-test-variables.md)
1. [ตั้งค่าคอนฟิกกลุ่มทดสอบ](quality-test-groups.md)
1. ไม่ระบุ: [ตั้งค่าคอนฟิกกลุ่มคุณภาพ และเชื่อมโยงกับผลิตภัณฑ์](quality-groups.md)
1. ไม่ระบุ: [ตั้งค่าคอนฟิกการเชื่อมโยงคุณภาพ](quality-associations.md)

หลังจากเสร็จสิ้นการตั้งค่าคอนฟิกแล้ว คุณสามารถเริ่มต้นสร้างและประมวลผลใบสั่งตรวจสอบคุณภาพได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสร้างงานที่มีใบสั่งตรวจสอบคุณภาพ โปรดดู [ใบสั่งตรวจสอบคุณภาพ](quality-orders.md)

## <a name="nonconformance-management-configuration-process"></a>กระบวนการตั้งค่าคอนฟิกการจัดการความไม่สอดคล้องกัน

ก่อนที่คุณสามารถเริ่มใช้คุณลักษณะการจัดการความไม่สอดคล้องกันและสร้างความไม่สอดคล้องกันได้ คุณต้องตั้งค่าคอนฟิกระบบและข้อกำหนดเบื้องต้น ต่อไปนี้เป็นรายการขั้นตอนที่ต้องใช้ในการตั้งค่าคอนฟิกการจัดการความไม่สอดคล้องกัน

1. [เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน](#enable-qm)
1. [ตั้งค่าคอนฟิกผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน](quality-responsible-workers.md)
1. [ตั้งค่าคอนฟิกชนิดของปัญหา](quality-problem-types.md)
1. [ตั้งค่าคอนฟิกโซนตรวจสอบสินค้า](quality-quarantine-zones.md)
1. [ตั้งค่าคอนฟิกชนิดของการวินิจฉัย](quality-diagnostic-types.md)
1. [ตั้งค่าคอนฟิกการดำเนินการ](quality-operations.md)
1. ไม่ระบุ: [ตั้งค่าคอนฟิกค่าธรรมเนียมคุณภาพ](quality-charges.md)

หลังจากเสร็จสิ้นการตั้งค่าคอนฟิกแล้ว คุณสามารถเริ่มต้นสร้างและประมวลผลความไม่สอดคล้องกันได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างและทำงานกับความไม่สอดคล้องกัน ให้ดูที่ [สร้างและประมวลผลความไม่สอดคล้องกัน](tasks/create-process-non-conformance.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ภาพรวมของการจัดการคุณภาพ](quality-management-processes.md)
- [เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน](enable-quality-management.md)
- [การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
