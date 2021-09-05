---
title: การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง จาก Microsoft Dynamics Lifecycle Services (LCS)
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2cfe6d882c5de763164ddb4a344cba2991c88783
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416662"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้อธิบายวิธีการเปิดใช้งานการรวมแบบสองทิศทางจาก Microsoft Dynamics Lifecycle Services (LCS)

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

คุณต้องทำการรวม Power Platform ให้เสร็จสิ้นตามที่อธิบายไว้ในหัวข้อต่อไปนี้

+ [การรวม Power Platform - เปิดใช้งานในระหว่างการปรับใช้สภาพแวดล้อม](../../power-platform/overview.md#enable-during-environment-deployment)
+ [การรวม Power Platform - ตั้งค่าหลังจากการปรับใช้สภาพแวดล้อม](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>ตั้งค่าการรวมแบบสองทิศทางสำหรับสภาพแวดล้อม Dataverse ใหม่

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าการรวมแบบสองทิศทางจากหน้า **รายละเอียดสภาพแวดล้อม** LCS

1. ในหน้า **รายละเอียดสภาพแวดล้อม** ให้ขยายส่วน **การรวม Power Platform**

2. เลือกปุ่ม **แอปพลิเคชันการรวมแบบสองทิศทาง**

    ![การรวม Power Platform](media/powerplat_integration_step2.png)

3. ตรวจสอบข้อกำหนดและเงื่อนไข จากนั้นเลือก **กำหนดค่า**

4. เลือก **ตกลง** เพื่อดำเนินการต่อ

5. คุณสามารถตรวจสอบความคืบหน้าโดยการรีเฟรชหน้ารายละเอียดสภาพแวดล้อมเป็นระยะๆ โดยปกติการตั้งค่าจะใช้เวลา 30 นาทีหรือน้อยกว่า  

6. เมื่อการตั้งค่าเสร็จสิ้น จะมีข้อความแจ้งคุณว่ากระบวนการประสบความสาเร็จหรือถ้ามีความล้มเหลว ถ้าการตั้งค่าล้มเหลว จะมีข้อความแสดงข้อผิดพลาดที่เกี่ยวข้องแสดงขึ้น คุณต้องแก้ไขข้อผิดพลาดใด ๆ ก่อนย้ายไปยังขั้นตอนถัดไป

7. เลือก **ลิงค์ไปยังสภาพแวดล้อม Power Platform** เพื่อสร้างลิงค์ระหว่าง Dataverse และฐานข้อมูลของสภาพแวดล้อมปัจจุบัน โดยปกติขั้นตอนนี้จะใช้เวลาน้อยกว่า 5 นาที

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="เชื่อมโยงกับสภาพแวดล้อม Power Platform":::

8. เมื่อการเชื่อมโยงเสร็จสมบูรณ์ ไฮเปอร์ลิงค์จะแสดงขึ้น ใช้ลิงค์เพื่อเข้าสู่ระบบพื้นที่การรวมแบบสองทิศทางในสภาพแวดล้อม Finance and Operations จากที่นั่น คุณสามารถตั้งค่าการแม็ปเอนทิตีได้

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>ตั้งค่าการรวมแบบสองทิศทางสำหรับสภาพแวดล้อม Dataverse ที่มีอยู่

เมื่อต้องการตั้งค่าการรวมแบบสองทิศทางให้กับสภาพแวดล้อม Dataverse ที่มีอยู่ คุณต้องสร้าง [ตั๋วสนับสนุน](../../lifecycle-services/lcs-support.md) Microsoft ตั๋วต้องรวม:

+ รหัสสภาพแวดล้อม Finance and Operations ของคุณ
+ ชื่อสภาพแวดล้อมของคุณจาก Lifecycle Services
+ รหัสองค์กร Dataverse หรือรหัสสภาพแวดล้อม Power Platform จากศูนย์การจัดการ Power Platform ในตั๋วของคุณ ให้ขอรหัสเป็นอินสแตนซ์ที่ใช้ในการรวม Power Platform

> [!NOTE]
> คุณไม่สามารถยกเลิกการเชื่อมโยงสภาพแวดล้อมได้โดยใช้ LCS เมื่อต้องการยกเลิกการเชื่อมโยงสภาพแวดล้อม ให้เปิดพื้นที่ทำงาน **การรวมข้อมูล** ในสภาพแวดล้อม Finance and Operations และจากนั้น เลือก **ยกเลิกการเชื่อมโยง**

## <a name="linking-mismatch"></a>การเชื่อมโยงไม่ตรงกัน

คุณสามารถเชื่อมโยงสภาพแวดล้อม LCS กับอินสแตนซ์ Dataverse ใดอินสแตนซ์หนึ่งได้ ขณะที่สภาพแวดล้อมการรวมแบบสองทิศทางของคุณเชื่อมโยงกับอินสแตนซ์ Dataverse อื่น การเชื่อมโยงไม่ตรงกันอาจทําให้เกิดลักษณะการทํางานที่ไม่คาดคิด และอาจส่งข้อมูลไปยังสภาพแวดล้อมที่ไม่ถูกต้อง สภาพแวดล้อมแนะนำที่จะใช้กับการรวมแบบสองทิศทาง คือสภาพแวดล้อมที่สร้างขึ้นเป็นส่วนหนึ่งของการรวม Power Platform และระยะยาว การสภาพแวดล้อมนี้จะเป็นเพียงวิธีเดียวที่คุณจะสามารถสร้างการเชื่อมโยงระหว่างสภาพแวดล้อมต่างๆ ได้

ถ้าสภาพแวดล้อมของคุณมีการเชื่อมโยงไม่ตรงกัน LCS จะแสดงคําเตือนในหน้ารายละเอียดสภาพแวดล้อมของคุณคล้ายกับ "Microsoft ตรวจพบว่าสภาพแวดล้อมของคุณได้รับการเชื่อมโยงกับผ่านการรวมแบบสองทิศทางไปยังปลายทางอื่นที่แตกต่างจากที่ระบุในการรวม Power Platform ซึ่งไม่แนะนำ":

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="การเชื่อมโยงการรวม Power Platform ไม่ตรงกัน":::

ถ้าคุณพบข้อผิดพลาดนี้ มีตัวเลือกสองตัวเลือก ตามความต้องการของคุณ

+ [ยกเลิกการเชื่อมโยงและเชื่อมโยงสภาพแวดล้อมการรวมแบบสองทิศทางใหม่ (รีเซ็ตหรือเปลี่ยนการเชื่อมโยง)](relink-environments.md#scenario-reset-or-change-linking) ตามที่ระบุบนหน้ารายละเอียดสภาพแวดล้อม LCS ของคุณ นี่เป็นตัวเลือกที่ดีที่สุด เนื่องจากคุณสามารถเรียกใช้โดยไม่ได้รับการสนับสนุนของ Microsoft  
+ ถ้าคุณต้องการเก็บการเชื่อมโยงของคุณไว้ในการรวมแบบสองทิศทาง คุณสามารถขอความช่วยเหลือจาก Microsoft Support เพื่อเปลี่ยนการรวม Power Platform เพื่อใช้สภาพแวดล้อม Dataverse ที่มีอยู่ตามที่ได้บันทึกเอกสารในส่วนก่อนหน้านี้  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
