---
title: เริ่มต้นใช้งานการจัดการบริการ Add-On ของใบแจ้งหนี้ทางอิเล็กทรอนิกส์
description: หัวข้อนี้จะอธิบายวิธีการเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104443"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a>เริ่มต้นใช้งานการจัดการบริการ Add-On ของใบแจ้งหนี้ทางอิเล็กทรอนิกส์

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะดำเนินการกระบวนงานต่างๆ ในหัวข้อนี้ให้เสร็จสมบูรณ์ ต้องมีข้อกำหนดเบื้องต้นต่อไปนี้:

- คุณต้องมีสิทธิ์เข้าถึงบัญชี Microsoft Dynamics Lifecycle Services (LCS) ของคุณ
- คุณต้องมีโครงการ LCS ที่มีรุ่น 10.0.13 หรือใหม่กว่าของ Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management นอกจากนี้ แอปเหล่านี้ต้องถูกปรับใช้ในหนึ่งในภูมิศาสตร์ Azure ต่อไปนี้:

    - สหรัฐอเมริกาตะวันออก
    - สหรัฐอเมริกาตะวันตก
    - EU เหนือ
    - EU ตะวันตก

- คุณต้องมีสิทธิ์เข้าถึงบัญชี Dynamics 365 Regulatory Configuration Services (RCS) ของคุณ
- คุณต้องเปิดใช้งานคุณลักษณะที่ใช้ทั่วโลกสำหรับบัญชี RCS ของคุณในการจัดการคุณลักษณะ สำหรับข้อมูลเพิ่มเติม ดู [Regulatory Configuration Services (RCS) - คุณลักษณะที่ใช้ทั่วโลก](rcs-globalization-feature.md)
- คุณต้องสร้าง Key Vault และบัญชีการจัดเก็บใน Azure สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a>ติดตั้ง Add-on สำหรับ microservices ใน Lifecycle Services

1. ลงชื่อเข้าใช้บัญชี LCS ของคุณ
2. เลือกไทล์ **การจัดการคุณลักษณะพรีวิว**
3. ในส่วน **คุณลักษณะพรีวิวสำหรับสาธารณะ** ให้เลือก **บริการออกใบแจ้งหนี้อิเล็กทรอนิกส์**
4. ตรวจสอบให้แน่ใจว่าตัวเลือก **เปิดใช้งานคุณลักษณะพรีวิวแล้ว** ได้ถูกตั้งค่าเป็น **ใช่**

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a>ตั้งค่าพารามิเตอร์สำหรับการรวม RCS กับ add-on ใบแจ้งหนี้อิเล็กทรอนิกส์

1. ลงชื่อเข้าใช้บัญชี RCS ของคุณ
2. ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ในส่วน **ลิงค์ที่เกี่ยวข้อง** ให้เลือก **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**
3. บนแท็บ **บริการการออกใบแจ้งหนี้อิเล็กทรอนิกส์** ในฟิลด์ **URI ปลายทางของบริการ** ให้ป้อนปลายทางของบริการที่เหมาะสมสำหรับภูมิศาสตร์ Azure ของคุณ ดังแสดงในตารางต่อไปนี้

    | ภูมิศาสตร์ของ Datacenter Azure | URI ปลายทางของบริการ                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | สหรัฐอเมริกาตะวันออก                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | สหรัฐอเมริกาตะวันตก                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | EU เหนือ                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | EU ตะวันตก                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. ตรวจสอบว่ามีการตั้งค่าฟิลด์ **รหัสแอปพลิเคชัน** เป็น **0cdb527f-a8d1-4bf8-9436-b352c68682b2** ค่านี้เป็นค่าคงที่
5. ในฟิลด์ **รหัสสภาพแวดล้อม LCS** ป้อนรหัสของบัญชีการบอกรับเป็นสมาชิก LCS ของคุณ
6. เลือก **ตกลง** และจากนั้นปิดหน้า

## <a name="create-key-vault-secret"></a>สร้างข้อมูลลับของ Key Vault

1. ลงชื่อเข้าใช้บัญชี RCS ของคุณ
2. ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **สภาพแวดล้อม** ให้เลือกไทล์ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์**
3. บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมบริการ** และจากนั้น เลือก **พารามิเตอร์ Key Vault**
4. เลือก **สร้าง** เพื่อสร้างข้อมูลลับของ Key Vault
5. ในฟิลด์ **ชื่อ** ป้อนชื่อสำหรับข้อมูลลับของ Key Vault ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
6. ในฟิลด์ **URI ของ Key URI** ให้วางข้อมูลลับจาก Azure Key Suite
7. เลือก **บันทึก**

## <a name="create-storage-account-secret"></a>สร้างข้อมูลลับของบัญชีที่จัดเก็บ

1. บนหน้า **พารามิเตอร์ Key vault** ในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม**
2. ในฟิลด์ **ชื่อ** ป้อนชื่อข้อมูลลับของบัญชีที่จัดเก็บเดียวกัน ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
3. ในฟิลด์ **ชนิด** เลือก **ใบรับรอง**
4. เลือก **ตกลง** และจากนั้นปิดหน้า

## <a name="create-an-electronic-invoicing-add-on-environment"></a>สร้างสภาพแวดล้อม add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์

1. ลงชื่อเข้าใช้บัญชี RCS ของคุณ
2. ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **สภาพแวดล้อม** ให้เลือกไทล์ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์**

## <a name="create-a-service-environment"></a>สร้างสภาพแวดล้อมบริการ

1. บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมบริการ**
2. เลือก **สร้าง** เพื่อสร้างสภาพแวดล้อมบริการใหม่
3. ในฟิลด์ **ชื่อ** ป้อนชื่อของสภาพแวดล้อมการออกใบแจ้งหนี้อิเล็กทรอนิกส์ ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
4. ในฟิลด์ **ข้อมูลลับโทเค็น SAS ของที่จัดเก็บ** ให้เลือกชื่อของใบรับรองที่ต้องใช้ในการพิสูจน์ตัวจริงในการเข้าถึงบัญชีการจัดเก็บ
5. ในส่วน **ผู้ใช้** ให้เลือก **เพิ่ม** เพื่อเพิ่มผู้ใช้ที่ได้รับอนุญาตให้ส่งใบแจ้งหนี้อิเล็กทรอนิกส์ผ่านสภาพแวดล้อม และเชื่อมต่อกับบัญชีการจัดเก็บด้วย
6. ในฟิลด์ **รหัสผู้ใช้** ให้ป้อนนามแฝงของผู้ใช้ ในฟิลด์ **อีเมล** ป้อนอยู่อีเมลของผู้ใช้
7. เลือก **บันทึก**
8. ถ้าใบแจ้งหนี้เฉพาะประเทศ/ภูมิภาคของคุณ จำเป็นต้องมีกลุ่มของใบรับรองเพื่อใช้ลายเซ็นดิจิทัล บนบานหน้าต่างการดำเนินการ เลือก **พารามิเตอร์ Key Vault** แล้วเลือก **กลุ่มของใบรับรอง** และทำตามขั้นตอนเหล่านี้:

    1. เลือก **สร้าง** เพื่อสร้างกลุ่มของใบรับรอง
    2. ในฟิลด์ **ชื่อ** ป้อนชื่อของกลุ่มของใบรับรอง ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
    3. ในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม** เพื่อเพิ่มใบรับรองให้กับกลุ่ม
    4. ใช้ปุ่ม **ขึ้น** หรือ **ลง** เพื่อเปลี่ยนตําแหน่งของใบรับรองในกลุ่ม
    5. เลือก **ตกลง** และจากนั้นปิดหน้า
    6. ปิดหน้า
9. บนหน้า **สภาพแวดล้อมบริการ** บนบานหน้าต่างการดำเนินการ ให้เลือก **เผยแพร่** เพื่อเผยแพร่สภาพแวดล้อมไปยังระบบคลาวด์ ค่าของฟิลด์ **สถานะ** ถูกเปลี่ยนเป็น **เผยแพร่แล้ว**

## <a name="create-a-connected-application"></a>สร้างแอปพลิเคชันที่เชื่อมต่อ

1. บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **แอปพลิเคชันที่เชื่อมต่อ**
2. เลือก **สร้าง** เพื่อสร้างแอปพลิเคชันที่เชื่อมต่อ
3. ในฟิลด์ **ชื่อ** ให้ป้อนชื่อของแอปพลิเคชันที่จะเชื่อมต่อ
4. ในฟิลด์ **แอปพลิเคชัน** ให้ป้อน URL ของสภาพแวดล้อม Finance และ Supply Chain Management ที่จะเชื่อมต่อ
4. ในฟิลด์ **ผู้เช่า** ให้ป้อนผู้เช่าของสภาพแวดล้อม Finance และ Supply Chain Management
5. เลือก **บันทึก**
6. ในบานหน้าต่างการดำเนินการ ให้เลือก **ตรวจสอบการเชื่อมต่อ** เพื่อทดสอบการเชื่อมต่อกับสภาพแวดล้อม จากนั้น ปิดหน้า

## <a name="link-connected-applications-to-environments"></a>เชื่อมโยงแอปพลิเคชันที่เชื่อมต่อกับสภาพแวดล้อม

1. บนหน้า **การตั้งค่าสภาพแวดล้อม** ให้เลือก **สร้าง** เพื่อกําหนดแอปพลิเคชันที่เชื่อมต่อให้กับสภาพแวดล้อม
2. ในฟิลด์ **แอปพลิเคชันที่เชื่อมต่อ** ให้เลือกแอปพลิเคชันที่เชื่อมต่อ
3. ในฟิลด์ **สภาพแวดล้อมบริการ** เลือกสภาพแวดล้อมบริการ
4. เลือก **ตกลง** และจากนั้นปิดหน้า

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a>ตั้งค่าการรวม add-on ของการออกใบแจ้งหนี้อิเล็กทรอนิกส์ใน Finance และ Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>เปิดคุณลักษณะการรวมของ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์

1. ลงชื่อเข้าใช้อินสแตนซ์ Finance หรือ Supply Chain Management ของคุณ
2. ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้ค้นหาคุณลักษณะ **การรวม add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์** ถ้าคุณลักษณะนี้ไม่ปรากฏบนหน้า ให้เลือก **ตรวจสอบการอัปเดต**
3. เลือกคุณลักษณะ และจากนั้นเลือก **เปิดใช้งานตอนนี้**

### <a name="set-up-the-service-endpoint-url"></a>ตั้งค่า URL ปลายทางการบริการ

1. ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**
2. บนแท็บ **บริการการส่ง** ในฟิลด์ **URL ปลายทางของบริการ** ให้ป้อนปลายทางของบริการที่เหมาะสมสำหรับภูมิศาสตร์ Azure ของคุณ ดังแสดงในตารางต่อไปนี้

    | ภูมิศาสตร์ของ Datacenter Azure | URL ปลายทางของบริการ                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | สหรัฐอเมริกาตะวันออก                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | สหรัฐอเมริกาตะวันตก                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | EU เหนือ                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | EU ตะวันตก                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. ในฟิลด์ **สภาพแวดล้อม** ป้อนชื่อของสภาพแวดล้อม add-on ของการออกใบแจ้งหนี้อิเล็กทรอนิกส์
4. เลือก **ตกลง** และจากนั้นปิดหน้า
