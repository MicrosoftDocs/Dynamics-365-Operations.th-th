---
title: ตั้งค่าคอนฟิกระบบบริการตนเองของพนักงาน
description: ใน Microsoft Dynamics 365 Human Resources คุณสามารถตั้งค่าคอนฟิกของไทล์สำหรับการนำทางระดับบนสุดในบริการตนเองของพนักงาน
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cdc82c23635cc99c37aa770b996d9d2df43f5059
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324652"
---
# <a name="configure-employee-self-service"></a>ตั้งค่าคอนฟิกระบบบริการตนเองของพนักงาน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

ใน Microsoft Dynamics 365 Human Resources คุณสามารถตั้งค่าคอนฟิกของไทล์สำหรับการนำทางระดับบนสุดใน **บริการตนเองของพนักงาน** ไทล์แผนสิทธิประโยชน์ครอบคลุมผู้ใช้โดยตรงสำหรับแผนสิทธิประโยชน์ที่พวกเขามีสิทธิ์

## <a name="set-up-a-benefit-plans-tile"></a>ตั้งค่าไทล์ของแผนสิทธิประโยชน์

1. ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ค่าพารามิเตอร์การบริการตนเองของพนักงาน**

2. เลือกแท็บ **การตั้งค่าไทล์ของแผนสิทธิประโยชน์** จากนั้นเลือก **ใหม่**

3. ระบุค่าสำหรับฟิลด์ต่อไปนี้

   | ฟิลด์ | คำอธิบาย |
   | --- | --- |
   | **รหัสชนิดแผน** | ชนิดแผนที่จะแสดงเมื่อเลือกไทล์นี้ใน **ระบบบริการตนเองของสวัสดิการ** |
   | **รหัสไทล์** | ตัวระบุเฉพาะสำหรับไทล์ |
   | **ข้อความป้ายชื่อของไทล์** | ข้อความที่จะปรากฏสำหรับไทล์ใน **ระบบบริการตนเองของสวัสดิการ** |
   | **คำอธิบาย** | คำอธิบายเกี่ยวกับไทล์ |
   | **รูปภาพพื้นหลังของไทล์** | URL ของรูปภาพที่จะใช้สำหรับไทล์ (เลือกกำหนดได้) |
   | **ติดตามการลงทะเบียนที่เปิด** | เลือกตัวเลือกนี้เพื่อติดตามความคืบหน้าของการลงทะเบียนที่เปิดของแผนชนิดนี้ ตัวอย่างเช่น คุณอาจมีแผนที่สร้างโดยที่ **ชนิดแผน = อื่นๆ** แผนเหล่านี้อาจเป็นแผนที่เลือกระบุได้ ซึ่งคุณไม่ต้องการติดตามความคืบหน้าของการลงทะเบียน ถ้าคุณไม่ได้เลือกแผนชนิดนี้ แผนชนิดนี้จะถูกละเว้นเมื่อติดตามความคืบหน้าของการลงทะเบียนหรือการเสร็จสมบูรณ์ของการลงทะเบียนบนแท็บ **การลงทะเบียนที่เปิด** การตั้งค่านี้จะใช้กับชนิดของแผนที่เลือกไว้ให้กับรอบระยะเวลาและนิติบุคคลทั้งหมด |

4. เลือก **บันทึก**

## <a name="set-up-a-flex-credit-plan-tile"></a>ตั้งค่าไทล์แผนเครดิตการทำงานแบบยืดหยุ่นเวลา

1. ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **ค่าพารามิเตอร์การบริการตนเองของพนักงาน**

2. เลือกแท็บ **การตั้งค่าไทล์แผนเครดิตการทำงานแบบยืดหยุ่นเวลา** จากนั้นเลือก **ใหม่**

3. ระบุค่าสำหรับฟิลด์ต่อไปนี้

   | ฟิลด์ | คำอธิบาย |
   | --- | --- |
   | **รหัสเครดิตสวัสดิการ** | แผนโปรแกรมเครดิตแบบยืดหยุ่นที่จะแสดงเมื่อเลือกไทล์นี้ใน **ระบบบริการตนเองของสวัสดิการ** |
   | **รหัสไทล์** | ตัวระบุเฉพาะสำหรับไทล์ |
   | **ข้อความป้ายชื่อของไทล์** | ข้อความที่จะปรากฏสำหรับไทล์ใน **ระบบบริการตนเองของสวัสดิการ** |
   | **คำอธิบาย** | คำอธิบายเกี่ยวกับไทล์ |
   | **รูปภาพพื้นหลังของไทล์** | URL ของรูปภาพที่จะใช้สำหรับไทล์ (เลือกกำหนดได้) |
   | **ติดตามการลงทะเบียนที่เปิด** | เลือกตัวเลือกนี้เพื่อติดตามความคืบหน้าของการลงทะเบียนที่เปิดของแผนชนิดนี้ ตัวอย่างเช่น คุณอาจมีแผนที่สร้างโดยที่ **ชนิดแผน = อื่นๆ** แผนเหล่านี้อาจเป็นแผนที่เลือกระบุได้ ซึ่งคุณไม่ต้องการติดตามความคืบหน้าของการลงทะเบียน ถ้าคุณไม่ได้เลือกแผนชนิดนี้ แผนชนิดนี้จะถูกละเว้นเมื่อติดตามความคืบหน้าของการลงทะเบียนหรือการเสร็จสมบูรณ์ของการลงทะเบียนบนแท็บ **การลงทะเบียนที่เปิด** การตั้งค่านี้จะใช้กับชนิดของแผนที่เลือกไว้ให้กับรอบระยะเวลาและนิติบุคคลทั้งหมด |

4. เลือก **บันทึก**


[!INCLUDE[footer-include](../includes/footer-banner.md)]
