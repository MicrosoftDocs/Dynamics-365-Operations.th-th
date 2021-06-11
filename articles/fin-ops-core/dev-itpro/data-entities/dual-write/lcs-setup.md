---
title: การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง จาก Microsoft Dynamics Lifecycle Services (LCS)
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103580"
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

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
