---
title: ตั้งค่าคอนฟิกพารามิเตอร์การจัดการสวัสดิการต่อบริษัท
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าคอนฟิกพารามิเตอร์สำหรับการจัดการสวัสดิการต่อบริษัทใน Microsoft Dynamics 365 Human Resources
author: twheeloc
ms.date: 8/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d0bc8d511126901be09028dc3c10636f2902e79
ms.sourcegitcommit: 8592c661b41f9cef8b7ef2863a3b97bf49a4e6f9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/26/2021
ms.locfileid: "7423316"
---
# <a name="configure-benefits-management-parameters-per-company"></a>ตั้งค่าคอนฟิกพารามิเตอร์การจัดการสวัสดิการสำหรับแต่ละบริษัท

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

สำหรับแต่ละองค์กรที่มีสวัสดิการ คุณต้องตั้งค่าคอนฟิกการตั้งค่าสำหรับอีเมลการยืนยันสวัสดิการ

## <a name="configure-confirmation-email-settings"></a>ตั้งค่าคอนฟิกการตั้งค่าอีเมลการยืนยัน

1. ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ทรัพยากรบุคคล**

2. ในแท็บ **การจัดการสวัสดิการ** ระบุค่าในฟิลด์ต่อไปนี้: 

   | ฟิลด์ | คำอธิบาย |
   | --- | --- |
   | **ส่งอีเมลการยืนยัน** | เมื่อมีการเปิดใช้งานคุณลักษณะนี้ จะมีการส่งอีเมลการยืนยันให้กับพนักงาน เมื่อพวกเขาตรวจดูจากประสบการณ์ในการลงทะเบียนสวัสดิการใน **บริการตนเองของพนักงาน** |
   | **เท็มเพลตอีเมลการยืนยัน** | เลือกเท็มเพลตอีเมลขององค์กรที่จะใช้ เมื่อส่งการยืนยันการลงทะเบียน ถ้าคุณไม่เลือกเท็มเพลต จะมีการส่งอีเมลทั่วไปต่อไปนี้:<br><br>%EmployeeFirstName%<br><br>ขอแสดงความยินดี คุณได้ทำการลงทะเบียนสวัสดิการเสร็จเรียบร้อยแล้ว<br><br>ขอบคุณ<br><Company/Org name> สวัสดิการ |
   | **ที่อยู่อีเมลผู้ส่งเริ่มต้น** | ที่อยู่อีเมลที่จะใช้เมื่อส่งอีเมลยืนยัน |

3. เลือก **บันทึก**

[!INCLUDE[footer-include](../includes/footer-banner.md)]
