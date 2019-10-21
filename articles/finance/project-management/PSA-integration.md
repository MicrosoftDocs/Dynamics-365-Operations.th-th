---
title: ภาพรวมของ Project Service Automation
description: หัวข้อนี้แสดงข้อมูลทั่วไปเกี่ยวกับ Dynamics 365 Project Service Automation to Dynamics 365 Finance integration solution
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250564"
---
# <a name="project-service-automation-overview"></a>ภาพรวมของ Project Service Automation

[!include[banner](../includes/banner.md)]

The Project Service Automation to Finance integration solution ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Dynamics 365 Finance และ Dynamics 365 Project Service Automation ผ่าน Common Data Service เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูลเปิดใช้งานทิศทางของโครงการ สัญญาโครงการ รายการสัญญาโครงการ เหตุการณ์สำคัญของรายการสัญญาโครงการ งานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง และการประเมินค่าใช้จ่ายจาก Project Service Automation ไปยัง Finance

> [!NOTE]
> - ถ้าคุณกำลังใช้รุ่น 7.3.0 คุณต้องติดตั้ง KB 4074835 จากนั้น คุณจะสามารถรวมโครงการที่มีราคาคงที่ได้
> - ถ้าคุณกำลังใช้รุ่น 7.3.0 และคุณกำลังนำธุรกรรมค่าธรรมเนียมมาจาก Project Service Automation คุณต้องติดตั้ง KB 4345320 เพื่อรวมค่าธรรมเนียมดังกล่าวในใบแจ้งหนี้โครงการ
> - ถ้าคุณกำลังใช้รุ่น 8.0 คุณจะสามารถใช้การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชันได้
> - ถ้าคุณกำลังใช้รุ่น 8.0.1 หรือรุ่นที่ใหม่กว่า คุณจะสามารถซิงโครไนส์ค่าที่เกิดขึ้นจริงได้

ก่อนที่คุณจะสามารถรวม Project Service Automation Finance and Operations ได้ คุณต้องตั้งค่าคอนฟิกพารามิเตอร์การรวม Project Service Automation สำหรับข้อมูลเพิ่มเติม โปรดดู [พารามิเตอร์การรวม Project Service Automation](PSA-parameters.md)

โซลูชันการรวมนี้เปิดใช้งานการซิงโครไนส์โดยตรงในสถานการณ์จำลองต่อไปนี้:

- รักษาสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance
- สร้างโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance
- รักษารายการสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance
- รักษาเหตุการณ์สำคัญของรายการสัญญาโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance
- รักษางานโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance
- รักษาประเภทธุรกรรมค่าใช้จ่ายใน Finance และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Finance ไปยัง Project Service Automation
- สร้างการประเมินชั่วโมงของโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance
- สร้างการเมินค่าใช้จ่ายโครงการใน Project Service Automation และซิงโครไนส์รายการเหล่านั้นโดยตรงจาก Project Service Automation ไปยัง Finance
- สร้างระยะเวลาโครงการ ค่าใช้จ่าย และค่าธรรมเนียมจริงใน Project Service Automation และสร้างธุรกรรมโครงการในสมุดรายวันการรวม Project Service Automation เพื่อที่จะสามารถลงรายการบัญชีใน Finance ได้

## <a name="data-synchronization"></a>การซิงโครไนส์ข้อมูล

ภาพประกอบต่อไปนี้แสดงว่าข้อมูลถูกซิงโครไนส์อย่างไรโดยเป็นส่วนหนึ่งของการรวมระหว่าง Project Service Automation และ Finance

> [!NOTE]
> ไม่ใช่ทุกเท็มเพลตที่พร้อมใช้งานในขณะนี้ เท็มเพลตจะถูกนำออกใช้เมื่อเสร็จสมบูรณ์แล้ว

[![การรวม Project Service Automation กับ Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>ความต้องการของระบบสำหรับ Finance

ในการใช้ the Project Service Automation ไปจนถึง Finance integration solution คุณต้องติดตั้ง Enterprise Edition 7.3 ที่มีการอัพเดตแพลตฟอร์ม 12 หรือใหม่กว่า

## <a name="system-requirements-for-project-service-automation"></a>ข้อกำหนดของระบบสำหรับ Project Service Automation

ในการใช้ the Project Service Automation ไปจนถึง Finance integration solution คุณต้องติดตั้งส่วนประกอบต่อไปนี้:

- Dynamics 365 Project Service Automation รุ่น 9.0.0.0 หรือใหม่กว่า
- โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสดสำหรับ Dynamics 365 Sales รุ่น 1.14.0.0 (v14) หรือใหม่กว่า
- Project Service Automation ไปจนถึง Finance solution สำหรับ Dynamics 365 Project Service Automation รุ่น 1.0.0.0 หรือใหม่กว่า

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>ติดตั้ง the Project Service Automation ไปจนถึงโซลูชันการรวม Finance ในอินสแตนซ์ Project Service Automation ของคุณ

ดาวน์โหลด Project Service Automation ไปจนถึงโซลูชันการรวม Finance จาก [ศูนย์ดาวน์โหลด Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) และทำตามคำแนะนำที่มาพร้อมกับโซลูชัน
