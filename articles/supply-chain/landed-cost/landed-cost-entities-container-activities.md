---
title: เอนทิตีกิจกรรมคอนเทนเนอร์
description: หัวข้อนี้มีข้อมูลเกี่ยวกับกิจกรรมคอนเทนเนอร์ ที่ใช้ในการติดตามความคืบหน้าของคอนเทนเนอร์การจัดส่ง
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 7bb2b97e8885e3b1265f0c93585873c8a64f1dfb
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813094"
---
# <a name="container-activities-entity"></a>เอนทิตีกิจกรรมคอนเทนเนอร์

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

กิจกรรมคอนเทนเนอร์ใช้ในการติดตามความคืบหน้าของคอนเทนเนอร์การจัดส่ง เรกคอร์ดจะถูกสร้างขึ้นมาให้กับแต่ละขาที่มอบหมายให้กับเทมเพลตการเดินทางที่เลือกเมื่อสร้างคอนเทนเนอร์การจัดส่ง เรกคอร์ดจะถูกสร้างขึ้นด้วยเมื่อมีการสร้างคอนเทนเนอร์ผ่านเอนทิตีข้อมูล

ข้อมูลเกี่ยวกับความคืบหน้าของคอนเทนเนอร์การจัดส่งที่อยู่ระหว่างส่งต่อมักจะได้รับมาจากแหล่งที่มาภายนอก เอนทิตีกิจกรรมคอนเทนเนอร์ช่วยให้สามารถอัปเดตแหล่งที่มาภายนอก เช่น ผู้ขนส่งสินค้าเพื่ออัปเดตเรกคอร์ดโดยตรงได้ ดังั้น จึงไม่ต้องใช้การอัปเดตข้อมูลด้วยตนเอง

## <a name="container-activities-itmcontaineractivityentity"></a>กิจกรรมคอนเทนเนอร์ (ITMContainerActivityEntity)

คุณสามารถใช้เอนทิตีกิจกรรมคอนเทนเนอร์ (`ITMContainerActivityEntity`) เพื่อสร้างเรกคอร์ดกิจกรรมเพิ่มเติมได้ หรือผู้ขนส่งสินค้าอาจผ่านการอัปเดตค่า **วันที่สิ้นสุดจริง** ที่ยืนยัน

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| วันที่สิ้นสุดจริง | ITMContainerActivityTable.ActualEndDate | วันที่และเวลา | ไม่ | ไม่ |
| วิธีการจัดส่ง | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | ไม่ | ไม่ |
| ประเมินวันที่สิ้นสุด | ITMContainerActivityTable.EsimatedDate | วันที่และเวลา | ไม่ | ไม่ |
| หมายเลขรายการ | ITMContainerActivityTable.LineNum | Numeric(32, 16) | **ใช่** | ไม่ |
| บันทึกย่อ | ITMContainerActivityTable.Notes | nvarchar(MAX) | ไม่ | ไม่ |
| กิจกรรม | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | ไม่ | **ใช่** |
| คอนเทนเนอร์การจัดส่ง | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **ใช่** | **ใช่** |
| การเดินทาง | ITMContainerActivityTable.ShipId | Nvarchar(20) | **ใช่** | **ใช่** |
| ช่วง | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | ไม่ | **ใช่** |
| ผู้ให้บริการ | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | ไม่ | ไม่ |
| อุณหภูมิ | ITMContainerActivityTable.ShipTemperature | Numeric(32, 6) | ไม่ | ไม่ |
| เรือ | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | ไม่ | ไม่ |
| วันที่เริ่มต้น | ITMContainerActivityTable.StartDate | วันที่และเวลา | ไม่ | ไม่ |

## <a name="tracking-control"></a>ตัวควบคุม Tracking

ศูนย์ควบคุมการติดตามจะเปิดใช้งานการอัปเดตฟิลด์ต้นทางที่ระบุที่จะทริกเกอร์โดยการอัปเดตฟิลด์เป้าหมายที่ระบุ หากทั้งค่าฟิลด์ต้นทางและค่าของฟิลด์เป้าหมายมีการอัปเดตโดยใช้เอนทิตีกิจกรรมคอนเทนเนอร์ ฟิลด์เป้าหมายจะแสดงค่าเอนทิตี ลักษณะการทำงานนี้เกี่ยวข้องกับเรกคอร์ดการควบคุมการติดตามที่มีค่า **ชนิดการสร้าง** ของ *ระยะรอคอยสินค้า*

สำหรับพื้นที่ต้นทุนที่มีค่า **ชนิดการสร้าง** ของ *อัปเดตสถานะ* หรือ *ว่างเปล่า* (ซึ่งเป็นค่าที่ผู้ใช้กําหนด) ระบบจะอัปเดตสถานะการเดินทางหรือฟิลด์เป้าหมายตามการตั้งค่าคอนฟิกการควบคุมการติดตาม

## <a name="calculated-fields"></a>ฟิลด์ที่คำนวณได้

ค่าของฟิลด์ต่อไปนี้ในเรกคอร์ดกิจกรรมคอนเทนเนอร์จะคํานวณตามค่าของฟิลด์อื่นๆ แม้ว่าฟิลด์ที่คํานวณได้เหล่านี้จะไม่รวมอยู่ในเอนทิตีข้อมูล แต่ก็จะถูกตั้งค่าถ้ามีการจัดเตรียมฟิลด์ที่ใช้ในการคํานวณไว้

- **จำนวนวันที่ประเมิน** = **วันที่สิ้นสุดโดยประมาณ** – **วันที่เริ่มต้น**
- **จำนวนวันจริง** = **วันที่สิ้นสุดจริง** – **วันที่เริ่มต้น**
