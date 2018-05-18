---
title: "เพิ่มมิติทางการเงินไปยังพื้นที่ทำงานของ CFO"
description: "หัวข้อนี้อธิบายวิธีการเพิ่มมิติทางการเงินไปยังพื้นที่ทำงานของ CFO เพื่อให้สามารถใช้สำหรับการรายงานบัญชีแยกประเภทและงบประมาณ"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5faefe5da8c3a64987a38ebef92eb87049ebe874
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>เพิ่มมิติทางการเงินไปยังพื้นที่ทำงานของ CFO

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการเพิ่มมิติทางการเงินไปยังพื้นที่ทำงานของประธานคณะผู้บริหารด้านการเงิน (CFO) เพื่อให้สามารถใช้สำหรับการรายงานบัญชีแยกประเภทและงบประมาณ พื้นที่ทำงานของ CFO มีแท็บ **ภาพรวม** และแท็บ **การเงิน** รายงานบนสองแท็บนี้มีข้อมูลสำรองโดยหน่วยวัดสองแบบ: LedgerActivityMeasure และ BudgetActivityMeasure ใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (กรกฎาคม 2017) มีความสัมพันธ์ระหว่างหน่วยวัดสองแบบนั้นและเอนทิตี้ DimensionCombinationEntity ดังนั้น คุณสามารถเลือกมิติได้

1. ใน Finance and Operations ในหน้า **ที่จัดเก็บเอนทิตี้** อัพเดตหน่วยวัด **LedgerActivityMeasure** และ **BudgetActivityMeasure**
2. ใน Microsoft Visual Studio เปิดแอพลิเคชัน Application Explorer และค้นหา **LedgerCFO**
3. ภายใต้ **ทรัพยากร** เปิด **LedgerCFOWorkspacePBIX**
4. เมื่อทรัพยากรถูกเปิดขึ้นในเดสก์ท็อป Microsoft Power BI เลือก **รับข้อมูล** เลือก**ฐานข้อมูล SQL Server** แล้วเลือก **เชื่อมต่อ**
5. ป้อนชื่อเซิร์ฟเวอร์ แล้วป้อน **AxDW** เป็นฐานข้อมูล เลือก **DirectQuery** แล้วเลือก **ตกลง**
6. ค้นหาและเลือก **LedgerActivityMeasure\_DimensionCombination** แล้วเลือก **โหลด**

    > [!TIP]
    > ในรายการ **ฟิลด์** เปลี่ยนชื่อตาราง **มิติทางการเงิน** เพื่อให้สามารถระบุได้ง่ายขึ้น

7. เลือก **จัดการความสัมพันธ์** แล้วเลือก **สร้าง**
8. ในฟิลด์แรก เลือก **กิจกรรมบัญชีแยกประเภททั่วไป** แล้วเลือก **LedgerDimension**
9. ในฟิลด์ที่สอง เลือก **LedgerActivityMeasure\_DimensionCombination** (หรือ **มิติทางการเงิน** ถ้าคุณเปลี่ยนชื่อตาราง) เลือกส่วนหัว **DimensionCombinationRECID**
10. ในฟิลด์ **จำนวนนับ** เลือก **หลายต่อหนึ่ง**
11. เปลี่ยนค่า **ทิศทางตัวกรองแบบข้าม** เป็น **เดี่ยว**
12. เลือกทั้ง **ทำให้ความสัมพันธ์นี้เป็นใช้งานอยู่** และ **ยอมรับความถูกต้องของการอ้างอิง** เลือก **ตกลง** แล้วเลือก **ปิด**

    [![สร้างความสัมพันธ์](./media/Create-relationship.png)](./media/Create-relationship.png)

13. ในรายการ **ฟิลด์** คุณควรเห็นตารางและมิติทางการเงินที่พร้อมใช้งาน ลากมิติทางการเงินที่คุณต้องการไปยังตัวกรองระดับรายงาน
14. บันทึกการเปลี่ยนแปลง
15. ใน Application Object Tree (AOT) คลิกขวาโครงการของคุณ จากนั้นเลือก **ซิงโครไนส์**
16. สร้างโครงการของคุณ และจากนั้นเปิดแอพลิเคชันเพื่อดูผลลัพธ์

    [![พื้นที่ทำงานที่เสร็จสมบูรณ์](./media/workspace.png)](./media/workspace.png)

