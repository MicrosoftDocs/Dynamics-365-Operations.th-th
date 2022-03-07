---
title: จัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบมีพร้อมใช้งานสำหรับเซลล์ทำงาน
description: 'งานนี้มุ่งเน้นการเตรียมกระบวนการงานคัมบังเมื่อวัสดุทั้งหมดจะพร้อมใช้งานสำหรับเซลล์ทำงาน '
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 460d55a8c4b8a8401db7abc43721cf0d114c27c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807835"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a>จัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบมีพร้อมใช้งานสำหรับเซลล์ทำงาน

[!include [banner](../../includes/banner.md)]

งานนี้มุ่งเน้นการเตรียมกระบวนการงานคัมบังเมื่อวัสดุทั้งหมดจะพร้อมใช้งานสำหรับเซลล์ทำงาน  ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF งานนี้มีไว้สำหรับผู้ปฏิบัติงานเครื่องจักร

1. ไปที่บอร์ดคัมบังสำหรับงานกระบวนการ
2. ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา 
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
    * เลือกเซลล์ทำงาน 1250 และคลิกตกลง   
4. ในรายการ ให้เลือกแถว 4
    * ในบริษัทสาธิตสะอาด คัมบัง 000329 ในแถว 4 คืองานแรกที่ยังไม่เสร็จสมบูรณ์  
5. สลับการขยายของส่วนรายการเบิกสินค้า
    * ตรวจสอบว่าสถานะการจัดหาวัสดุพร้อมใช้งานสำหรับสินค้าทั้งหมดในรายการเบิกสินค้า   
    * ถ้ามีงานหลายงานให้เลือก รายการเบิกสินค้าจะแสดงผลรวมของรายการทั้งหมดที่จำเป็นสำหรับงานที่เลือก  
6. คลิกจัดเตรียม 
    * กระบวนการจัดเตรียมตอนนี้เสร็จสมบูรณ์แล้ว  กล่องกาเครื่องหมายที่เลือกสำหรับแถวทั้งหมดในรายการเบิกสินค้าบ่งชี้ว่า มีการเบิกตามสถานะการจัดหาวัสดุ  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]