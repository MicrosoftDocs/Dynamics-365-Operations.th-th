---
title: สร้างบัญชีการจัดเก็บของ Azure และ Key Vault
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างบัญชีการจัดเก็บของ Azure และ Key Vault
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d076aa5230437d1ef90f6b46d49ee4dea526db24
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104240"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>สร้างบัญชีการจัดเก็บของ Azure และ Key Vault

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะสามารถทำขั้นตอนต่างๆ ให้เสร็จสมบูรณ์ในหัวข้อนี้ คุณต้องแน่ใจว่างานต่อไปนี้ได้เสร็จสมบูรณ์แล้ว:

- สร้างทรัพยากร Key Vault ใน Azure สำหรับข้อมูลเพิ่มเติม ให้ดู [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview)
- สร้างบัญชีการจัดเก็บของ Azure (ที่จัดเก็บ Blob) สำหรับข้อมูลเพิ่มเติม ให้ดู [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/)

## <a name="overview"></a>ภาพรวม

ในหัวข้อนี้ คุณจะดำเนินการขั้นตอนหลักสองขั้นตอนต่อไปนี้:

- ตั้งค่าบัญชีการจัดเก็บของ Azure เพื่อให้ได้ URI บัญชีการจัดเก็บ
- ตั้งค่า Key Vault สำหรับจัดเก็บ URI ของบัญชีการจัดเก็บ

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>ตั้งค่าบัญชีการจัดเก็บของ Azure เพื่อให้ได้ URI ของบัญชีการจัดเก็บ

1. เปิดบัญชีจัดการเก็บที่คุณวางแผนที่จะใช้กับ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์
2. ไปที่ **บริการ Blob** \> **คอนเทนเนอร์** และสร้างคอนเทนเนอร์ใหม่
3. ป้อนชื่อสำหรับคอนเทนเนอร์ และตั้งค่าฟิลด์ **ระดับการเข้าถึงสาธารณะ** เป็น **ส่วนตัว (ไม่มีการเข้าถึงแบบไม่ระบุชื่อ)**
4. เปิดคอนเทนเนอร์ และไปที่ **การตั้งค่า \> นโยบายการเข้าถึง**
5. เลือก **เพิ่มนโยบาย** เพื่อเพิ่มนโยบายการเข้าถึงการจัดเก็บ
6. ตั้งค่าฟิลด์ **ตัวระบุ** และ **สิทธิ์** ตามความเหมาะสม ในฟิลด์ **สิทธิ์** คุณควรเลือกสิทธิ์ทั้งหมด

    ![สิทธิ์การจัดเก็บ Granting Blob](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. ป้อนวันที่เริ่มต้นและวันที่หมดอายุ วันหมดอายุควรอยู่ในอนาคต
8. เลือก **ตกลง** เพื่อบันทึกนโยบาย แล้วบันทึกการเปลี่ยนแปลงของคุณไปยังคอนเทนเนอร์
9. กลับไปยังบัญชีการจัดเก็บ และเปิด **Storage Explorer (การแสดงตัวอย่าง)**
10. คลิกขวาที่คอนเทนเนอร์ แล้วเลือก **รับลายเซ็นที่ใช้การเข้าถึงร่วมกัน**
11. ในกล่องโต้ตอบ **ลายเซ็นที่ใช้การเข้าถึงร่วมกัน** ให้คัดลอกและจัดเก็บค่าในฟิลด์ **URI** ค่านี้จะใช้ในขั้นตอนถัดไป และจะถูกเรียกว่า *URI ลายเซ็นที่ใช้การเข้าถึงร่วมกัน*

    ![การเลือกและการคัดลอกค่า URI](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>ตั้งค่า Key Vault สำหรับจัดเก็บ URI ของบัญชีการจัดเก็บ

1. เปิด Key Vault ที่คุณตั้งใจที่จะใช้กับ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์
2. ไปที่ **การตั้งค่า** \> **ความลับ** แล้วเลือก **สร้าง/นำเข้า** เพื่อสร้างความลับใหม่
3. บนหน้า **สร้างความลับ** ในฟิลด์ **ตัวเลือกการอัพโหลด** ให้เลือก **ด้วยตนเอง**
4. ป้อนชื่อของความลับ ชื่อนี้จะใช้ในระหว่างการตั้งค่าบริการใน Regulatory Configuration Service (RCS) และจะถูกอ้างอิงถึง *ชื่อความลับของ Key Vault*
5. ในฟิลด์ **ค่า** ให้เลือก **URI ลายเซ็นที่ใช้การเข้าถึงร่วมกัน** แล้วเลือก **สร้าง**
6. ตั้งค่านโยบายการเข้าถึงเพื่อให้ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ แก้ไขระดับของการเข้าถึงลับที่คุณสร้างขึ้น ไปที่ **การตั้งค่า \> นโยบายการเข้าถึง** และเลือก **เพิ่มนโยบายการเข้าถึง**
7. ตั้งค่าสิทธิ์ลับ สำหรับการดำเนินงาน **รับ** และ **รายการ**

    ![การให้สิทธิการเข้าถึงบริการ](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. ตั้งค่าสิทธิ์ใบรับรอบ สำหรับการดำเนินงาน **รับ** และ **รายการ**

    ![การให้สิทธิ์ใบรับรอง](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. ในกล่องโต้ตอบ **หลัก** ให้เลือกหลักโดยการเพิ่ม **add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์**
10. เลือก **เพิ่ม** แล้วเลือก **บันทึกการเปลี่ยนแปลง Key Vault**
11. บนหน้า **ภาพรวม** สำเนาค่า **ชื่อ DNS** สำหรับ Key Vault ค่านี้จะใช้ในระหว่างการตั้งค่าของบริการใน RCS และจะถูกอ้างอิงเป็น *URI ของ Key Vault*
