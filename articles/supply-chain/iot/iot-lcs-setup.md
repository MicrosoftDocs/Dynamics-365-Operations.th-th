---
title: ติดตั้ง Add-in เครื่องมือ IoT ใน LCS
description: หัวข้อนี้อธิบายถึงวิธีการติดตั้ง Add-in เครื่องมือ IoT ใน Microsoft Dynamics Lifecycle Services (LCS)
author: tonyafehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 89d2f53a761085949885c987d664654c3423524b
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645090"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>ติดตั้ง Add-in เครื่องมือ IoT ใน LCS

[!include [banner](../../includes/banner.md)]

หัวข้อนี้อธิบายถึงวิธีการติดตั้ง Add-in เครื่องมือ IoT ใน Microsoft Dynamics Lifecycle Services (LCS) โปรดทราบว่า add-in ไม่สามารถติดตั้งบนสภาพแวดล้อมการสาธิต/การทดลองได้ ก่อนที่คุณจะสามารถติดตั้ง Add-in คุณต้อง [สร้างทรัพยากร Azure](iot-azure-setup.md)

คุณสามารถตั้งค่าและตั้งค่าคอนฟิกเครื่องมือ IoT โดยไม่เขียนโค้ดใดๆ ต่อไปนี้เป็นขั้นตอนพื้นฐาน

1. [ตั้งค่าทรัพยากร Azure](iot-azure-setup.md) – สร้างฮับ IoT แคช Redis และ Key Vault ที่สามารถเข้าถึงได้จาก Supply Chain Management
2. [รูปแบบเค้าร่างข้อความของฮับ IoT](iot-schema-format.md) – ตั้งค่าคอนฟิกอุปกรณ์ให้ส่งข้อความไปยังฮับ IoT และกําหนดรูปแบบข้อความ JavaScript Object Notation (JSON)
3. ในการจัดการคุณลักษณะ ให้เปิดใช้งานแฟล็กคุณลักษณะเครื่องมือ IoT
4. ติดตั้ง Add-in ของเครื่องมือ IoT ใน Microsoft Dynamics Lifecycle Services (LCS) – ติดตั้ง Add-in LCS และตั้งค่าคอนฟิกข้อมูลลับ Azure (ตามที่อธิบายไว้ในหัวข้อนี้)
5. [ตั้งค่าเมตริก](iot-metrics-setup.md) – ตั้งค่าเมตริกใน Supply Chain Management
6. [การตั้งค่าสถานการณ์](iot-scenario-setup.md) – ตั้งค่าสถานการณ์ใน Supply Chain Management

## <a name="set-up-the-lcs-environment"></a>ตั้งค่าสภาพแวดล้อม LCS

1. เปิด LCS และไปที่สภาพแวดล้อม Microsoft Dynamics 365 Supply Chain Management ของคุณ
2. เลื่อนลงไปที่ส่วน **Add-in ของสภาพแวดล้อม**
3. เลือก **ติดตั้ง Add-in ใหม่** เพื่อแสดงรายการของ Add-in ที่เปิดใช้งานสำหรับสภาพแวดล้อม
4. ในกล่องโต้ตอบ **เลือก Add-in เพื่อติดตั้ง** ให้เลือก **เครื่องมือ IoT**
5. ในกล่องโต้ตอบ **ตั้งค่า Add-in** ให้ระบุรายละเอียดของฮับ IoT ของคุณและแคช Redis คุณสามารถค้นหาค่าที่จำเป็นใน Key Vault ที่คุณสร้างขึ้นใน [สร้างทรัพยากร Azure](iot-azure-setup.md)

    + **รหัสผู้เช่า** – ในพอร์ทัล Azure ให้ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ภาพรวม** และคัดลอกค่า **รหัสไดเรกทอรี** วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**
    + **ฮับเหตุการณ์ IoT ที่เข้ากันได้กับ Key Vault URI ของปลายทาง** – ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ภาพรวม** และคัดลอกค่า **ชื่อ DNS** วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**
    + **ฮับเหตุการณ์ IoT-ชื่อลับปลายทางที่เข้ากันได้** – ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ข้อมูลลับ** และคัดลอกชื่อข้อมูลลับที่สตริงการเชื่อมต่อฮับเหตุการณ์สำหรับฮับ IoT ถูกจัดเก็บไว้ วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**
    + **URI ของ Key Vault แคช Redis** – ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ภาพรวม** และคัดลอกค่า **ชื่อ DNS** วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**
    + **ชื่อข้อมูลลับปลายทางแคช Redis** – ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ข้อมูลลับ** และคัดลอกชื่อข้อมูลลับที่สตริงการเชื่อมต่อฮับสำหรับแคช Redis ถูกจัดเก็บไว้ วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**

6. เลือกกล่องกาเครื่องหมายเพื่อยอมรับข้อกำหนดและเงื่อนไข
7. เลือก **ติดตั้ง**
8. กล่องข้อความจะปรากฏขึ้นโดยระบุว่า "Add-in ถูกทริกเกอร์สำหรับการติดตั้งเสร็จเรียบร้อยแล้ว" เลือก **ตกลง**

ขณะนี้การตั้งค่า LCS เสร็จสมบูรณ์แล้ว ขั้นตอนต่อไปคือ [ตั้งค่าสถานการณ์จำลอง](iot-scenario-setup.md)

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>ถอนการติดตั้ง Add-in

1. ใน Supply Chain Management [ปิดใช้งานสถานการณ์จำลอง](iot-scenario-setup.md#disable-a-scenario)
2. ใน LCS ไปยังรายละเอียดสภาพแวดล้อม Supply Chain Management ของคุณ
3. เลื่อนลงไปที่ส่วน **Add-in ของสภาพแวดล้อม**
4. เลือก **ถอนการติดตั้ง** สำหรับ Add-in ครื่องมือ IoT


[!INCLUDE[footer-include](../../includes/footer-banner.md)]