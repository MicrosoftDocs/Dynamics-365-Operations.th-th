---
title: การควบคุมต้นทุนข้อบกพร่องของสินทรัพย์
description: บทความนี้อธิบายถึงการควบคุมต้นทุนข้อบกพร่องของสินทรัพย์ในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 553b89a43b656669b7730b19898f3a5d81a3873a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889677"
---
# <a name="asset-fault-cost-control"></a>การควบคุมต้นทุนข้อบกพร่องของสินทรัพย์

[!include [banner](../../includes/banner.md)]

 

ในการจัดการสินทรัพย์ คุณสามารถคำนวณต้นทุนของการลงทะเบียนข้อบกพร่องของสินทรัพย์ เพื่อดูภาพรวมของต้นทุนจริงเปรียบเทียบกับต้นทุนตามงบประมาณ ต้นทุนจริงจะขึ้นอยู่กับธุรกรรมที่ลงรายการบัญชี วันที่ คือวันที่ข้อบกพร่องได้มีการเรกคอร์ดอาการ

1. คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **ข้อบกพร่องของสินทรัพย์** > **การควบคุมต้นทุนข้อบกพร่องของสินทรัพย์**

2. ในกล่องโตัตอบ **การควบคุมต้นทุนข้อบกพร่องของสินทรัพย์** ให้เลือกเซ็ตมิติทางการเงินที่จะรวมไว้ในการคำนวณ หากจำเป็น

4. เลือก "ใช่" บนปุ่มสลับ **ข้ามเลขศูนย์** ถ้าคุณไม่ต้องการแสดงผลลัพธ์ที่มีต้นทุนเป็นศูนย์

5. คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้รายการการควบคุมต้นทุนเกี่ยวกับตำเเหน่งที่ทำงานมากเพียงใด 

    ตัวอย่างเช่น หากคุณใส่หมายเลข "1" ในฟิลด์ และคุณมีโครงสร้างตำเเหน่งที่ทำงานหลายระดับ รายการการควบคุมต้นทุนข้อบกพร่องทั้งหมดสำหรับตำเเหน่งที่ทำงาน จะถูกเเสดงบนระดับบนสุด ดังนั้นชั่วโมงในรายการอาจจะมีการเพิ่มจากตำเเหน่งที่ทำงานที่อยู่ในระดับที่ต่ำกว่า 
    
    หากคุณใส่หมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดแสดงรายการควบคุมต้นทุนข้อบกพร่องทั้งหมด บนระดับตำเเหน่งที่ทำงานทั้งหมดที่เกี่ยวข้อง

6. หากคุณต้องการจำกัดการค้นหา คุณสามารถเลือกสินทรัพย์เฉพาะ วันที่บกพร่อง สาเหตุของความบกพร่อง บนแท็บด่วน **เรกคอร์ดที่จะรวม**

7. คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณ

8. คลิกปุ่ม **จัดกลุ่มโดย** เพื่อแสดงระดับรายละเอียดที่จำเป็นต้องใช้ในการคำนวณ ปุ่ม **จัดกลุ่มโดย** ที่เลือกจะถูกเน้น คลิกบนปุ่มเพื่อเรียกใช้งานหรือยกเลิกการเรียกใช้งาน

## <a name="example"></a>ตัวอย่าง

ตัวอย่างนี้แสดงการคำนวณการควบคุมต้นทุนที่บกพร่องของสินทรัพย์

- ฟิลด์ **งบประมาณเดิม** แสดงต้นทุนตามงบประมาณจากการคาดการณ์ใบสั่งงาน 
- ฟิลด์ **ต้นทุนจริง** แสดงต้นทุนที่ลงรายการบัญชีบนใบสั่งงาน 
- ฟิลด์ **ต้นทุนผูกมัด** แสดงจำนวนรวมของต้นทุนที่บริษัทของคุณจะได้รับการกำหนดในความสัมพันธ์กับใบสั่งงาน

    ![รูปที่ 1.](media/05-controlling-and-reporting.png)

สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าข้อบกพร่อง ดูที่บทความ [การจัดการข้อบกพร่อง](../setup-for-work-orders/fault-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]