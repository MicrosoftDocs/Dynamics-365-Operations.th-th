---
title: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากปัญหากับปฏิทิน
description: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากปัญหากับปฏิทิน
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938562"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากปัญหากับปฏิทิน

รหัสข้อผิดพลาด: TRX2716

## <a name="symptoms"></a>อาการ

เมื่อคุณพยายามยืนยันการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:

> ชนิดปฏิทิน %1 กำหนดให้ต้องมีการเช็คอินและเช็คเอาท์การนัดหมาย %2

ดังนั้นคุณจึงไม่สามารถยืนยันการจัดส่งของสินค้าได้

## <a name="cause"></a>สาเหตุ

มีการนัดหมายที่ใช้งานอยู่ ตัวอย่างเช่น มีกฎที่ต้องมีการเช็คอินโดยพนักงานขับรถ ขณะนี้โหลดอยู่ในสถานะที่การยืนยันการจัดส่งล้มเหลว

## <a name="resolution"></a>ความละเอียด

คุณต้องตรวจสอบและแก้ไขปัญหาใด ๆ กับการนัดหมายที่ใช้งานอยู่ที่เชื่อมโยงกับงาน

1. ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**
1. เลือกสินค้าที่การจัดส่งไม่สามารถยืนยันได้
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **การขนส่ง** ในกลุ่ม **การนัดหมาย** ให้เลือก **การจัดกำหนดการนัดหมาย**
1. ทำตามขั้นตอนเหล่านี้

    - ตรวจสอบให้แน่ใจว่าการเช็คอิน/เช็คเอาท์พนักงานขับรถเสร็จสิ้นแล้วสำหรับการนัดหมาย
    - ทำให้เสร็จสมบูรณ์หรือยกเลิกการนัดหมาย
    - ปิดใช้งานตัวเลือก **ต้องใช้การเช็คอินโดยพนักงานขับรถ** สำหรับกฎการนัดหมายที่เกี่ยวข้อง
