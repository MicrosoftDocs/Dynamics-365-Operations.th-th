---
title: ตั้งค่าคอนฟิกพารามิเตอร์การจัดการสวัสดิการสำหรับแต่ละบริษัท
description: ตั้งค่าคอนฟิกพารามิเตอร์สำหรับการจัดการสวัสดิการสำหรับแต่ละบริษัทใน Microsoft Dynamics 365 Human Resources
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/05/2021
ms.locfileid: "4984611"
---
# <a name="configure-benefits-management-parameters-per-company"></a>ตั้งค่าคอนฟิกพารามิเตอร์การจัดการสวัสดิการสำหรับแต่ละบริษัท

สำหรับแต่ละองค์กรที่มีสวัสดิการ คุณต้องตั้งค่าคอนฟิกการตั้งค่าสำหรับอีเมลการยืนยันสวัสดิการ

## <a name="configure-confirmation-email-settings"></a>ตั้งค่าคอนฟิกการตั้งค่าอีเมลการยืนยัน

1. ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ทรัพยากรบุคคล**

2. ในแท็บ **การจัดการสวัสดิการ** ระบุค่าในฟิลด์ต่อไปนี้: 

   | ฟิลด์ | คำอธิบาย |
   | --- | --- |
   | **ส่งอีเมลการยืนยัน** | เมื่อมีการเปิดใช้งานคุณลักษณะนี้ จะมีการส่งอีเมลการยืนยันให้กับพนักงาน เมื่อพวกเขาตรวจดูจากประสบการณ์ในการลงทะเบียนสวัสดิการในการบริการตนเองของพนักงาน |
   | **เท็มเพลตอีเมลการยืนยัน** | เลือกเท็มเพลตอีเมลขององค์กรที่จะใช้ เมื่อส่งการยืนยันการลงทะเบียน ถ้าคุณไม่เลือกเท็มเพลต จะมีการส่งอีเมลทั่วไปต่อไปนี้:<br><br>%EmployeeFirstName%,<br><br>ขอแสดงความยินดี คุณได้ทำการลงทะเบียนสวัสดิการเสร็จเรียบร้อยแล้ว<br><br>ขอบคุณ<br><Company/Org name> สวัสดิการ |
   | **ที่อยู่อีเมลผู้ส่งเริ่มต้น** | ที่อยู่อีเมลที่จะใช้เมื่อส่งอีเมลยืนยัน |

3. เลือก **บันทึก**