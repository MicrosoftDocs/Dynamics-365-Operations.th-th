---
title: Project Service Automation
description: "โซลูชันนี้ใช้คุณลักษณะการรวมข้อมูลในการซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Microsoft Dynamics 365 for Finance and Operations และ Microsoft Dynamics 365 for Project Service Automation ผ่าน Common Data Service (CDS)"
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: th-th
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a>Project Service Automation

โซลูชันการรวม Project Service Automation กับ Finance and Operations ใช้คุณลักษณะการรวมข้อมูลในการซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Microsoft Dynamics 365 for Finance and Operations และ Microsoft Dynamics 365 for Project Service Automation ผ่าน Common Data Service (CDS) เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมเปิดใช้งานทิศทางของโครงการ สัญญาโครงการ รายการสัญญาโครงการ เหตุการณ์สำคัญของรายการสัญญาโครงการ งานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง และการประเมินค่าใช้จ่ายจาก Project Service Automation ไปยัง Finance and Operations

> [!NOTE] 
> ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 คุณต้องติดตั้ง KB 4074835 ซึ่งจะทำให้คุณสามารถรวมโครงการที่มีราคาคงที่ได้
>
> ถ้าคุณกำลังใช้ Dynamics 365 for Finance and Operations รุ่น 8.0 คุณจะสามารถใช้การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชันได้
>
> ถ้าคุณกำลังใช้ Dynamics 365 for Finance and Operations รุ่น 8.0.1 คุณจะสามารถซิงโครไนส์ค่าที่เกิดขึ้นจริงได้
>
> ถ้าคุณกำลังใช้ Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้เท็มเพลตเพื่อรวมงานโครงการ ค่าใช้จ่ายประเภทธุรกรรม การประเมินชั่วโมง การประเมินค่าใช้จ่าย และค่าที่เกิดขึ้นจริงได้ และสามารถตั้งค่าคอนฟิกการล็อคฟังก์ชันได้ ถ้าคุณต้องตั้งค่าการกระจายการลงบัญชี เราขอแนะนำให้ คุณติดตั้ง KB 4131710 ด้วย

ก่อนที่คุณจะสามารถรวม Project Service Automation กับ Finance and Operations ได้ คุณต้องตั้งค่าคอนฟิกพารามิเตอร์การรวม Project Service Automation สำหรับข้อมูลเพิ่มเติม โปรดดูพารามิเตอร์การรวม Project Service Automation

โซลูชันการรวมนี้เปิดใช้งานการซิงโครไนส์โดยตรงในสถานการณ์จำลองต่อไปนี้:

- รักษาสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
- สร้างโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
- รักษารายการสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
- รักษาเหตุการณ์สำคัญของรายการสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
- รักษางานโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
- รักษาประเภทธุรกรรมค่าใช้จ่ายใน Finance and Operations และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Finance and Operations ไปยัง Project Service Automation
- สร้างการประมาณการชั่วโมงของโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
- สร้างการประมาณการค่าใช้จ่ายของโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance and Operations

## <a name="data-synchronization"></a>การซิงโครไนส์ข้อมูล
ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลที่เป็นส่วนหนึ่งของการรวมระหว่าง Project Service Automation และ Finance and Operations

> [!NOTE]
> ไม่ใช่ทุกเท็มเพลตที่พร้อมใช้งานในขณะนี้ เท็มเพลตจะถูกนำออกใช้เมื่อเสร็จสมบูรณ์แล้ว

[![การรวม Project Service Automation กับ Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>ความต้องการของระบบสำหรับ Finance and Operations

ในการใช้โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations คุณต้องติดตั้ง Microsoft Dynamics 365 for Finance and Operations, Enterprise edition รุ่น 7.3 ที่มีการอัพเดตแพลตฟอร์ม 12 หรือใหม่กว่า

## <a name="system-requirements-for-project-service-automation"></a>ข้อกำหนดของระบบสำหรับ Project Service Automation

ในการใช้โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations คุณต้องติดตั้งส่วนประกอบต่อไปนี้:

- Microsoft Dynamics 365 for Project Service Automation รุ่น 9.0.0.0 หรือใหม่กว่า
- โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Dynamics 365 for Sales เวอร์ชัน 1.14.0.0 (v14) หรือใหม่กว่า
- โซลูชัน Project Service Automation ไปยัง Operations solution สำหรับ Dynamics 365 for Project Service Automation รุ่น 1.0.0.0 หรือใหม่กว่า

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>ติดตั้งโซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ในอินสแตนซ์ Project Service Automation ของคุณ



